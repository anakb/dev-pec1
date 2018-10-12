# dev-pec1 - Módulo 2 Diseño y desarrollo

## EJERCICIO 1

### Construya y configure su propia blockain a partir del archivo génesis que ha definido. Cree una cuenta mediante el cliente Geth. Consiga su propio Ether mediante minería. 

---

**1. "Archivo génesis, creación de cuenta y puesta en marcha del nodo con Geth"** 

Para empezar, he creado una directorio con el nombre redPrivada. Después he creado una nueva cuenta en Geth alojando los archivos en el directorio que he creado. Para crear la cuenta me ha pedido una contraseña y me ha lanzado mi address. (Comando: geth --datadir ~/redPrivada account new)

A continuación, he creado el archivo genesis.json y lo he alojado en el directorio redPrivada. El archivo json (archivo génesis) define los parámetros de la red, el coste del gas, la  dificultad y los nodos, entre otros parámetros de la nueva red. 

![Configuración de nodo en cliente geth](https://github.com/anakb/dev-pec1/blob/master/1.png "Configuración de nodo en cliente geth")

---

**2. Lanzamiento de la red** 

geth --datadir ~/redPrivada/ --networkid 15

![Lanzamiento de la red](https://github.com/anakb/dev-pec1/blob/master/2.png "Lanzamiento de la red")

---

**2.** "Comprobaciones en la **Geth JavaScript console**"

Datos del bloque 0 y representación hexadecimal de la codificación RLP 

![Lanzamiento de la red](https://github.com/anakb/dev-pec1/blob/master/3.png "Lanzamiento de la red")


![Lanzamiento de la red](https://github.com/anakb/dev-pec1/blob/master/4.png "Lanzamiento de la red")

