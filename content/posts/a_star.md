Title: Innovación en búsqueda multi-objetivo para robots móviles
Date: 2025-09-01 9:18
Summary: Inteligencia artificial, un enfoque moderno
Category: algorithms
Status: Published
hide_from_latest: false
slug: multiobjetive-search
***

Esta semana leí el artículo titulado [*Combined improved A\* and
greedy algorithm for path planning of multi‑objective mobile robot*
(Xiang et. al,
2022)](https://www.nature.com/articles/s41598-022-17684-0). En este
proponen mejoras al algoritmo $A*$, primero a la función de evaluación
para que converja más rápido, después podando los nodos innecesarios
mientras mantienen solo los nodos de puntos de inflexión necesarios y,
por último, combinándolo con el algoritmo voraz (*greedy*) para
planeación de rutas optimas. Prometen mejorar un 5% y rutas más
*smooth*.

### Busqueda del mejor camino

El artículo esta en el contexto de los *Autonomus Mobile Robots (AMR)*
cuyo objetivo es encontrar el camino más corto, sin colisiones, desde
un origen a un destino. Los algoritmos propuestos son probados
diferentes grids con obstaculos como se muestra en la imagen 1. La
planeación de caminos óptimos en *AMR* es un problema de optimización
restringido por lo que pueden utilizarse una amplia variedad de
algoritmos como algoritmos genéticos, Dijkstra, *Machine Learning* y
$A*$.

!TEMPLATE!  
<div class="row"> 
	<div class="col-sm mt-3 mt-md-0"> 
	{{figure(path="images/grid.png",title="example image", class="img-fluid rounded z-depth-1") }} </div>
</div> 
<div class="caption"> 
	Tres diferentes grids <b>a) 20x20</b> <b>b) 30x30</b> <b>c) 50x50</b>
</div>
!TEMPLATE!


### A\*

Particularmente, el algoritmo de $A*$ es un algoritmo basado en
heurísticas de tal forma que la función de evaluación es del estilo
$F(n) = G(n) + H(n)$ donde $G(n)$ será la función de costos y $H(n)$
la heurística. La correcta elección de $F(n)$ impactará en la calidad
del algoritmo.

$A*$ es uno de los algoritmos más eficientes buscando el camino más
corto en un ambiente estático. Sin embargo, el algoritmo tradicional
tiene problemas con búsqueda en ramas redundantes. Se han propuesto
mejoras para invalidar nodos redundantes, utilizar la información del
problema, como los obstáculos en la heurística, o apalancarse de la
resolución del grid para descomponer la búsqueda del camino en
segmentos para que el robot seleccione dinámicamente la mejor
opción. Aquí es claro como el modelado del ambiente es crucial para
tener un mejor desempeño.

Me sorprende ver como en investigaciones de vanguardia siguen
presentes elementos abordados en la clase de Inteligencia Artificial
del programa de maestría en el que estoy (PCIC). Por ejemplo, la
heurística utilizada en el artículo será la distancia Euclidiana con
mejoras para tomar en cuenta obstáculos, pesar mejor si se está
aproximando el robot al objetivo y constantes que pesaran que tanto se
toman en cuenta dichas mejoras.
	
Es claro como la implementación de algoritmos a entornos de la
"realidad" complica los supuestos teórico aunque la esencia se
mantiene. Detalles como la suavidad del camino o reducir el espacio de
búsqueda de nodos basándose en el angulo que forman son detalles que
en el entorno definido impactaron en el performance.

### De objetivo individual a multiobjetivos

El algoritmo $A*$ tradicional solo es adecuado para búsqueda de
objetivos individuales. Para multiples objetivos tiene poca
eficiencia. En general, las tareas de *AMR* no se limitan a este tipo
de problemas, si no que, se busca el mejor camino basándose en
multiobjetivos.

Aquí es donde entra la idea del algoritmo voraz propuesto en este
artículo. En combinación con $A\*$ mejoró la eficiencia de
planificación de caminos. Combinando la selección ordenada del camino
basándose en $F(n)$ del $A*$ con la introducción de nodos intermedios
con una estrategia voraz obtuvieron una mejora en el performance de
aproximadamente 5%. Esto puede sonar poco pero consideremos que están
mejorando el performance de un algoritmo que ya es bastante
eficiente. También, a escala industrial una mejora acumulativa puede
suponer ahorros millonarios.

La complejidad del algoritmo, por otro lado, no es tan buena. Por un
lado, $A*$ tiene una complejidad $O(s^2)$, donde $s$ será el número
de nodos. Esto es solo para la objetivo singular. Si agregamos la
complejidad de agregar las permutaciones para considerar los nodos
intermedios óptimos, para multiobjetivos, tendremos una complejidad de
$O((n!)s^2)$. Considerando las mejoras agregadas al $A*$ original,
esto es que dependerá de los puntos $n-m$ donde $n$ sera la cantidad
de nodos intermedios y $m$ la cantidad de nodos restantes a explorar
dada una frontera en un segmento seleccionado, obtenemos la
complejidad de $O(((n-m)!)s^2)$. Esto significa que para entornos con
un grid muy granular o ambiantes grande donde el camino sea largo no
sería escalable este algoritmo.

!TEMPLATE!  
<div class="row justify-content-center"> 
	<div class="col-sm mt-3 mt-md-0"> 
	{{figure(path="images/multiobjetive_path.png",title="example image", class="img-fluid rounded z-depth-1") }} 
	</div> 
</div> 
<div class="caption"> Camino multiobjetivo calculado </div>
!TEMPLATE!

### Conclusiones

- Vemos la aplicación de algoritmos bien conocidos[^1] en
  investigaciones novedosas que pueden ser aplicadas al ámbito
  industrial.
- Combinar el algoritmo $A*$ con el algoritmo voraz para búsqueda de
  caminos óptimos multi-objetivos parece mejorar el performance del
  trazado del camino aunque la complejidad es considerable.
- Se tiene que considerar el ambiente para mejorar el performance a
  diferencia del algoritmo en la literatura.

[^1]: Depende a quien le preguntes claro
