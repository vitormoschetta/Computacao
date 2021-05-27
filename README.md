## Sistema Binário

O sistema de números binários é uma forma de armazenar e enviar informações digitalmente, a partir de sinais elétricos, representados por `1` e/ou `0`.
Os circuitos elétricos possuem dois estados principais, ligado ou desligado, passando corrente ou não. Dessa forma, é possvel utilizar o sistema binário em circuitos eletrônicos para fins de comunicação. 

Podemos utilizar o [código de Morse](https://pt.wikipedia.org/wiki/C%C3%B3digo_Morse) como um comparativo.

Um único binário (0 ou 1) é chamado de `bit`.   
Um bit pode representar apenas um único caractere.  
Dois bits podem representar até 4 combinações de uns e zeros:  
``` 
00 
01
10
11
``` 
Nesse caso, podemos dizer que com dois bits podemos representar até 4 caracteres.  

Cada bit adicional dobra a quantidade de combinações possíveis de uns e zeros. Logo, com três bits podemos representar 4 x 2 combinações de uns e zeros, ou seja, 8 combinações diferentes:
``` 
000
001
010
011
100
101
110
111
``` 

Com quatro bits podemos apresentar 8 x 2 combinações diferentes de uns e zeros, ou seja 16 combinações. E assim por diante.

Com 7 bits, por exemplo, podemos representar 127 combinações diferentes de uns e zeros. E com essas 127 combinações diferentes é possível representar todo o alfabeto de caracteres e símbolos dos norte americanos. Falando nisso, o sistema ASCII foi criado justamente para isso. ASCII significa `American Standard Code for Information Interchange`, traduzido: `Código Padrão Americano para o Intercâmbio de Informação`.

Para esclarecer melhor, precisamos ter em mente que todo `objeto / valor` computacional precisa ter um endereço no circuito de memória. Porém, para se ter um endereço na memória também é preciso informar o quanto de memória esse objeto irá utilizar. 

Por exemplo, quero poder atribuir há um objeto chamado `alfabeto`, qualquer letra do alfabeto português do Brasil. Sei que existem 26 letras, então o maior valor que eu posso ter é 26. Esse objeto precisa ter quantos bits para que possa armazenar qualquer caractere do alfabeto? 

Como vimos anteriormente, com três bits podemos ter 8 combinações diferentes. Isso é suficiente? Não.   
4 bits equivale a 8 X 2 (16 combinações) é suficiente? Não.  
5 bits equivale a 16 X 2 (32 combinaçoes) é suficiente? Sim.  
Logo, concluímos que meu objeto `alfabeto` precisa ser declarado na memória como um objeto de 5 bits.  

Voltando onde estávamos, para representar todo o alfabeto e a numereção decimal, os americanos precisavam de apenas 7 bits. 


##### Avançando na história

Logo que a internet se difundiu, começou a ficar necessário a comunicação mundial. Acontece que alguns alfabetos pelo mundo precisam de muito mais que 127 caracteres (7 bits) para ser representado. Por isso surgiram outros padrões que utilizavam uma outra quantidade de bits para representar um sistema único de códigos e caracteres. O padrão de 256 caracteres (8 bits), por exemplo, foi amplamente utilizado. O modelo Latim1 que acrescentava símbolos da linguagem latina é um exemplo. Essa é uma das principais razões para a definição de `1 byte` como equivalente a `8 bits`. Ou seja, percebeu-se que com 8 bits era possível fazer muita coisa. 

Porém, nem tudo ainda era possível ser representado com 8 bits, e por isso foi decidido criar uma tabela de código único mundial, o **Unicode**. Porém, o unicode requer 3 bytes (24 bits) para representar qualquer caractere. Agora imagine os americanos tendo que utilizar 24 bits para armazenar seu alfabeto, sendo que antes fazia a mesma coisa com apenas 8 bits. Muito espaço perdido. 

Foi por isso que surgiu então o padrão **UTF-8**. Esse padrão possibilita que cada grupo de caracteres tenha um tamanho variável. Sendo assim, os caracteres ASCII e Latim1 podem utilizar 8 bits (1 byte) e outros caracteres poderão utilizar mais bits, evitando a perda desnecessária de espaço. Como isso é possível? Simples, o padrão UTF-8 utiliza os mesmos caractes do ASCII nas posições até 256. Portanto, fica fácil converter um grupo de caracteres ASCII ou Latim1 em UTF-8.


##### Numero ou Caractere?

No modelo de codificação ASCII, o número 65 pode ser equivalente ao número decimal '65' ou a letra 'A' do alfabeto. E como o computador sabe se estamos apresentado um número ou um caractere? O compilador deve informar isso. Logo as linguagens de programação e linguagens intermediárias possuem recurso para isso.


##### Curiosidade

Sabe aquelas páginas antigas da web que viamos coisas como a baixo:

![alt text](images/erro-codificacao.png?raw=true=250x250 "Title") 

Isso acontece exatamente porque informava-mos ao navegador utilizar um modelo de codificação ao mesmo tempo que nosso texto continha caracteres não suportados / mapeados por esse modelo. O navegador tentava achar na tabela do modelo o número binário referente aquele caractere e não encontrava.



##### Byte, Kilobyte, Megabyte, Gigabyte...

Um conjunto de 8 bits equivale a um `byte`. Um `kilobyte` equivale a 1.024 bytes, ou 8.192 bits. Um `megabyte` equivale a 1024 kilobytes, ou 8.388.608 bits. Um `gigabyte` equivale a 1024 megabytes, ou 8.589.934.592 bits.


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

Uma imagem computacional é representada por `pixels`, que são pequeníssimos pontos quadrados na tela. Quanto maior a resolução, maior o número de pixels, e consequentemente maior a qualidade da imagem. Quando a resolução é baixa, podemos observar os pixels na tela, pois a imagem apresenta um tom quadriculado.

Se uma imagem é formada por `pixels`, como os pixels são formados? Um pixel é formado por `24 bits`, ou `3 bytes`. Um byte para cada cor primário, ou seja, 1 byte para Vermelho, 1 byte para Verde e 1 byte para Azul.

Cada byte equivale a 8 bits, que pode conter 256 diferentes combinações. Ou seja, cada cor tem uma extremidade mais baixa (zero), representando o tom mais claro, e uma extremidade mais alta (255), representando o tom mais escuro da cor.

Logo, em um pixel existem a combinação dessas três cores, que formam uma cor determinante para aquela posição da tela na formação de uma imagem.

Se você der um zoom, com uma boa camera, em qualquer tela ligada (principalmente nos televisores ou monitores mais antigos), verá uma imagem parecida com esta:

![alt text](images/pixels.jpg?raw=true=250x250 "Title")  


#### Informação adicional: 

Existem algumas técnicas para diminuir a quantidade de bits utilizados por pixel. Uma delas é usar uma tabela de cores externa.

<br>



## Som Digital

Para converter sinal analógico em sinal digital com boa qualidade, é necessário observar dois parâmetros basicamente:

1. Frequência de amostra
    
    Tem haver com a constância na captação do som, com o mínimo de intervalo de tempo possível.

2. Taxa de bits

    Tem haver com a quantidade de tons sonoros capturados em cada intervalo de frequência. Com 16 bits é possível obter uma boa quantidade de tons: 65 mil tons. 
    Parece muito para tão pouco espaço? Mas definitivamente não é, se imaginarmos que cada pessoa tem seu próprio tom de voz, e que sua própria voz tem dezenas de milhares de tons distintos, então não é muito.

<br>



## Base64

Base64 é um método para codificação de dados para transferência na Internet. 

A codificação Base64 é frequentemente utilizada quando existe uma necessidade de transferência e armazenamento de dados binários para um dispositivo designado para trabalhar com dados textuais. Esta codificação é amplamente utilizada por aplicações em conjunto com a linguagem de marcação XML, possibilitando o armazenamento de dados binários em forma de texto. 

![alt text](images/base64.png?raw=true=250x250 "Title")  



<br>



## Bits e números inteiros

8 bits  --> 255 combinações
16 bits --> 65.535 combinações
32 bits --> 4.294.967.295 (bilhões) combinações
64 bits --> 18.446.744.073.709.551.615 combinações

<br>
<br>
<br>



#### Referências

<https://pt.wikipedia.org/wiki/Byte>

<https://athoselectronics.com/conversao-de-binario-decimal-hexadecimal/>

<https://www.copeltelecom.com/site/blog/kilobyte-megabyte-gigabyte-terabyte/#:~:text=Seguindo%20a%20mesma%20linha%20de,%C3%A9%20maior%20que%201%20byte%3B&text=Um%20Gigabyte%20%C3%A9%20composto%20por%201024%20Megabytes.>

<https://netiz.com.br/blog/saiba-as-diferencas-entre-megabits-megabytes-e-gigas/#:~:text=A%20mensura%C3%A7%C3%A3o%20da%20velocidade%20da,Mbps%20(megabits%20por%20segundo).&text=Uma%20vez%20que%2C%201%20Kbps,Mbps%20(megabits%20por%20segundo).>

<https://pt.wikipedia.org/wiki/Sistema_de_numera%C3%A7%C3%A3o_hexadecimal>

<https://www.embarcados.com.br/conversao-entre-sistemas-de-numeracao/>

<http://paulbourke.net/dataformats/bitmaps/index_pt.html>

<https://pt.wikipedia.org/wiki/Base64>








