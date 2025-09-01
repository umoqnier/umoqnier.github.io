Title: Sobre el juego de la imitación y su vigencia
Date: 2025-08-21 21:53
Summary: Una crítica a la propuesta de Turing
Category: computer-theory
Status: Published
hide_from_latest: false
slug: imitation-game
***

En su famoso artículo "Computing Machinery and Intelligence" (Turing,
1950), Alan Turing busca de forma precisa y digerible responder a la
pregunta **¿Pueden una máquina pensar?** Para lograrlo propone
realizar un ejercicio, un juego cuyo nombre es *El juego de la
imitación* y que es ampliamente conocido en nuestros días como el
*Test de Turing*. El juego consiste, parafraseando, en los siguientes
puntos:

- Habrá tres entes. Una persona que interrogará (`I`), una persona
  interrogada (`P`) y una máquina/computadora digital (`M`)[^1].
- El interrogador estará situado en una habitación aparte.
- El juego consiste en que `I` debe determinar quien de los dos entes
  restantes es `P` y quien es `M` con base en una serie de preguntas
  escritas a traves de una terminal.


En este post indagaremos sobre si esta propuesta sigue siendo
relevante y si podemos obtener una respuesta satisfactoria de parte de
Mr. Turing.

### Preguntar o no preguntar (?)

Intentar responder la controversial pregunta no es tarea fácil y menos
en 1950 cuando fue publicado el artículo. Tanto alboroto causaba el
ejercicio que, una vez definido el juego de la imitación, Turing
dedica el resto del artículo en abordar las posibles contra
argumentaciones y críticas que pudiera tener el ejercicio mental
propuesto.

Comienza preguntándose si es útil y si es un buen enfoque tratar de
llegar a una respuesta con un juego basado en preguntas. Probablemente
Turing propone esta metodología como consecuencia de la época, considerando
que las computadoras estaban en una etapa temprana y que se asemejaban
más a lo que consideramos maquinaría industrial que a lo que tenemos
hoy día en nuestros hogares o bolsillos. 

Turing sostiene que el ejercicio de realizar y responder preguntas es
suficiente para abarcar (o al menos simular) casi cualquier actividad
de la vida humana. Esto me parece razonable considerando que Socrates
ya lo proponía como un método para encontrar la verdad filosofal.

### Actuar bien

Naturalmente se atienden las limitantes de las computadoras de la
época alegando que conviene tener en mente que "existirán computadoras
que actuaran bien" o dicho en otros términos, existirán máquinas que
podrán imitar efectivamente la actividad humana, al menos en un
entorno controlado.

Aquí vemos la inclinación de Turing a favor de las máquinas. Incluso
vemos que retoma el concepto de máquina universal y advierte que
"todos (procesos computacionales) pueden efectuarse en una sola
computadora digital, convenientemente programada en cada caso". Me
parece *shockeante* reconocer que su predicción fue relativamente
acertada considerando la adopción masiva de herramientas con interface
textual de pregunta-respuesta como los *Large Language Models, LLMS*,
o, más bien, ¿Será que el desarrollo de esta tecnología fue inspirada
por las propuestas de Turing? Queda como ejercicio al lector la
respuesta de esta pregunta. Donde no acertó fue en sostener que "a
finales de siglo podrá hablarse de maquinas sin levantar
controversias". Este claramente no es el caso ya que el debate sigue
en nuestros días.

### Objeciones varias

Como ya mencioné, buena parte del texto es ocupada para abordar e
intentar refutar las objeciones que pueden hacerse sobre el
tema. Estas objeciones son tan variadas que van desde lo teológico;
que alega que el pensamiento es una función del alma inmortal dotada
por dios; cuestiones matemáticas, como el teorema de incompletitud de
Gödel, que indica que hay cosas que las máquinas digitales, basadas en
sistemas lógicos, no pueden efectuar; argumentos sobre la conciencia
que apunta que las máquinas, a pesar de imitar adecuadamente, no son
conscientes de lo que esta haciendo, ni sentir; la objeción de Ada
Lovelace que menciona que las computadoras no están hechas para crear
nada si no que están supeditadas a la programación que ordenemos; o
el argumento más simple y poderoso que es "las máquinas son feas" que
en todo caso es sorteado por Turing atajandose de máquinas abstractas
que son "más ficciones matemáticas que objetos físicos".

Omitiendo varias objeciones abordadas me detengo en la más curiosa en
mi opinión y es que Turing, fiel creyente de la clarividencia y la
telepatía, plantea que si el preguntador es una persona sensible a
psicosínesis puede estropear el test por lo que sugiere depurar la
prueba con una "habitación a prueba de telepatía". Esto rara vez
se menciona al hablar de la prueba de Turing, probablemente por que
le quitaría credibilidad al famoso computólogo, y es que la telepatía
no tiene sustento racional ni científico cayendo en el campo de los
pensamiento oscuros o sea de la charlatanería.

### Aprendizaje

Turing admite que no tiene ningún punto fuerte, hasta el momento, para
derrumbar todas las objeciones antes mencionadas. Sin embargo, se
propone a mostrar evidencia en favor de su punto de vista. Esta
sección se titula "Máquinas que aprenden" y no se me pudieron saltar
más los ojos cuando leí este título teniendo a un lado mi libro de
*Machine Learning with `pytorch`*. 

Turing empuja la idea de que se pueden "inyectar ideas" en máquinas
así como en mentes, que hay procesos mentales que pueden ser descritos
en pasos puramente mecánicos y sostiene, no con argumentos
convincentes si no como "una letanía destinada a inculcar una
creencia", que será cuestión de tiempo para que los avances
ingenieriles permitan el desarrollo de computadoras con la suficiente
memoria y poder de computo para jugar bien al juego de la imitación.

En ese sentido hace especial énfasis en la imitación de la mente
humana, desde el estado inicial de la mente al nacer, la educación que
se nos da y la adquisición de experiencias. "¿Por qué no establecer un
programa que simula una mente infantil?" concluye a la que habrá que
enseñarle a resolver alguna tarea, comprobar si aprendió bien y luego
repetir el ciclo. No es muy distinta de la definición de Mitchell,
1997:

> "A computer program is said to learn from experience E with respect
> to some class of tasks T and performance measure P, if its
> performance at tasks in T, as measured by P, improves with
> experience E."
>
> *Machine Learning, Tom M. Mitchell (1997)*

Añade que el lenguaje con el que se debe enseñar a la máquina debe ser
simbólico, que la máquina puede que tenga un comportamiento que no
entenderemos o puramente aleatorio y advierte que sería lo adecuado
para que la máquina efectivamente aprenda "Como probablemente existe
un gran número de soluciones satisfactorias, el método aleatorio
parece mejor que el sistemático". Me sorprende como toda un área
moderna de la inteligencia artificial como el *Machine Learning* es,
con varias acotaciones, una inspiración directa de lo que expone
Turing en esta parte de su texto.

### Conclusión

En conclusión, considero que el juego de la imitación fue un buen
ejercicio mental para la época en la que se pensó, considerando los
conocimientos, críticas y avances en términos computacionales (siendo
estos los últimos aun prematuros). Sin embargo, es evidente que este
ejercicio ya esta rebasado y que hoy día, por ejemplo, un número de
personas nada despreciable considera que los modelos del lenguaje con
los que interactúa son entes que sienten, amigos con quienes hablar
del día a día e incluso acompañantes amorosos virtuales[^2].

Con el conocimiento actual y los desarrollos del área de inteligencia
artificial podemos decir que las computadoras, al menos
algunas, ya juegan suficientemente bien el juego de la
imitación. Es ambicioso intentar responder la pregunta inicial
**¿Puede una máquinas pensar?** Pero, si pueden imitar el
comportamiento humano tan bien que no sean distinguibles para las
personas, ¿vale la pena responder la pregunta? Creo que esa es la
premisa fundamental del juego de la imitación.

Por otro lado, Turing sienta las bases conceptuales y se adelanta unas
buenas décadas al surgimiento de la disciplina del **aprendizaje de
máquina** y eso es lo que me parece notable de su artículo más haya
del juego de la imitación. Recordemos que la adopción de este enfoque
para resolución de problemas fue posible gracias al avance ingenieril
que propició la creación de computadoras más eficientes, poderosas y
capaces. Esto es justo lo que Turing deja tácito en su escrito y, en
ese sentido, podemos darle la razón a Mr. Turing.  Quizá si tenía algo
de telépata después de todo[^3].

[^1]: En adelante trataré indistintamente máquina y computadora
    digital simplificando a computadora por practicidad.
[^2]: https://www.youtube.com/watch?v=XZ7XTTaXfOk
[^3]: Es una broma, todo el mundo sabe que la telepatía es una estafa
    :)
