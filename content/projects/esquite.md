---
title: Esquite
template: page
summary: Framework for parallel corpora
img: images/esquites.jpg
importance: 1
category: work
---

## What is Esquite?

Esquite is a framework intended for people who have parallel corpus
(bilingual texts) and wish to get a web system that allows them to upload
documents, manage them and perform queries based on words and phrases in both
languages.

### Features

* Perform advanced queries in your parallel corpus thanks to the search engine
[*Elasticsearch*](https://www.elastic.co/es/)
* Manage your documents through the corpus administrator
* Customization of the Web Client
    * Colors
    * Keyboard with special characters (useful for non-english languages)
    * Add custom `html` information to the views: **help**, **about corpus**,
      **links**, **etc**.
* New features in development


!TEMPLATE!
<div class="row">
    <div class="col-sm mt-6 mt-md-0">
        {{ figure(path="images/tsunkua_preview.png",title="Main page of the framework. You can select a lang and made searches", class="img-fluid rounded z-depth-1") }}
    </div>
    <div class="col-sm mt-6 mt-md-0">
        {{ figure(path="images/tsunkua_export_csv.png",title="Results can be downloaded as csv format", class="img-fluid rounded z-depth-1") }}
    </div>
</div>
<div class="caption">
    Main screens of the web framework. You can search by languages (On the left) and download the results as <code>.csv</code> (on the right)
</div>
!TEMPLATE!

### Instances

- [Tsunkua](https://tsunkua.elotl.mx/): Otomí-Spanish parallel corpus
- [Kolo](https://kolo.elotl.mx/): Mixteco-Spanish parallel corpus
- [Axolotl](https://axolotl-corpus.mx/search): Náhuatl-Spanish corpus (Old version)

## Docker image alternative: Esquite-Docker

Alternatively, it is possible to use Esquite and deploy it in an easier way by
using our official Docker image.

Detailed documentation is available on:

- [Esquite-Docker Github](https://github.com/ElotlMX/Esquite-docker)
- [Esquite-Docker Dockerhub](https://hub.docker.com/r/elotlmx/esquite)

## Contact

Are you a speaker/researcher of a minority language and would like to upload
your parallel corpus? Contact us: `contacto at elotl.mx`

### Collaborators

* **Collaborator:** Xim ([@XimGutierrez](https://twitter.com/XimGutirrez)) - `xim at unam.mx`
* **Mantainer:** Diego B. ([@umoqnier](https://mstdn.mx/@umoqnier)) - `dbarriga at ciencias.unam.mx`
* **DevOps**: Javier ([@jusafing](https://twitter.com/jusafing)) - `jusafing at jusanet.org`

### Community

* Twitter: [@elotlmx](https://twitter.com/elotlmx)
* Site: [https://elotl.mx/](https://elotl.mx)
* Email: `contacto at elotl.mx`
