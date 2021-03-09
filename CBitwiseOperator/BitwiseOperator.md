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
| Giriş      	| İşlem   		| 
| ------------- |:----------------: 	| 
| a            	| 0000 0000 0000 1100   | 
| b             | 0000 0000 0000 1010   |
| a & b         | 0000 0000 0000 1000   |


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
| a \| b        | 0000 0000 0000 1110   |


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
| a ^ b       	| 0000 0000 0000 0110   |

# Slayt 31 Saga Bit Kaydırma (>>)

| Verinin hareket yönü	| Sag ========>>>>>   		| 
| -------------		|:----------------: 		| 
| Orjinal Sayı A        | 0000 0000 0011 1100   	| 
| 1 bit kaydırma        | **0**000 0000 0001 1110   	|


# Slayt 35 Saga Bit Kaydırma (>>)
```c
#include<stdio.h>
int main()
{
	int a = 60;
	printf("\nNumber is Shifted By 1 Bit  : %d",a >> 1);
	printf("\nNumber is Shifted By 2 Bits : %d",a >> 2);
	printf("\nNumber is Shifted By 3 Bits : %d",a >> 3);

	return(0);
}
```
| Giriş      	| İşlem   			| 
| -------------	|:----------------: 		| 
| a            	| 0000 0000 0011 1100   	| 
| a >> 1        | **0**000 0000 0001 1110   	|
| a >> 2       	| **00**00 0000 0000 1111   	|
| a >> 3       	| **000**0 0000 0000 0111   	|



# Slayt 38 Sola Bit Kaydırma (<<)

| Verinin hareket yönü	| Sol <<<<<========   		| 
| -------------		|:----------------: 		| 
| Orjinal Sayı A        | 0000 0000 0011 1100   	| 
| 1 bit kaydırma        | 0000 0000 0111 100**0**   	|


# Slayt 41 Sola Bit Kaydırma (<<)
```c
#include<stdio.h>
int main()
{
	int a = 60;
	printf("\nNumber is Shifted By 1 Bit  : %d",a << 1);
	printf("\nNumber is Shifted By 2 Bits : %d",a << 2);
	printf("\nNumber is Shifted By 3 Bits : %d",a << 3);

	return(0);
}
```
| Giriş      	| İşlem   			| 
| -------------	|:----------------: 		| 
| a            	| 0000 0000 0011 1100   	| 
| a << 1        | 0000 0000 0111 100**0**   	|
| a << 2       	| 0000 0000 1111 00**00**  	|
| a << 3       	| 0000 0001 1111 0**000**   	|


# Slayt 45 Bit Maskeleme
Gerekli verilerin tutulup ve kalanının maskelenmesi (bloke edildigi)
En Sık Kullanılan Operatör: AND (&)

| Giriş      		| İşlem  (AND) 			| 
| -------------		|:----------------: 		| 
| veri          	| 0000 0000 100\|101\|01   	| 
| maske        		| 0000 0000 000\|**111**\|00   	|
| maskelenmiş veri	| 0000 0000 000\|**101**\|00 	|

# Slayt 51 Bit Kaydırma (Negatif Sayılar)
```c
#include<stdio.h>
void main()
{
	printf("%x",-1<<4);
}
```
| Giriş      	| Giriş 	| İşlem						|
| -------------	|:-------------:| :----------------:				|	 		 
| -1	        | FFFFFFFF	| 1111 1111 1111 1111 1111 1111 1111 1111	|
| -1 << 1      	| FFFFFFF**E**	| 1111 1111 1111 1111 1111 1111 1111 111**0**	|
| -1 << 2	| FFFFFFF**D**	| 1111 1111 1111 1111 1111 1111 1111 11**00**	|
| -1 << 3	| FFFFFFF**8** 	| 1111 1111 1111 1111 1111 1111 1111 1**000**	|
| -1 << 4	| FFFFFFF**0** 	| 1111 1111 1111 1111 1111 1111 1111 **0000**	|

# Slayt 53 Bit Kaydırma (Negatif Sayılar)
```c
#include<stdio.h>
int main()
{
	int a = -60;
	
	printf("\nNegative Right Shift by 1 Bit : %",a >> 1);
	printf("\nNegative Right Shift by 2 Bits : %d",a >> 2);
	printf("\nNegative Right Shift by 3 Bits : %d",a >> 3);

	return(0);
}
```
Negative Right Shift by 1 Bit  : -30
Negative Right Shift by 2 Bits : -15
Negative Right Shift by 3 Bits : -8


# Slayt 55 printf içinde degisken kaydırma
```c
#include<stdio.h>
main()
{
	int i;
	for(i=0;i<5;i++)
   		printf("%d\n", 1 << i);
}

```
| Giriş      	| Giriş 	| İşlem						|
| -------------	|:-------------:| :----------------:				|	 		 
| 1	        | 00000001	| 0000 0000 0000 0000 0000 0000 0000 0001	|
| 1 << 0      	| 0000000**1**	| 0000 0000 0000 0000 0000 0000 0000 0001	|
| 1 << 1	| 0000000**2**	| 0000 0000 0000 0000 0000 0000 0000 001**0**	|
| 1 << 2	| 0000000**4** 	| 0000 0000 0000 0000 0000 0000 0000 01**00**	|
| 1 << 3      	| 0000000**8**	| 0000 0000 0000 0000 0000 0000 0000 1**000**	|
| 1 << 4	| 000000**10**	| 0000 0000 0000 0000 0000 0000 0001 **0000**	|


# Slayt 63 1’e tümleme

| Giriş      		| İşlem  (AND) 			| 
| -------------		|:----------------: 		| 
| Orjinal Sayı A        | 0000 0000 0011 1100   	| 
| 1’e Tümlenmis A       | 1111 1111 11**00 00**11   	|

# Slayt 65 1’e tümleme
```c
#include<stdio.h>
int main()
{
	int a=10;
	printf("\nNegation of Number 10 : %d",~a);
	return(0);
}
```
| Giriş			| İşlem  			| 
| -------------		|:----------------: 		| 
| a			| 0000 0000 0000 1010   	| 
| ~a			| 1111 1111 1111 **01 01**   	|

Ekran:
	Negation of Number 10 : -11
	
# Slayt 68 BIT_GET
```c
#define BIT_GET(VAR, BIT_NO) ((VAR >> BIT_NO) & 1)
```

| BIT_NO		| İşlem		  			| 
| -------------		|:----------------: 			| 
| 			| VAR			11**0**0   	| 
| BIT_NO = 0 =>		| VAR >> BIT_NO		1100   		|
| BIT_NO = 1 =>		| VAR >> BIT_NO		011**0**   	|


|	|	|		|
|-------|-------|---------------|
|	|VAR	|011**0**	|
|&	|1	|0001		|
|	|	|0000		|


# Slayt 70 BIT_GET
```c
#define BIT_GET(VAR, BIT_NO) ((VAR >> BIT_NO) & 2)
```

| BIT_NO		| İşlem		  			| 
| -------------		|:----------------: 			| 
| 			| VAR			1**1**00   	| 
| BIT_NO = 0 =>		| VAR >> BIT_NO		1100   		|
| BIT_NO = 1 =>		| VAR >> BIT_NO		0110   		|
| BIT_NO = 2 =>		| VAR >> BIT_NO		001**1**   	|


|	|	|		|
|-------|-------|---------------|
|	|VAR	|001**1**	|
|&	|1	|0001		|
|	|	|0001		|

# Slayt 70 BIT_SET
```c
#define BIT_SET(VAR, BIT_NO) do { 
VAR |= 1<<BIT_NO; 
} while (0)
```
| BIT_NO		| İşlem		  			| 
| -------------		|:----------------: 			| 
| 			| 1			00**0**1   	| 
| BIT_NO = 0 =>		| 1 << BIT_NO		0001   		|
| BIT_NO = 1 =>		| 1 << BIT_NO		00**1**0   	|
| BIT_NO = 2 =>		| 1 << BIT_NO		0100    	|
| BIT_NO = 3 =>		| 1 << BIT_NO		1000   		|

|	|		|		|
|-------|---------------|---------------|
|	|VAR		|01**0**1	|
|\|	|1 << BIT_NO	|0010		|
|	|VAR		|01**1**1	|	



