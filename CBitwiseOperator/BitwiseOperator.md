# Slayt 1 Veri Tipleri
| Veri Tipi     | Byte(8 Bit)   | 
| ------------- |:-------------:| 
| char          | 8             | 
| byte          | 8             |
| short         | 16            |
| int           | 32            |
| long          | 64            |
| float         | 32            |
| double        | 64            |
| boolean       | 1             |

# Slayt 10 Bit Operatörleri
| Operator      | islem   | 
| ------------- |:-------------:    | 
| ~             | 1’ tümleyen       | 
| >>            | Sağa Kaydırma     |
| <<            | Sola Kaydırma     |
| &             | Bit düzeyinde AND |
| |             | Bit düzeyinde OR  |
| ^             | Bit düzeyinde XOR |

# Slayt 16 Bit Operatörleri
| Giriş Bitler      | AND   OR    XOR   | 
| -------------     |:----------------: | 
| 0   0             | 0     0     0     | 
| 0   1             | 0     1     1     |
| 1   0             | 0     1     1     |
| 1   1             | 1     1     0     |


# Slayt 24 AND
```c
#include<stdio.h>
int main()
{
	int a=12;
	int b=10;
	printf("\nNumber1 AND Number2 : %d",a & b);
	return(0);
}
```
| Giriş      | İşlem   | 
| -------------     |:----------------: | 
| a            | 0000 0000 0000 1100     | 
| b             | 0000 0000 0000 1010    |
| a and b           | 0000 0000 0000 1000    |


# Slayt 27 OR
```c
#include<stdio.h>
int main()
{
	int a=12;
	int b=10;
	printf("\nNumber1 OR Number2 : %d",a | b);
	return(0);
}
```
| Giriş      	| İşlem   		| 
| -------------	|:----------------: 	| 
| a            	| 0000 0000 0000 1100	| 
| b             | 0000 0000 0000 1010   |
| a or b        | 0000 0000 0000 1110   |


# Slayt 29 XOR
```c
#include<stdio.h>
int main()
{
	int a=12;
	int b=10;
	printf("\nNumber1 XOR Number2 : %d",a ^ b);
	return(0);
}
```
| Giriş      	| İşlem   		| 
| -------------	|:----------------: 	| 
| a            	| 0000 0000 0000 1100   | 
| b             | 0000 0000 0000 1010   |
| a xor b       | 0000 0000 0000 0110   |

# Slayt 31 Saga Bit Kaydırma (>>)

| Verinin hareket yönü	| Sag ========>>>>>   	| 
| -------------		|:----------------: 	| 
| Orjinal Sayı A        | 0000 0000 0011 1100   | 
| 1 bit kaydırma        | ~~**0**~~0000 0000 001 1110   |







