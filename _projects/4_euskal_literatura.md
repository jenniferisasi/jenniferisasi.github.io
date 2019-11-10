---
layout: page
title: "Euskal Literatura beste hizkuntzetan"
description: A map of translations of Basque literary works
img: /assets/img/euskal_literatura/euskal-lit_0.png
tags: 
- euskal literatura
- humanidades digitales
- digital humanities
- humanitate digitalak
---

La Universidad del País Vasco ofrece, en abierto, un catálogo de las traducciones de la literatura en euskera (o vasco) a otros idiomas recopilado por Elizabete Manterola hacia 2012 para su tesis. La base de datos recoge 1.595 entradas en total, con datos como el título y autor/a original de la obra, su fecha de publicación, editoriales, traductores, idioma de la traducción, etc. Se trata, por tanto, de un corpus muy rico que permite explorar al interesado en la literatura en euskera bastantes variables. 

Yo, por curiosidad, decidí realizar unas visualizaciones para ver la extensión de la literatura vasca por el mundo, así como la red de autores y traductores que se ha formado a lo largo de los años. Para ello, he ampliado la base de datos con cuatro columnas de coordenadas (la latitud y longitud del lugar de publicación original y las mismas para el lugar de publicación de la traducción). 

Estos son los resultados visualizados en la plataforma [kepler.gl](https://kepler.gl/demo): 

A vista de pájaro podemos observar que la literatura vasca ha llegado a muchos puntos del planeta y en varios idiomas. En la siguiente captura de pantalla vemos que el lugar de mayor producción de originales (en tonos tierra) es el País Vasco, pero también destaca Reno, en Nevada, Estados Unidos, en su publicación y exportación de obras en euskera hacia España, Italia y Rusia. 

![euskal-lit_2](/Users/jenniferisasi/Documents/GitHub/jenniferisasi.github.io/assets/img/euskal_literatura/euskal-lit_2.png)



Al acercarnos más al panorama europeo, observamos la gran cantidad de idiomas a las que se ha traducido la literatura vasca por su distribución a muchos países en Europa y varias comunidades autónomas dentro de la península.   

![euskal-lit_1](/Users/jenniferisasi/Documents/GitHub/jenniferisasi.github.io/assets/img/euskal_literatura/euskal-lit_1.png)



Y ¿quiénes son los autores más traducidos? No es sorpresa que destaquen Bernardo Atxaga,  Mariasun Landa Etxebeste, Kirmen Uribe o Piedad Ateka. 

![euskal-lit_3](/Users/jenniferisasi/Documents/GitHub/jenniferisasi.github.io/assets/img/euskal_literatura/euskal-lit_3.png)



Kepler también nos permite ver la evolución de nuestra red de traducciones a lo largo del tiempo. En este caso, y como es normal por la trayectoria de la literatura en euskera y la historia del País Vasco en general, el número de traducciones ha ido aumentando hacia finales de la década de los 90 y, sobre todo, a partir del año 2000. 

<iframe src="https://dr.jenniferisasi.com/assets/img/euskal_literatura/euskal_literatura.mov" width="100%" heigth="100%" > </iframe>



Una visualización geográfica nos permite observar la expansión de la literatura por el planeta. No obstante, ello invisibiliza la labor de autores y traductores en tanto que sus nombres no aparecen - se pueden mostrar pero no aportan nada más que una gran cantidad de letras que impiden su lectura. Para observar quién traduce a quién, y cuánto, una visualización de red es mucho más adecuada. Así, vemos que Bernardo Atxaga es el más traducido según nuestros datos y, curiosamente, se traduce al castellano a sí mismo (línea rosa junto a su nodo). 



![euskal-lit_4](/Users/jenniferisasi/Documents/GitHub/jenniferisasi.github.io/assets/img/euskal_literatura/euskal-lit_4.png)



Aquí se supone que aparezca el mapa interactivo en versión html de Kepler en algún momento, pues ahora mismo y como muestra su repositori en Github, algo está "roto": 

<iframe src="https://dr.jenniferisasi.com/assets/img/euskal_literatura/euskal-lit-map" width="100%" heigth="100%" > </iframe>