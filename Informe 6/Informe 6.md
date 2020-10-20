Informe Bioinformática 6 - Ensamblaje de Genomas II
====

* Karina Campos

* Cristobal Madrid

Parte 1: 
=====

## Pregunta 1

**¿Qué ofrece o para qué sirve el portal Phylogeny.fr?**

Phylogeny.fr es un programa en donde podemos realizar nuestro propio flujo de trabajo, utilizando distintas herramientas, además proporciona una plataforma de alto rendimiento el cual tiene diversos programas que son sumamente relevantes para un análisis filogenético completo, ayudando a los biólogos que no son experimentados en filogenia a analizar sus datos.

## Pregunta 2

**Nombra y explica brevemente los 3 modos en los que se puede ejecutar el pipeline de Phylogeny.fr.**

* El "Modo de un clic": permite de forma predeterminada, ejecutar y conectar programas reconocidos por su precisión y velocidad (MUSCLE para la alineación múltiple y PhyML para la filogenia), reconstruyendo un árbol filogenético a partir de un conjunto de secuencias. El software toma sus propias decisiones, de forma de optimizar sus datos. 

* En el "Modo avanzado”: los usuarios pueden elegir los pasos a realizar y las opciones de cada programa, aun cuando Phylogeny.fr propone la sucesión de los mismos programas, a partir de una alineación de secuencia múltiple se realiza la reconstrucción filogenética, dibujando el árbol. Permite establecer manualmente parámetros para distintos pasos.

* El "modo A la carte": permite utilizar diferentes programas de alineación y filogenia (ej: MUSCLE, ClustalW, T-Coffee, PhyML, BioNJ, TNT), creando un flujo de trabajo perzonalizado de filogenia, lo cual puede ser beneficisoso dependiendo del trabajo que se requiere realizar. 

## Pregunta 3

**Menciona qué tipos de análsis se pueden realizar en el portal de acuerdo a la documentación. (Online Programs)**

* BLAST: Blast (Basic Local Alignment Tool)

* ALINEACIÓN MULTIPLE: MUSCLE, T-Coffee, ClustalW, ProbCons.

* FILOGENIA: PhyML, TNT, BioNJ, MrBayes.

* VISORES DE ÁRBOL: TreeDyn, Drawgram, Drawtree, ATV.

* UTILIDADES: Gblocks, Jalview (hand editing), Readseq, Format converter


## Pregunta 4

**Incluye en tu informe una captura de pantalla de las dos filogenias que inferiste. Recuerden que tu nombre completo debe aparecer en la imagen de cada filogenia (Name of the analysis).**

![Campos Madrid 1](https://raw.githubusercontent.com/CoderProgramerPro/bioinformatica/master/Informe%206/Campos%20Madrid%201.png)
**Figura 1.** Árbol de filogenia generado con los siguientes parámetros: ProbCons, GBlocks, MrBayes, y TreeDyn.

![Campos Madrid 2](https://raw.githubusercontent.com/CoderProgramerPro/bioinformatica/master/Informe%206/Campos%20Madrid%202.png)
**Figura 2.** Árbol de filogenia generado con los siguientes parámetros: ClustalW, Remove positions with gaps, TNT, y TreeDyn.

## Pregunta 5

**¿A qué se refiere el paso de Alignment curation y para qué sirve?**

Al reconstruir un árbol filogenético a partir de un conjunto de secuencias. los usuarios pueden usar o no el programa Gblocks, el cual permite eliminar posiciones mal alineadas y regiones divergentes, Gblocks tiene diferentes valores predeterminados que se encuentran bien definidos (ej: eliminar todas las posiciones con huecos).

## Pregunta 6

**¿Cuál es la diferencia entre BioNJ y Neighbor?**

Ambos se utilizan para la reconstrucción filogenética.

| BioNJ | NJ |
| :--- | ---: |
| Velocidad alta | Velocidad alta |
| Funciona incluso cuando el número de taxones es alto (> 1000 taxones) | Funciona mejor con un número bajo de taxones |
| Necesita más memoria para almacenar varias matrices | Sólo utiliza una matriz |

    
## Pregunta 7

**Incluye en tu informe una captura de pantalla de las dos filogenias que inferiste (sin Alignment curation). Recuerda que sus apellidos deben aparecer en la imagen de cada filogenia (Name of the analysis).**

![Campos Madrid 3](https://raw.githubusercontent.com/CoderProgramerPro/bioinformatica/master/Informe%206/Campos%20Madrid%203.png)
**Figura 3.** Árbol de filogenia generado con los siguientes parámetros: ProbCons, MrBayes, y TreeDyn.

![Campos Madrid 4](https://raw.githubusercontent.com/CoderProgramerPro/bioinformatica/master/Informe%206/Campos%20Madrid%204.png)
**Figura 4.** Árbol de filogenia generado con los siguientes parámetros: ClustalW, TNT, y TreeDyn.

## Pregunta 8

**¿Cuál es el efecto de no hacer la curación del alineamiento en las filogenias?**

En comparación con los árboles filogenéticos con alineamiento curado se observa que la confianza en los nodos cambia, aumentando en el que no tiene el alineamiento curado.
Se destaca además que en el alineamiento curado los nodos internos se encuentran mucho más pequeños y centrados que en las secuencias que no tienen alineamiento curado

Es notable la diferencia entre la Fig. 2 y la Fig. 4, SRY_Homo_sapiens se encuentra más alejado de SRY_Cebus_capucinus, poniendo en su lugar SRY_Rhin_t en la Fig. 4. También es aún mas notable la diferencia entre ambos árboles mientras se aumenta la distancia evolutiva de los genes que se muestran.


## Pregunta 9

**Describe las diferencias entre las filogenias que has estimado (4 en total): cantidad de grupos monofiléticos, relaciones que potencialmente cambiaron, etc.**

Muchas de las diferencias en las filogenias se generan debido a que se utilizan programas distintos para crearlas. Por ejemplo cuando eliminamos la curación del alineamiento algunas especies del árbol generado con curación que están en la misma escala evolutiva con el mismo ancestro en común, se encuentran separadas. 

Cabe destacar que cambia también la cantidad de grupos monofiléticos, siendo alterado cuando se elimina la curación o cuando utilizamos un programa de alineamiento múltiple distinto, como lo realizamos en este trabajo, generando filogenias con ClustalW y ProbCons.

También las distancias entre las filogenias cambian drásticamente utilizando configuraciones distintas y que para ser 100% reproducibles deben ser realizadas de la misma manera con los mismos parámetros.
