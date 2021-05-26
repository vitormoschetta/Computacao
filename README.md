## Sistema Binário

O sistema de números binários é uma forma de armazenar e enviar informações digitalmente, a partir de sinais elétricos, representados por `1` e/ou `0`.
Os circuitos elétricos possuem dois estados principais, ligado ou desligado, passando corrente ou não. Dessa forma, é possvel utilizar o sistema binário em circuitos eletrônicos para fins de comunicação. 

Podemos utilizar o [código de Morse](https://pt.wikipedia.org/wiki/C%C3%B3digo_Morse) como um comparativo.

Um único binário (0 ou 1) é chamado de `bit`. Um conjunto de 8 bits equivale a um `byte`. Um `kilobyte` equivale a 1.024 bytes, ou 8.192 bits. Um `megabyte` equivale a 1024 kilobytes, ou 8.388.608 bits. Um `gigabyte` equivale a 1024 megabytes, ou 8.589.934.592 bits.

<br>



## Mbps (Mega Bits por Segundo)

A velocidade de conexão com a internet é medida na escala de Mega Bits por Segundo. 

Se você possui um pacote de 100 Mega (megabit) você irá baixar arquivos em uma velocidade de 12,5 megabytes por segundo. Acompanhe:
100 Megabits é igual 100.000 (cem mil) bits. Considerando que 1 byte tem 8 bits, divide-se 100.000 / 8, que fica 12.500 bytes, ou seja, 12.5 Megabytes.

<br>



## Sistema Hexadecimal

O sistema hexadecimal é um sistema de numeração posicional que representa os números em base `16`. Nele, além dos números decimais de 0 (zero) a 9 (nove), são adicionados as letras do alfabeto de A a F, totalizando 16 caracteres.

Mas porque isso é necessário? Lembra que cada bit é representado por um único caractere? E também que `bytes` são multiplos de 8 `bits`? Com 2 (dois) bytes podemos representar muitas coisas na computação. 2 bytes equivalem a 16 bits, e na numeração decimal não possuímos 16 caracteres, mas apenas 10 (0 a 9). Logo, esse é o motivo de na numeração hexadecimal acrescentarmos as letras do alfabeto de A a F, somando mais 6 caracteres, totalizando 16.

![alt text](images/tabela.jpg?raw=true=250x250 "Title") 

<br>

## Conversões

#### Conversão de Decimal Para Binário:

![alt text](images/decimal-binario.jpg?raw=true=250x250 "Title")  

Se divide sempre por 2 (dois) anotando o resto da divisão, que será sempre 0 (zero) ou 1 (um). Se a ultima divisão não for um número inteiro (1 / 2 por exemplo) o resto valerá 1 (um) também. Depois junta os números restos (uns e zeros) de tráz pra frente.

<br>

#### Conversão Binário para Decimal:

![alt text](images/binario-decimal.jpg?raw=true=250x250 "Title")  

Abaixo de cada bit binário (1 ou 0), da direita para a esquerda, iniciando com o número 1 (um), e colocando múltiplos de 2 (dois), um abaixo de cada bit binário. 
Depois é só multiplicar o bit binário pelo respectivo número multiplo de dois adicionado abaixo, anotando os resultados. Por fim, basta somar os resultados.

<br>



## Cores e Pixels

Existem três cores primárias pelas quais podemos formar as demais, são elas: `Vermelho`, `Verde` e `Azul`. Em inglês: `Red`, `Green` e `Blue`, abreviados na computação como `RGB`.

Uma imagem computacional é representada por `pixels`, que são pequeníssimos pontos quadrados na tela. Quanto maior a resolução, maior o número de pixels, e consequentemente maior a qualidade da imagem. Quando a resolução é baixa, podemos observar os pixels na tela, pois a imagem apresenta quadrados definidos. 

Se uma imagem é formada por `pixels`, como os pixels são formados? Um pixel é formado por `24 bits`, ou `3 bytes`. Um byte para cada cor primário, ou seja, 1 byte para Vermelho, 1 byte para Verde e 1 byte para Azul.

Cada byte equivale a 8 bits, que pode conter 256 diferentes combinações. Ou seja, cada cor tem uma extremidade mais baixa (zero), representando o tom mais claro, e uma extremidade mais alta (255), representando o tom mais escuro da cor.

Logo, em um pixel existem a combinação dessas três cores, que formam uma cor determinante para aquela posição da tela na formação de uma imagem.

Se você der um zoom, com uma boa camera, em qualquer tela ligada (principalmente nos televisores ou monitores mais antigos), verá uma imagem parecida com esta:

![alt text](images/pixels.jpg?raw=true=250x250 "Title")  


#### Informação adicional: 

Existem algumas técnicas para diminuir a quantidade de bits utilizados por pixel. Uma delas é usar uma tabela de cores externa.



<br>
<br>
<br>



#### Referências

<https://athoselectronics.com/conversao-de-binario-decimal-hexadecimal/>

<https://www.copeltelecom.com/site/blog/kilobyte-megabyte-gigabyte-terabyte/#:~:text=Seguindo%20a%20mesma%20linha%20de,%C3%A9%20maior%20que%201%20byte%3B&text=Um%20Gigabyte%20%C3%A9%20composto%20por%201024%20Megabytes.>

<https://netiz.com.br/blog/saiba-as-diferencas-entre-megabits-megabytes-e-gigas/#:~:text=A%20mensura%C3%A7%C3%A3o%20da%20velocidade%20da,Mbps%20(megabits%20por%20segundo).&text=Uma%20vez%20que%2C%201%20Kbps,Mbps%20(megabits%20por%20segundo).>

<https://pt.wikipedia.org/wiki/Sistema_de_numera%C3%A7%C3%A3o_hexadecimal>

<https://www.embarcados.com.br/conversao-entre-sistemas-de-numeracao/>

<http://paulbourke.net/dataformats/bitmaps/index_pt.html>








