 Informe Bioinformática 8 - Comandos por Terminal.
====

* Karina Campos

* Cristobal Madrid


----

### Pregunta 1

**Defina la función de cada uno de los comandos more, head y tail.**


* more: Este comando mostrara los contenidos del fichero en la pantalla y le pedirá al usuario una pulsación de teclado para hacer un scroll en el fichero (`ejemplo: more<fichero>`). Mostrar línea por línea el archivo.


* head: mostrará las primeras líneas de un archivo, puedes indicarle el número de líneas comenzando desde arriba que quieres mostrar (`ejemplo: head -n 5 test.txt`).


* tail: mostrará las últimas líneas de un fichero, utilizando el comando tail y el número de líneas que queremos mostrar, este comando empezará desde la última línea hacía arriba (ejemplo: `tail -5 test.txt`).


### Pregunta 2

**Haga captura de pantalla de 1 ejemplo de cada item de línea de comando 1.- 2.- 3.- 4.-**

* 1: `head -20 mart_export.txt`

![1](https://raw.githubusercontent.com/CoderProgramerPro/bioinformatica/master/1.jpg)

* 2: `uniq mart_export.txt | wc -1`


![2](https://raw.githubusercontent.com/CoderProgramerPro/bioinformatica/master/2.jpg)

* 3: `grep -v " " mart_export.txt`

![3](https://raw.githubusercontent.com/CoderProgramerPro/bioinformatica/master/3.jpg)

* 4: `awk '$4~/NOTCH/ {print "chr"$1+1"\t"$4}' mart_export.txt`

![4](https://raw.githubusercontent.com/CoderProgramerPro/bioinformatica/master/4.jpg)



### Pregunta 3

**Escriba la línea de comando que genere un archivo ordenado alfabéticamente (considerando los números) y que no contenga líneas duplicadas, ¿Cuál sería la línea de comando para saber cuánto pesa el archivo nuevo (en formato legible para humanos)?**

Para generar un archivo ordenado alfabética o lexicográficamente es `sort mart_export.txt`, sin líneas duplicadas es `uniq mart_export.txt`.

`sort mart_export.txt`

![6](https://raw.githubusercontent.com/CoderProgramerPro/bioinformatica/ultimo%20informe/6.png)

`uniq mart_export.txt`

![7](https://raw.githubusercontent.com/CoderProgramerPro/bioinformatica/ultimo%20informe/7.png)


La línea de comando para saber cuanto pesa el archivo nuevo en formato legibles es: `du -sh mart_export.txt`

![5](https://raw.githubusercontent.com/CoderProgramerPro/bioinformatica/ultimo%20informe/5.png)

