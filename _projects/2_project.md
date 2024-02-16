---
layout: page
title: El elenco de Pedro Almodóvar
description: Acercamiento a la red de actores y actrices de las películas de Pedro Almodovar
img: /assets/img/post_almodovar/almodovar_logo.png
importance: 2
category: fun
giscus_comments: false
---

Pedro Almodóvar ha vuelto a la gran pantalla este año con *Dolor y gloria* y todo parece indicar que está siendo un éxito. Yo no la he visto todavía pero, he de confesar, al ver el trailer pensé ¡otra vez los mismos! Banderas, Pé, Cecilia Roth, Asier Etxeandia… algo que se ve muy bien en el propio cartel de la película: 

<img src="/assets/img/post_almodovar/dolor-y-gloria.jpeg" alt="Cartel de la película Dolor y gloria de Almodóvar"
	title="Cartel de la película 'Dolor y gloria' de Almodóvar"  width="50%" height="50%" />

Me picó la curiosidad por saber si Penélope Cruz estaría en el centro de la red de actrices y actores que Almodóvar suele contratar para sus películas. 

¡Manos a la  obra!

## Extracción de datos de reparto 

Para este experimento primero tomé los datos del "full cast" (reparto completo) de cada una de [las películas de las que Almodóvar ha sido director](https://www.imdb.com/name/nm0000264/?ref_=nv_sr_1?ref_=nv_sr_1#director) de la Base de Datos de Películas de Internet (IMDb). Para ello utilicé el "copia y pega" de toda la vida, pues no se trata de muchas películas. Extraje los datos de 25 películas (con algún corto incluido) pues faltan los datos de las primeras creaciones del director. Para algo más amplio conviene extraer los datos mediante un algoritmo de *webscrapping*. Puesto que IMDb tiene un *record* para cada persona en su base, no fue necesario realizar una limpieza de datos normalizando los nombres del reparto ni de las películas (cuyos títulos sí traduje) pues el sistema no da base a variaciones ortográficas o problemas similares que ocurren en otros sistemas.

Primero, creé una tabla (luego CSV) con las columnas año, película, reparto y personaje (esta variable no la he utilizado), lo que me permitió, a su vez, crear un listado de características de cada persona con su género.

A partir del listado del elenco de cada película, generé un archivo de co-aparición en cada película con un *loop* en R (reciclado de mi tesis). Lo que este código hace es crear un *data frame* estableciendo parejas de un listado. Por ejemplo, de este listado de cuatro personas en la última película

| Dolor y gloria     |
| ------------------ |
| Antonio Banderas   |
| Asier Etxeandia    |
| Leonardo Sbaraglia |
| Nora Navas         |

se genera un archivo de dos columnas que, para los propósitos de la red ,se llaman "source" (emisor) y "target" (receptor): 

| Source             | Target             |
| ------------------ | ------------------ |
| Antonio Banderas   | Asier Etxeandia    |
| Antonio Banderas   | Leonardo Sbaraglia |
| Antonio Banderas   | Nora Navas         |
| Asier Etxeandia    | Leonardo Sbaraglia |
| Asier Etxeandia    | Nora Navas         |
| Leonardo Sbaraglia | Nora Navas         |

Este listado indica la co-aparición de dos actores o actrices en una misma película, sin tener en cuenta si son protagonistas, secundarios, terciarios, la cantidad de palabras que dicen en la película, el tiempo que pasan en pantalla, etc. 



## Análisis de red en Gephi 

El siguiente paso para realizar un análisis de la red de reparto de Almodóvar es cargar los datos de nodos y aristas en Gephi. La red completa del elenco de Almodóvar tiene, así, en total, 529 personas o nodos con 13214 conexiones o aristas, es decir, que aparecen en la misma película entre todos ellos 13214 veces. 

En término del género del reparto (datos no contrastados, por lo que puede haber algún error), la red está dividida de forma equilibrada con un 51.42% de hombres y 48.58% de mujeres. Sin embargo, si tenemos en cuenta el grado de conectividad en orden descendiente, hay más actrices que actores, es decir, que Almodóvar repite más con su reparto femenino que masculino. La intuición y la memoria me dicen que esto ya lo sabíamos. 

Por supuesto, Antonio Banderas está en el top 10 de más conectados con un total de 215 conexiones (o *degree* en el análisis de redes), con Penélope Cruz algo más alejada en la lista con 160 conexiones, lo cual la coloca todavía en un puesto prominente. Cecilia Roth es la número 2 en el listado ordenado por grado, con 275 conexiones. 

El análisis también nos indica que se generan 11 comunidades. Esto quiere decir, explicado de forma sencilla, que de la forma en que se repite el reparto en el total de 25 películas hay 11 grupos que podemos distinguir puesto que aparecen juntos en mayor medida o más veces. Es un número más alto de lo que me esperaba, la verdad, teniendo en cuenta que Almodóvar suele repitir a sus favoritas (por decirlo de alguna manera). Ahora bien, el número de personas por comunidad sí varía significativamente entre comunidades. 



<img src="/assets/img/post_almodovar/almodovar_mod.png" alt="Gráfico de distribución del tamaño de cada comunidad según el altoritmo de modularidad de Gephi"
	title="Distribución del tamaño de cada comunidad de Almodóvar" width="100%" height="100%" />

Gephi genera estos datos de forma rápida y nos permite extraerlos en formato de valores separados por comas para poder realizar futuros análisis o simplemente estudiar los datos de otra forma. Por ejemplo, podemos generar un gráfico con la distribución del grado de centralidad en otro programa a partir de dichos datos. 

<img src="/assets/img/post_almodovar/almodovar_degree_graph.png" alt="Gráfico de distribución del grado de centralidad por reparto"
	title="Distribución del grado de centralidad de todo el reparto en la red de Almodóvar" width="100%" height="100%" />

Ahora bien, ¿quién o quiénes quedan en el centro de esta red de reparto? ¿Cómo quedan distribuidos el resto de actores y actrices? Hay alguna incidencia en la distribución de la red según el género? Veamos. 



## Visualización de red en Gephi

Para generar la visualización de la red almodovariana, he utilizado el algoritmo ForceAtlas2 con una escala de 250 puntos, con la gravedad "activada" con un grado de 0.8 (esto hace que todos los nodos de la red queden más cercanas al centro, lo cual es muy útil si tienes nodos no conectados a la red mayor). Además, he estudiado diferentes variables según el grado de conectividad y el posicionamiento del reparto en la red, su género, la formación de comunidades, y la situación del reparto por películas. 



### Grado de distribución y género

Pues bien, estudiando los parámetros de grado de centralidad en los nodos y un mayor peso en las aristas, vemos que el actor céntrico, más conectado, es el hermano menor y productor habitual en las películas de Pedro: Agustín Almodóvar. Este cuenta con un grado de conexión de 496 puntos, y es que resulta que aparece en las 22 de las 25 películas de este conjunto de datos. 

Cercanas al centro por su aparición continuada en las películas de Almodóvar también están Cecilia Roth (275 conexiones, 8 películas), Chus Lampreave (254 conexiones, 10 películas), Carlos García Cambero (246 conexiones, 7 películas), Esther García, Marisa Paredes, Antonio Banderas y Fernando Iglesias. 

<img src="/assets/img/post_almodovar/almodovar_degree.png" alt="Visualización de la red del reparto de Almodóvar con medidas de centralidad y peso de las aristas"
	title="Red del reparto de Almodóvar con medidas de centralidad y peso de las aristas" width="100%" height="100%" />

Penélope Cruz queda bastante alejada del centro, digamos en un segundo nivel aunque aparece en 8 filmes pero con un menor número de actores y actrices. Su grado de conectividad está cercano al del propio Pedro Almodóvar, la famosa Carmen Machi, Julieta Serrano y Lola Dueñas.  

Ya hemos dicho que el reparto de Almodóvar presenta una división bastante equilibrada en cuanto al número de mujeres y hombres con los que cuenta en sus películas, y que las mujeres ocupan un mayor grado de conectividad en la red. Podemos visualizar los datos para comprobar que, efectivamente, hay una distribución igual de ambos géneros, pues no pesa uno más que otro en el centro ni la periferia de la red. 

<img src="/assets/img/post_almodovar/almodovar_degree_gender.png" alt="Visualización de la red del reparto de Almodóvar con medidas de centralidad y peso de las aristas por género"
	title="Red del reparto de Almodóvar con medidas de centralidad y peso de las aristas por género" width="100%" height="100%" />

### Las comunidades del reparto 

El algoritmo de modularidad de Gephi ha determinado que del total de 25 películas, el reparto queda distribuido en 11 comunidades bastante bien definidas. Ahora bien, casi el 60% del total del reparto, esto es, de 529 actores y actrices del elenco de Almodóvar, quedan agrupados en 3 comunidades. Curiosamente, la comunidad con el mayor número de personas más conectadas entre ellas queda en la periferia de la red (arriba a la derecha, en color ocre), aunque su elenco tiene un alto grado de conectividad y quedan, por tanto, al centro. Es en esta comunidad en la que Cecilia Roth y Antonio Banderas quedan unidos. 

<img src="/assets/img/post_almodovar/almodovar_degree_mod.png" alt="Visualización de la red del reparto de Almodóvar con medidas de centralidad y división por comunidades"
	title="Red del reparto de Almodóvar con medidas de centralidad y su división por comunidades" width="100%" height="100%" />

En la segunda comunidad con un mayor porcentaje del reparto es donde aparecen otras de las actrices favoritas del director: Carmen Maura y Rossy de Palma, junto con Agustín Almodóvar y Chus Lampreave. Esta comunidad queda bastante centrada en la red (centro y abajo derecha, en rosa). Penélope Cruz tiene su propio grupo de co-apariciones según este algoritmo, con Esther García, Fernando Iglesias, Carmen Machi y Susi Sánchez, entre otros. 

Como veremos a continuación, la distribución del reparto por comunidades queda en mayor medida relacionado con el reparto de cada película. 



### Visualización de la red por película 

Al haber añadido en mi base de datos la información de cada película en las aristas o conexiones, también he podido visualizar la misma red pero por película. Esto añade otro tipo de información con la que no contábamos en las visualizaciones previas. Primero, por ejemplo, podemos saber que la película *Hable con ella* (2002) cuenta con el 26.77% del elenco puesto que es la que cuenta con un mayor número de actores y actrices (85) en el primer listado extraido de IMDb. La particularidad del reparto de esta película es que no se repite demasiado en otras películas, de ahí que en el análisis de modularidad éste forme su propia comunidad (izquierda, en azul oscuro). 

Vemos en las aristas o líneas que salen del nodo de Agustín Almodóvar que, por supuesto, aparece en muchas de las películas de la red, al igual que Antonio Banderas, Cecilia Roth, Chus Lampreave y Penélope Cruz, de nuevo. Como era de esperar, la localización en el centro de la red de los actores y actrices indica su participación en más películas y, al contrario, en la periferia y al borde tenemos a los que repiten menos. 

<img src="/assets/img/post_almodovar/almodovar_degree_film.png" alt="Visualización de la red del reparto de Almodóvar con medidas de centralidad y división por película"
	title="Red del reparto de Almodóvar con medidas de centralidad y su división por película" width="100%" height="100%" />

### La red de Almodóvar a través del tiempo 

Finalmente, otra cosa que podemos estudiar gracias a los datos obtenidos de la base de datos de internet y añadidos en mi tabla, es la evolución de la red de Almodóvar por año de estreno de cada película. Aprovecho los mismos colores o distribución de la red con cada película (imagen anterior).

Para no generar una imagen estática e individual con cada año, he creado un pequeño video que muestra únicamente las conexiones o las aristas de la película en tiempo cronológico. Sin ser ninguna sorpresa, se ve claramente que Almodóvar no contó con el elenco que será posteriormente central en su carrera (y la red) para su primer filme, de 1976. Lógico. 

En la segunda película (1980) , no obstante, el número del reparto se amplía y, además, incluye ya a la que serán dos de sus favoritas hasta sus películas más recientes, Cecilia Roth y Carmen Maura.



<img src="/assets/img/post_almodovar/red_almodovar.gif" alt="Gif de la red de Almodóvar"
	title="Red del reparto de Almodóvar por película" width="100%" height="100%" />



## Conclusión 

Penélope Cruz no es el centro de *este* universo de Almodóvar. Y, sin embargo, yo no puedo separar a Penélope Cruz y Almodóvar en mi mente (acordaos de ese famoso momento en que Pe grita: Pedrooo!). He aprendido, además, que el hermano pequeño de Pedro aparece en casi todas sus películas y, la verdad, no lo sabía. 

Sea como fuere, y como se puede comprobar, en un pequeño momento de inspiración y curiosidad he podido generar una red y un estudio bastante completo (dentro de mis posibilidades) del reparto de Pedro Almodóvar gracias a la extración y visualización de datos. 

Ahora me toca ver *Dolor y gloria* para cerrar, como espectadora, el ciclo de la trilogía de deseo y ficción que ésta forma con *La ley del deseo* (1987) y *La mala educación* (2004). 
