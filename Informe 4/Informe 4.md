Informe Bioinformática 4 - Ensamblaje de Genomas II
====

* Karina Campos

* Cristobal Madrid

Parte 1: La Tabla Hash
=====

## Pregunta 1

**¿En qué interval encontramos la consulta entera ACGAT?**

La consulta ACGAT la encontramos desde la base 6 hasta la 10 de la secuencia de referencia (ACGAACACGATCCTAACGCCA).

## Pregunta 2

**¿Cuál es el indice en que se almacena ACG, CGA y GAT?**

* La primera base de un 3-mer la convertimos en números (A,T,G,C) => (0,1,2,3)

* La segunda base igual (A,T,G,C) => (0,4,8,12)

* La tercera (A,T,G,C) => (0,16,32,48)

  * ACG => 0 + 12 + 32 = índice 44 de la tabla hash. 
  
  * CGA => 3 + 8 + 0 = índice 11 de la tabla hash.
  
  * GAT => 2 + 0 + 16 = índice 18 de la tabla hash. 


## Pregunta 3

**¿Una vez almacenadas, como podemos consultarlas? ¿Cuantos indices necesitamos checkear para la consulta ACGAT?**

Una vez almacenadas en la tabla hash podemos consultarlas por medio de los k-mers, en este caso serian 3 (ACG, CGA, GAT), necesitando 3 índices para checkear la consulta.

Parte 2: Arbol de sufijos, arreglo de sufijos y indice-FM
=====

## Pregunta 4

**Usa los sufijos siguientes para construir un arbol de sufijos para la referencia.**

Ahora vamos a almacenar otra secuencia en estructuras que se basan en sufijos.
Usando la referencia: ACTAGACTGGA$ (agregando el dollar para significar el fin de la secuencia), generamos todos los sufijos posibles (con indices).

                          ACTAGACTGGA$ 0
                          
                           CTAGACTGGA$ 1
                           
                            TAGACTGGA$ 2
                            
                             AGACTGGA$ 3
                             
                              GACTGGA$ 4
                              
                               ACTGGA$ 5
                               
                                CTGGA$ 6
                                
                                 TGGA$ 7
                                 
                                  GGA$ 8
                                  
                                   GA$ 9
                                   
                                    A$ 10
                                    
                                     $ 11

 

![arbol](https://raw.githubusercontent.com/CoderProgramerPro/bioinformatica/master/Informe%204/arbol.png)


## Pregunta 5

**Ordena los sufijos lexicograficamente guardando los indices dados arriba.**

![tabla](https://raw.githubusercontent.com/CoderProgramerPro/bioinformatica/master/Informe%204/tabla.PNG)

## Pregunta 6

**¿Cual es el arreglo de sufijos resultante?**

El arreglo de sufijo = {11, 10, 0, 5, 3, 1, 6, 9, 4, 8, 2, 7} 

## Pregunta 7

**¿Cual es la cantidad de A,T,G y C que tenemos en la secuencia original?**

Secuencia original: ATACCAG

* A: 3

* T: 1

* C: 2

* G: 1




## Pregunta 8

**¿Cual es la secuencia original?**

                       F                L

                      $0                G0 

                      A0                T0

                      A1                C0

                      A2                $0

                      C0                C1

                      C1                A0

                      G0                A1

                      T0                A2
                      
                        A2T0A0C1C0A1G0$0
                    Secuencia original: ATACCAG


## Pregunta 9

**Ahora que tenemos la secuencia original, representa la matriz Burrows-Wheeler que permitío generar el BWT arriba**


                      $0A2T0A0C1C0A1G0 

                      A0C1C0A1G0$0A2T0

                      A1G0$0A2T0A0C1C0

                      A2T0A0C1C0A1G0$0

                      C0A1G0$0A2T0A0C1

                      C1C0A1G0$0A2T0A0

                      G0$0A2T0A0C1C0A1

                      T0A0C1C0A1G0$0A2



