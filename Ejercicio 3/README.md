# dev-pec1 - Módulo 2 Diseño y desarrollo

## EJERCICIO 3

**Información compilador** 
---
**Contrato**

```
pragma solidity ^0.4.21;

contract SimpleCounter {
	int counter;
	
	constructor() public {
		counter = 0;
	}
	
	function getCounter() view public returns(int) {
		return counter;
	}
	
	function increment() public {
		counter += 1;
	}
}
```

---

**Códigos de operación del contrato inteligente** 

PUSH1 0x80 PUSH1 0x40 MSTORE CALLVALUE DUP1 ISZERO PUSH2 0x10 JUMPI PUSH1 0x0 DUP1 REVERT JUMPDEST POP PUSH1 0x0 DUP1 DUP2 SWAP1 SSTORE POP PUSH1 0xD1 DUP1 PUSH2 0x26 PUSH1 0x0 CODECOPY PUSH1 0x0 RETURN STOP PUSH1 0x80 PUSH1 0x40 MSTORE PUSH1 0x4 CALLDATASIZE LT PUSH1 0x49 JUMPI PUSH1 0x0 CALLDATALOAD PUSH29 0x100000000000000000000000000000000000000000000000000000000 SWAP1 DIV PUSH4 0xFFFFFFFF AND DUP1 PUSH4 0x8ADA066E EQ PUSH1 0x4E JUMPI DUP1 PUSH4 0xD09DE08A EQ PUSH1 0x76 JUMPI JUMPDEST PUSH1 0x0 DUP1 REVERT JUMPDEST CALLVALUE DUP1 ISZERO PUSH1 0x59 JUMPI PUSH1 0x0 DUP1 REVERT JUMPDEST POP PUSH1 0x60 PUSH1 0x8A JUMP JUMPDEST PUSH1 0x40 MLOAD DUP1 DUP3 DUP2 MSTORE PUSH1 0x20 ADD SWAP2 POP POP PUSH1 0x40 MLOAD DUP1 SWAP2 SUB SWAP1 RETURN JUMPDEST CALLVALUE DUP1 ISZERO PUSH1 0x81 JUMPI PUSH1 0x0 DUP1 REVERT JUMPDEST POP PUSH1 0x88 PUSH1 0x93 JUMP JUMPDEST STOP JUMPDEST PUSH1 0x0 DUP1 SLOAD SWAP1 POP SWAP1 JUMP JUMPDEST PUSH1 0x1 PUSH1 0x0 DUP1 DUP3 DUP3 SLOAD ADD SWAP3 POP POP DUP2 SWAP1 SSTORE POP JUMP STOP LOG1 PUSH6 0x627A7A723058 KECCAK256 0xf5 0xdc DUP12 0xf 0xc9 0xcb 0xe 0xad 0xc8 ADDMOD 0xcf STOP MSIZE SWAP2 DUP5 0x4c PUSH3 0xDD87C PUSH19 0xEC6DFA9FBBF835820AB32F0029000000000000

![OPCODES](https://github.com/anakb/dev-pec1/blob/master/Ejercicio%203/C%C3%B3digos%20de%20operacion"OPCODES")

Desde la EVM

![OPCODES desde EVM](https://github.com/anakb/dev-pec1/blob/master/Ejercicio%203/SimpleCounter_sol_SimpleCounter.disasm.txt"OPCODES desde EVM")



---

**Identificadores de las funciones** 


```
{
    "8ada066e": "getCounter()",
    "d09de08a": "increment()"
}
```

![Identificadores de las funciones](https://github.com/anakb/dev-pec1/blob/master/Ejercicio%203/1.png "Identificadores de las funciones")

---

**Estimaciones del gas utilizado por cada función** 

```
{
    "Creation": {
        "codeDepositCost": "39000",
        "executionCost": "infinite",
        "totalCost": "infinite"
    },
    "External": {
        "getCounter()": "infinite",
        "increment()": "infinite"
    }
}

```

![Codefile - gas](https://github.com/anakb/dev-pec1/blob/master/Ejercicio%203/2.png "Codefile - gas")

Errores de la EVM a la hora de indicar el gas

![Codefile - error gas](https://github.com/anakb/dev-pec1/blob/master/Ejercicio%203/3.png "Codefile - error gas")