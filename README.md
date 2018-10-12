# dev-pec1 - Módulo 2 Diseño y desarrollo

## EJERCICIO 1

### Construya y configure su propia blockain a partir del archivo génesis que ha definido. Cree una cuenta mediante el cliente Geth. Consiga su propio Ether mediante minería. 

**1.** Archivo génesis y lanzamiento en Geth

Para empezar, he creado una directorio con el nombre redPrivada. Después he creado una nueva cuenta en Geth alojando los archivos en el directorio que he creado. Para crear la cuenta me ha pedido una contraseña y me ha lanzado mi address. (Comando: geth --datadir ~/redPrivada account new)

A continuación he creado el archivo genesis.json y lo he alojado en el directorio redPrivada. El archivo json (archivo génesis) define los parámetros de la red, el coste del gas, la  dificultad y los nodos, entre otros parámetros de la nueva red. 

![alt text](https://github.com/anakb/dev-pec1/blob/master/1.png "Configuración de nodo en cliente geth")
