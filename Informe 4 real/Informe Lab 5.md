# Informe Bioinformática 5 - Ensamblaje de Genomas II
====

* Karina Campos

* Cristobal Madrid

Parte 1: 
=====

## Pregunta 1

**¿El archivo que está descargando está en el formato FASTQ o FASTA? ¿Cuál es la diferencia principal entre los dos?**


## Pregunta 2

**¿Los índices de calidad Phred están codificados en Phred+33 o Phred+64?**

Los índices de calidad están codificados en Phred+33


## Pregunta 3

**Copia los primeros 10 símbolos de esta codificación y convierten estos símbolos en índices de calidad Phred (usando el guía visual arriba). Separa cada índice con un espacio.**
Los primeros 10 símbolos son :

<B@BBBB@@B@>

Según la tabla guía, para Phred+33

![tablaguia](https://bioinformaticsworkbook.org/introduction/assets/qualityscore.png)

Estos son los indices de calidad Phred que corresponden a los primeros 10 símbolos de la codificación

33-31-33-33-33-33-31-31-33-31

## Pregunta 4

**¿Cuántos ORFs o genes encontró ORFfinder?**

![ORF](https://raw.githubusercontent.com/CoderProgramerPro/bioinformatica/master/Informe%204%20real/ORF.PNG)

## Pregunta 5

**¿En qué hebra están codificados?**

![orfstrand](https://raw.githubusercontent.com/CoderProgramerPro/bioinformatica/master/Informe%204%20real/ORFstrand.PNG)

## Pregunta 6

**¿De qué largo son los ORFs predichos?**


## Pregunta 7

**¿Algunos de ellos se sobreponen (fíjate en la posición de inicio [start] y término [stop])?**


## Pregunta 8

**¿Qué tipo de programa es ORFfinder, Ab initio o por homología?**

Es por Homología, ya que el programa busca en bases de datos curadas de proteinas o mRNas o transcriptomas, en este caso, el programa buscó por defecto en la base de datos curada **UniProtKB/Swiss-Prot(swissprot)**.

## Pregunta 9

**¿A qué organismo pertenece la secuencia en cuestión?**


## Pregunta 10

**¿Qué gen(s) está(n) codificados en la secuencia?**


## Pregunta 11

**Tomando en cuenta la evidencia que acumulaste usando ORFfinder y BLAST. ¿Cuál o cuáles ORFs predichos por ORFfinder dirías tú que son o es el correcto(s)?**

## Pregunta 12

**Coloca la o las secuencias de las proteínas que encontraste.(En formato fasta)**


## Pregunta 13

**¿Cual es la función de esa o esas proteínas?**


## Pregunta 14

** Según el paper original de la secuenciación del genoma del organismo con el que has trabajado (Fleischmann et al. 1995). ¿Cual es la metodología de secuenciación del genoma?, ¿Que ensamblador utilizaron? y ¿Cuantas regiones codificantes predijeron?**

