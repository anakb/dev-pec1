# dev-pec1 - Módulo 2 Diseño y desarrollo

## EJERCICIO 2

**Información nodos en red Rinkeby** 
---

**1. Inicie la sincronización de la red Rinkeby en su dispositivo.**

Para sincronizar con la red: 

`geth --rinkeby --datadir=&HOME/ .rinkeby`

Identificación del self=enode:

![Sincronización red Rinkeby](https://github.com/anakb/dev-pec1/blob/master/Ejercicio%202/1.png "Sincronización red Rinkeby")
---

**2. Obtenga el address correspondiente al bloque génesis de la red Rinkeby mediante el cliente Geth y demuestre cómo lo ha obtenido.**

Con otra inicialización del cliente geth, he abierto la consola de de geth:

`geth --datadir=$HOME/.rinkeby attach ipc:$HOME/.rinkeby/geth.ipc console`

A continuación, he desplegado el comando `admin`que me ha dado como resultado la información de mi nodo (a la que acompaña el hash/address del nodo génesis `genesis: "0x6341fd3daf94b748c72ced5a5b26028f2474f5f00d824504e4fa37a75767e177`"), confirmo el hash del nodo génesis de la red de pruebas de Rinkeby en Etherscan y el address lanzado para mi nodo coinciden.

![Bloque génesis](https://github.com/anakb/dev-pec1/blob/master/Ejercicio%202/2.png "Bloque génesis")
---

**3. Obtenga sólo la cantidad de peers a los que está conectado**

Para obtener el número de peers a los que estás conectado, utilizas el siguiente comando en la consola de Geth: 

`net.peerCount`

En mi caso la consola me arrojó el número 3, tres nodos conectados.

![Cantidad de peers](https://github.com/anakb/dev-pec1/blob/master/Ejercicio%202/3.png "Cantidad de peers")
---

**4. Obtenga información acerca de los peers a los que está conectado e indique la altura máxima de bloque de los peers.**

Para saber información sobre los peers a los que se está conectado se utiliza `admin.peers` de la consola de Geth. 

Para el primero de los peers si nos fijamos en el "head" del nodo, vemos en Etherescan que ese bloque está a la altura de 3153654 bloques. 

![Peer 1](https://github.com/anakb/dev-pec1/blob/master/Ejercicio%202/3.png "Peer 1")

Para el segundo de los peers si nos fijamos en el "head" del nodo, vemos en Etherescan que ese bloque está a la altura de 3153649 bloques. 

![Peer 2](https://github.com/anakb/dev-pec1/blob/master/Ejercicio%202/4.png "Peer 2")


Para el tercer de los peers si nos fijamos en el "head" del nodo, vemos en Etherescan que ese bloque está a la altura de 3153647 bloques. 

![Peer 3](https://github.com/anakb/dev-pec1/blob/master/Ejercicio%202/5.png "Peer 3")

El primero de los peers está más actualizado. 