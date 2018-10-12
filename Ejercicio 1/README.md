# dev-pec1 - Módulo 2 Diseño y desarrollo

## EJERCICIO 1

**Construya y configure su propia blockain a partir del archivo génesis que ha definido. Cree una cuenta mediante el cliente Geth. Consiga su propio Ether mediante minería.** 

---

**1. Archivo génesis, creación de cuenta y puesta en marcha del nodo con Geth** 

Para empezar, he creado una directorio con el nombre redPrivada. Después he creado una nueva cuenta en Geth alojando los archivos en el directorio que he creado. Para crear la cuenta me ha pedido una contraseña y me ha lanzado mi address. (Comando: geth --datadir ~/redPrivada account new)

A continuación, he creado el archivo genesis.json y lo he alojado en el directorio redPrivada. El archivo .json (archivo génesis) define: los parámetros de la red, el coste del gas, la  dificultad y los nodos, entre otros.

![Configuración de nodo en cliente geth](https://github.com/anakb/dev-pec1/blob/master/1.png "Configuración de nodo en cliente geth")

---

**2. Lanzamiento de la red** 

geth --datadir ~/redPrivada/ --networkid 15

![Lanzamiento de la red](https://github.com/anakb/dev-pec1/blob/master/2.png "Lanzamiento de la red")

---

**3. Comprobaciones en la Geth JavaScript console**

Datos del bloque 0 

![Bloque 0](https://github.com/anakb/dev-pec1/blob/master/3.png "Bloque 0")

Representación hexadecimal de la codificación RLP 

![Representación hexadecimal](https://github.com/anakb/dev-pec1/blob/master/4.png "Representación hexadecimal")

Geth balance y estado del minado

![Balance y estado del minado](https://github.com/anakb/dev-pec1/blob/master/5.png "Balance y estado del minado")

---

**4. Minado**

Para iniciar el minado:

geth --mine --minerthreads1 --datadir ~/redPrivada --networkid 15

![Lanzamiento del minado](https://github.com/anakb/dev-pec1/blob/master/6.png "Lanzamiento del minado")

Creación del primer bloque:

![Primer bloque confirmado](https://github.com/anakb/dev-pec1/blob/master/7.png "Primer bloque confirmado")

----

**5. Comprobaciones del minado**

Minado activo 

![Minado activo](https://github.com/anakb/dev-pec1/blob/master/8.png "Minado activo")

**Estado del balance de la cuenta y datos del bloque 1**

![Datos del bloque 1](https://github.com/anakb/dev-pec1/blob/master/9.png "Datos del bloque 1")

---- 

## EJERCICIO 2