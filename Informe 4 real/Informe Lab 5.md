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

> B@BBBB@@B@

Según la tabla guía, para Phred+33

![tablaguia](https://bioinformaticsworkbook.org/introduction/assets/qualityscore.png)

Estos son los indices de calidad Phred que corresponden a los primeros 10 símbolos de la codificación

> 33-31-33-33-33-33-31-31-33-31

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

Pertenece a Haemophilus influenzae.

## Pregunta 10

**¿Qué gen(s) está(n) codificados en la secuencia?**

En la secuencia según BLASTx, el gen que esta codificado en el ORF1 corresponde al de una proteína accesoria de Formato Deshidrogenasa de Haemophilus influenzae.

![Blastx](https://raw.githubusercontent.com/CoderProgramerPro/bioinformatica/master/Informe%204%20real/blastx.PNG)


Utilizando SmartBLAST en la secuencia de ORF3 SmartBLAST determinó que este ORF es similar al de una proteína hipotética de Pseudoalteromonas agarivorans con un 66.7% de identidad. 

![ORF3](https://raw.githubusercontent.com/CoderProgramerPro/bioinformatica/master/Informe%204%20real/ORF3.PNG)

Utilizando SmartBLAST en el la secuencia de ORF4 podemos encontrar que la proteína codificada es N-acetil transferasa, esta proteína se encuentra relativamente conservada en distintos organismos siendo más cercana a N-acetil transferasa de Shewanella oneidensis.

![ORF4](https://raw.githubusercontent.com/CoderProgramerPro/bioinformatica/master/Informe%204%20real/ORF4.PNG)


Utilizando SmartBLAST en el la secuencia de ORF5 podemos encontrar que es la subunidad psi de la DNA polimerasa III de Haemophilus influenzae.

![orf5](https://raw.githubusercontent.com/CoderProgramerPro/bioinformatica/master/Informe%204%20real/ORF5.PNG)

Utilizando SmartBLAST en el la secuencia de ORF6 podemos encontrar que tiene un bajo porcentaje de identidad con otras proteínas y no es coherente con proteínas del organismo que se esta trabajando Haemophilus influenzae. Esto se puede deber a lo corta que es la secuencia de aminoácidos. Sin embargo BLAST determinó que es más cercana a una proteína hipotetica de Actinobacteria bacterium

![orf6](https://raw.githubusercontent.com/CoderProgramerPro/bioinformatica/master/Informe%204%20real/ORF6.PNG)

Utilizando SmartBLAST en el la secuencia de ORF7 podemos encontrar que es similar a la secuencia de helicasa de Candidatus Parcubacteria bacterium y a Helicasa de Anaerolineae bacterium con E-values de 0.005 y 0.006 que son relativamente altos comparado a los E-value que se encontraron en los alineamientos de ORF1, lo cual es explicado por el corto tamaño de la secuencia.

![orf7](https://raw.githubusercontent.com/CoderProgramerPro/bioinformatica/master/Informe%204%20real/ORF7.PNG)

Para ORF2 SmartBLAST no fue capaz de encontrar coincidencias

## Pregunta 11

**Tomando en cuenta la evidencia que acumulaste usando ORFfinder y BLAST. ¿Cuál o cuáles ORFs predichos por ORFfinder dirías tú que son o es el correcto(s)?**

Los ORFs que pueden ser correctos son aquellos que tienen una secuencia relativamente larga, alto porcentaje de identidad con las secuencias alineadas y tienen una covertura cercana al 100%. Dentro de estos criterios ORF1 es el mejor candidato de ORF correcto, este codifica para una proteína accesoria de formato deshidrogenasa.

## Pregunta 12

**Coloca la o las secuencias de las proteínas que encontraste.(En formato fasta)**
La secuencia de la proteína encontrada en ORF 1 en formato FASTA es la siguiente

>WP_118871546.1 formate dehydrogenase accessory protein FdhE [Haemophilus influenzae]
MSIKILSESEIKQVANSYQAPAVLFANPKNLYQRRAKRLRDLAQNHPLSDYLLFAADIVESQLSTLEKNP
LPPQQLEQLNAIEPLNAKTFKRNSIWREYLTEILDEIKPKANEQIAATIEFLEKASSAELEEMANKLLAQ
EFNLVSSDKAVFIWAALSLYWLQAAQQIPHNSQVENAENLHHCPVCGSLPVASMVQIGTSQGLRYLHCNL
CESEWNLVRAQCTNCNSHDKLEMWSLNEELALVRAETCGSCESYLKMMFQEKDPYVEPVADDLASIFLDI
EMEEKGFARSGLNPFVFPAEEA

## Pregunta 13

**¿Cual es la función de esa o esas proteínas?**


## Pregunta 14

**Según el paper original de la secuenciación del genoma del organismo con el que has trabajado (Fleischmann et al. 1995). ¿Cual es la metodología de secuenciación del genoma?, ¿Que ensamblador utilizaron? y ¿Cuantas regiones codificantes predijeron?**


