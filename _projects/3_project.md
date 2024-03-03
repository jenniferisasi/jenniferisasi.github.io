---
layout: page
title: "Euskal Literatura beste hizkuntzetan"
description: A map of translations of Basque literary works
img: /assets/img/euskal_literatura/euskal-lit_0.png
importance: 3
category: fun
---

La Universidad del País Vasco ofrece, en abierto, un [catálogo de las traducciones de la literatura en euskera](https://www.ehu.eus/ehg/eli/?z=bila&m=osorik) a otros idiomas recopilado por [Elizabete Manterola](http://istres.letras.ulisboa.pt/manterola/) hacia 2012 para su tesis. La base de datos recoge 1.595 entradas en total, con datos como el título y autor/a original de la obra, su fecha de publicación, editoriales, traductores, idioma de la traducción, etc. Se trata, por tanto, de un corpus muy rico que permite explorar al interesado en la literatura en euskera bastantes variables. 

Yo, por curiosidad, decidí realizar unas visualizaciones para ver la extensión de la literatura vasca por el mundo, así como la red de autores y traductores que se ha formado a lo largo de los años. Para ello, he ampliado la base de datos con cuatro columnas de coordenadas (la latitud y longitud del lugar de publicación original y las mismas para el lugar de publicación de la traducción). 

Estos son los resultados visualizados en la plataforma [kepler.gl](https://kepler.gl/demo): 

A vista de pájaro podemos observar que la literatura vasca ha llegado a muchos puntos del planeta y en varios idiomas. En la siguiente captura de pantalla vemos que el lugar de mayor producción de originales (en tonos tierra) es el País Vasco, pero también destaca Reno, en Nevada, Estados Unidos, en su publicación y exportación de obras en euskera hacia España, Italia y Rusia.

<img src="/assets/img/euskal_literatura/euskal-lit_2.png" alt="Visualización de las traducciones de literatura vasca a otros idiomas/países en un mapa"  title="Lugares de traducción de la literatura vasca"  width="80%" height="80%" />

Al acercarnos más al panorama europeo, observamos la gran cantidad de idiomas a las que se ha traducido la literatura vasca por su distribución a muchos países en Europa y varias comunidades autónomas dentro de la península.   

<img src="/assets/img/euskal_literatura/euskal-lit_1.png" alt="Visualización de las traducciones de literatura vasca a otros idiomas/países en Europa"  title="Traducción de la literatura vasca en Europa"  width="80%" height="80%" />

Y ¿quiénes son los autores más traducidos? No es sorpresa que destaquen Bernardo Atxaga,  Mariasun Landa Etxebeste, Kirmen Uribe o Piedad Ateka. 

<img src="/assets/img/euskal_literatura/euskal-lit_3.png" alt="Visualización del número de traducciones por autor/a en Europa"  title="Traducciones por autor/a en Europa"  width="80%" height="80%" />

Kepler también nos permite ver la evolución de nuestra red de traducciones a lo largo del tiempo. En este caso, y como es normal por la trayectoria de la literatura en euskera y la historia del País Vasco en general, el número de traducciones ha ido aumentando hacia finales de la década de los 90 y, sobre todo, a partir del año 2000. 

<iframe src="/assets/img/euskal_literatura/euskal-lit-map.html" width="50%" heigth="100%" > </iframe>
Una visualización geográfica nos permite observar la expansión de la literatura por el planeta. No obstante, ello invisibiliza la labor de autores y traductores en tanto que sus nombres no aparecen - se pueden mostrar pero no aportan nada más que una gran cantidad de letras que impiden su lectura. Para observar quién traduce a quién, y cuánto, una visualización de red es mucho más adecuada. Así, vemos que Bernardo Atxaga es el más traducido según nuestros datos y, curiosamente, se traduce al castellano a sí mismo (línea rosa junto a su nodo). 



<img src="/assets/img/euskal_literatura/euskal-lit_4.png" alt="Visualización de la red de autores y traductores"  title="Red de autores y traductores de literatura en euskera"  width="80%" height="80%" />

A 10 de noviembre de 2019 (fecha en que he realizado este mapa) la función de exportación del mapa en formato HTML funciona pero no se visualiza en la web. No obstante, te invito a [descargarte el archivo JSON](/assets/datasets/euskal_literatura.json) de mi repositorio y cargarlo en [kepler.gl](https://kepler.gl) tú mismo/a para poder interactuar con el mapa.  

Para saber más sobre la euskal literatura en traducción, puedes consultar las siguientes referencias: 

- Auzmendi, Lurdes. "El reconocimiento de la traducción literaria en lengua vasca en España". XXXIII *Encuentros de Escritores y Críticos en Verines Creadores en la sombra. La traducción literaria en la actualidad*, 2017

- López Gaseni, José Manuel. "Literatura traducida." *Portal de Literatura Vasca*. http://www.basqueliterature.com/es/basque/historia/itzulia 

- López Gaseni, Jose Manuel (2000) *Euskarara itzulitako haur eta gazte literatura: funtzioak, eraginak eta itzulpen-estrategiak*. Bilbao: Universidad del País Vasco.

- Manterola Agirrezabalaga, Elizabete. 2014. «Una mirada hacia la traducción literaria del euskera al castellano». *Hermeneus: Revista de la Facultad de Traducción e Interpretación de Soria*, n. 16: 177–208.

- —. 2014. *La literatura vasca traducida*. Bern/New York: Peter Lang.

- Pérez Isasi, Santiago. La literatura vasca en el contexto de los Estudios Ibéricos: Historiografía y traducción. *1616: Anuario de Literatura Comparada*, 4, 2014, pp. 107-126.
