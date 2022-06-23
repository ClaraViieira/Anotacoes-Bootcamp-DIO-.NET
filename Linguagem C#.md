# Conhecendo a linguagem de programação C#

O C# é uma linguagem que foi criada paralelamente ao .NET. Sendo fortemente equipada e similar ao C, C++ ou Java. O código fonte do C# é compilado numa IL, e seus recursos são armazenados no disco de um arquivo executavél chamado assembly, de extensão .exe ou .dll. Dll é um código compilado numa linguagem intermediária. Ou seja, quando é feito o comando **dotnet build**, a linguaguem escrita em C#, sendo uma linguagem de alto nível, é compilado numa IL com extensão dll. Assim que o programa C# é executado, o assembly é corregado para o CLR, que transformará o C# em linguagem de máquina, ou uma linguagem de baixo nível. 

C# -> C# Compilador (Roslyn) -> Assembly (.exe ou .dll) -> IL -> CLR do .NET Framework -> Class Libraries -> Linguaguem de máquina.

# Estrutura de programa 

Programas C# são um ou mais arquivos, esse programas declaram tipos, que contem membros e são organizados em *namespace*, classes e interfaces são exemplos de tipos e campos, métodos, propiedades e eventos são exemplos de membros. 

# Variáveis do C#

Tipo de váriáveis de *valor*, possuem os dados diretamente. 

Tipos de variáveis | Comando no C#
-------------------|--------------
Numéricos          | **sbyte, short, int, lomg, byte, unshort, uint, ulong** 
Caracteres Unicode | **char**
Pontos Flutuantes  | **float, double, decimal**
Booleano           | **bool** 

Tipos de variáveis de *referência*, que armazem somente as referências de seus dados. 

Tipos de Variáveis | Comando no C#
-------------------|--------------
Classe             | **class, object, string**
Arrays             | **int[], int[,], etc...**

# Instruções

Ações de um programa que podemos agrupar num bloco, delimitado por chave -> { }

Bloco que permite que as instruções sejam escritas.

Intrução | Definição
---------|----------
*if, switch* | condicional
*while, do, for, foreach*  | repetição
*break, continue, return* | trabalha em conjunto com as instruções de condicional e repetição
*throw, try, catch, finally* | tratativa de excessão
*using* | importar referências dentro de uma classe

# Definição Arrays

É uma estrutara de dados que contém número x de elementos, todos do mesmo tipo, e são tipos de *referência*. Ao criar um Array, é especificado o tamanho da instância e é fixo durante o tempo de vida dessa instância. A posiçao inicia-se em 0 e seu comprimento é variado. 

# Classes, Objetos e Membros

A classe é uma estrutura de dados que combina estado (propriedades) e ações (métodos). Os objetos são instâncias de uma classe.  

Os membros nada mais são do que constantes, variáveis, métodos, propriedades, etc., de uma classe e podem ser estáticos ou de instância. Os estáticos pertencem a classe e os de instância pertecem ao objeto. 

# Structs, Interfaces e Enums

Os *structs* são estruturas de dados que podem ser de dados e de ação, e são do tipo de valor e não referência como as classes.

A *Interface* é como se fosse um contrato que pode ser implementada por classes e structs.

O *Enum* é um tipo de valor distinto com um conjunto de constantes nomeadas.

# Definindo Value Types

Contém uma **instância** do tipo criado. Em que essa **instância** é copiada ao atribuir o valor a outra variável. E o valor inicial é o valor default, que são os valores determinados. 

*Tipos primitivos* |
-----------------|
Valores numéricos (int, decimal, double, etc) |
Boolean (true/false) |
Char |
Tuples |

# Definindo Reference Types

Contém uma **refrência** para uma instância. A **referência** nunca muda seu valor ao atribuir o valor para outra variável. E seus valores são alocados na *HEAP*. Seu valor inicial é sempre NULL. 

*Tipos primitivos* |
-----------------|
Classe |
Innterface |
Delegate |
Record |
Object |
String |
