Informe Bioinformática 3 - Ensamblaje de Genomas
====

* Karina Campos

* Cristobal Madrid

Parte 1: El artículo Genoma
=====

## Pregunta 1

**¿Cuántos *Sequencing Projects y Analysis Projects* hay depositados en GOLD? ¿Cuál es la diferencia entre ambos?**

* Hay 356.082 **Sequencing Projects** y 283.853 **Analysis projects** a la fecha 15 de septiembre. 

La diferencia que existe es que Sequencing Projects es el organismo individual o la muestra que se desea secuenciar (puede ser más de una reacción de secuenciación y/o tecnologías de secuenciación) y Analysis Projects es el análisis de estos resultados (proyecto de secuenciación) de manera informática.

## Pregunta 2

**¿Cuál es el dominio más representado en la base de datos, *archea*, *bacteria*, *eukaryote*, o *virus*?**


A la fecha, el dominio más representado es el de bacteria, teniendo 175.897 a la fecha.

![1](https://raw.githubusercontent.com/CoderProgramerPro/bioinformatica/master/informe%203/Imagenes%20informe%203/1.png)

## Pregunta 3

**¿Cuáles son los *phyla* más representados entre los proyectos de genomas bacterianos en la base de datos?**

Los *phyla* más representados entre los proyectos de genomas bacterianos en la base de datos son proteobacterias (94,808) correspondiendo al 42,3%.

![2](https://raw.githubusercontent.com/CoderProgramerPro/bioinformatica/master/informe%203/Imagenes%20informe%203/2.png)


## Pregunta 4

**¿A qué tipo de proyectos pertenece la mayor cantidad de genomas bacterianos depositados en GOLD? 
(tipo de proyecto, se refiere al tópico de la investigación, por ejemplo, salud humana, ambiental, etc.)**


La mayor cantidad de genomas bacterianos depositados en GOLD pertenecen al tipo de proyecto médico.

![3](https://raw.githubusercontent.com/CoderProgramerPro/bioinformatica/master/informe%203/Imagenes%20informe%203/3.png)

Parte 2
====

## Pregunta 5

**¿Cuál es el artículo original del genoma? (en el cual se reporta la sequenciación y ensamble del genoma)**

El articulo original del proyecto genoma es: Lander, E., Linton, L., Birren, B. et al. Initial sequencing and analysis of the human genome. Nature 409, 860–921 (2001). https://doi.org/10.1038/35057062 se puede encontrar en el siguiente [link](https://www.nature.com/articles/35057062)

## Pregunta 6

**Explica, qué es el N50, L50, y NG50.**

* N50: define la calidad del ensamblaje en términos de contigüidad. El número de bases de todos los contigs más cortos que el N50 serán más cercanas al número de bases de todos los contigs más largos al N50, además el N50 corresponde a la longitud de la secuencia en pares de bases.


![4](https://raw.githubusercontent.com/CoderProgramerPro/bioinformatica/master/informe%203/Imagenes%20informe%203/4.png)


* L50: Dado un conjunto de contigs, cada uno con su propia longitud, el recuento L50 es el número más pequeño de contigs cuya suma de longitud constituye la mitad del tamaño del genoma. L50 representa el número de secuencias.

![5](https://raw.githubusercontent.com/CoderProgramerPro/bioinformatica/master/informe%203/Imagenes%20informe%203/5.png)


* NG50: La estadística NG50 es la misma que N50 excepto que es el 50% del tamaño del genoma conocido o estimado que debe tener la longitud NG50 o más. Puede realizar comparaciones significativas entre diferentes ensamblajes. La estadística NG50 no será mayor que la estadística N50.


## Pregunta 7

**¿Cuál es el propósito de calcular estas estadísticas?**

N50, L50 y NG50 son estadísticas de un conjunto de longitudes de contig. Se utilizan en el ensamblaje del genoma.

## Pregunta 8

**¿Cuántos *contigs* conforman el genoma del Bonobo? ¿Cuál es el N50 y L50 del genoma? (responde basado en los *contigs*)**


![6](https://raw.githubusercontent.com/CoderProgramerPro/bioinformatica/master/informe%203/Imagenes%20informe%203/6.png)


## Pregunta 9

**¿Cuál es el largo total y porcentaje de GC del genoma del Bonobo? ¿Qué quieren decir o qué indican éstos valores?**

* Mediana de la longitud total (Mb): 3169,27

* Mediana de GC%: 41,5096

El contenido GC se utiliza a veces para clasificar organismos en taxonomía, también en una secuencia genómica larga los genes se caracterizan por un elevado GC en comparación con el genoma completo. Un ADN con bajo contenido de GC es menos estable que el ADN con alto contenido de GC. 


## Pregunta 10

**¿Qué tipo de tecnología se usó para secuenciar el genoma del Bonobo? ¿Qué método (programa o algorítmo bioinformático) se usó para ensamblar el genoma?**

El genoma se ensambló utilizando el software [Celera Assembler](http://wgs-assembler.sourceforge.net/wiki/index.php?title=Main_Page) de código abierto, se secuenciaron 19 individuos de bonobos y chimpancés en la plataforma [Illumina GAIIx](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC3334598/) teniendo una cobertura genómica de aproximadamente el doble por individuo.

