---
layout: post
title: "Distinción de géneros literarios a través de la visualización de redes de personajes: El caso de diez Episodios nacionales de Pérez Galdós"
description: "NoviembreHD por la Asociación Argentina de Humanidades Digitales"
date: 2020-11-05
location: "Twitter" 
---

En este póster presento los resultados de una lectura a media distancia que combina métodos de minería de datos y de redes para identificar el género en obras narrativas escritas en español. En este caso, se analizaron las diez novelas históricas de la tercera serie de los *Episodios Nacionales* de Benito Pérez Galdós (1843-1920).

En 2003, Alex Woloch afirmó que las estructuras narrativas están formadas por un sistema de personajes o "la disposición de espacios de personajes múltiples y diferenciados [, es decir,] configuraciones y manipulaciones diferenciadas de la figura humana" (Trad. propia, 14). Por su potencial como estudio cuantificable, varios humanistas digitales como Elson et al. (2010), Sack (2011), Agarval et al. (2012) o Moretti (2011-2016) han comparado el concepto de sistema de personajes de Woloch con la noción de red social, donde los nodos son los personajes y las conexiones representan interacciones entre ellos. En la presente metodología sigo dicha noción, y procedo en tres pasos para curar y analizar los datos: 1) Un algoritmo (escrito en R) detecta nombres en los textos y los sustituye por un nombre resuelto de un archivo de metadatos de 4.644 personajes; 2) Otro algoritmo en R extrae el número de co-ocurrencias de personajes por capítulo; y 3) Calculo la centralidad y modularidad de la suma de co-ocurrencias por novela en Gephi y visualizo cada sistema de personajes como una red.

Los resultados de esta lectura a media distancia muestran que existe una reciprocidad entre el posicionamiento de los personajes históricos y de ficción en los sistemas-personajes y la tipología de las novelas que había sido previamente identificada por la lectura atenta de galdosistas como Urey (1989) o García Castañeda (2012). De hecho, hay un mayor énfasis en lo que Galdós llamó "historia integral" en aquellas novelas que relatan la trayectoria vital del personaje principal como un *bildungsroman* en varios tomos. En general, esta metodología busca una mejor comprensión de las posibilidades que ofrecen las herramientas digitales para el estudio de los operadores culturales textuales en español.

<img src="/assets/posters/Isasi_NoviembreHD-AAHD.jpeg" alt="Distinción de géneros literarios a través de la visualización de redes de personajes: El caso de diez Episodios nacionales de Pérez Galdós"
	title="Distinción de géneros literarios a través de la visualización de redes de personajes: El caso de diez Episodios nacionales de Pérez Galdós" width="100%" height="100%" />

You can find this poster in English in "[Distinction of Literary Genres through the Visualization of Character Networks: The Case of ten *National Episodes* by Pérez Galdós](https://jenniferisasi.github.io/blog/2018/poster-dhcs/)" 

