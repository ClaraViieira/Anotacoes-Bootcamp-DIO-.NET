# História do .NET 

Para entender o que é a atual plataforma do .NET, precisamos entender como surgiu essa plataforma, as linguagens que são utilizadas dentro dela, e claro, todo o contexto por trás desse framework. 

Antes de começar a falar do .NET, precisamos falar sobre a Microsoft, pois foi a partir da criação das linguagens de progranação, iniciado com a **Basic**, que se deu início ao percurso do .NET. 

Logo depois a Microsoft firma uma parceria com a IBM, dando início ao sistema DOS. E a partir dali, a Microsoft começa a focar em sistemas operacionais, logo visando o OS Windows. 

Foi a partir daí, que a Microsoft começou a criar IDE's e runtimes com uma única ferramenta, chamada de **Visual Basic 97**, que perimtia trabalhar com diversas linguagens de progrramação, como C++, VS Basic, J++, entre outros. Desse ano em diante, a Microsoft começou a atualizar sua plataforma, sempre atualizando as linguagens embutidas dentro da ferramenta. Ou seja, logo foi lançada a **Visual Studio 6**, com o VS 6, C++ 6 e por ai vai. 

Em 99, foi criado o ASP+, que é uma plataforma web de desenvolvimento, que mais para a frente seria utilizada na plataforma do .NET Framework. Nesse mesmo ano, foi criada a commom runtime, a CLR, que é a limguagem intermediária digamos assim, que compila os códigos a uma limguagem de máquina. E também foi dado início a criação da limgaguem C#.

No ano seguinte, a Microsoft enfim lança o ambiente de desenvolvimento .NET Framework 1.0. No entanto, essa plataforma era somente para usuários do Windows. Em 2002, foi lançado o VS .NET com 22 linguagens de programação, inclusive com o C# 1.0, tudo isso em 1 plataforma.  Em 2003 lança o .NET Framework 1.1, com o VS 2003, e melhorias na CLR, criando a CLR 2. Em 2005 é lançado o .NET Framework 2.0 com C# 2.0, no VS 2005. Entre 2007 e 2008 ocorre o lançamento do .NET Framework 3.5 com C# 3.0 no VS 2008. Em 2010 é lançado o .NET Framework 4.0 com C# 4.0 no VS 2010. 

Em 2011 é lançado o Xamarin, que desenvolvia aplicativos em C# para usuários de Android e IOS. 

Em 2012 é lançado o .NET Framework 4.5 com C# 5.0 no VS 2012. E é lançado o Typescript. Em 2013 é lançada o .NET 4.5.1 no VS 2013. 

Mesmo com esses diversos lançamentos e atualizações de plataforma da Microsft, tudo era muito voltado para o Windows, restringindo acesso de usuários de outros sistemas operacionais. 

É ai então, que o novo CEO da Microsoft direciona o foco para a Cloud, ou seja, a nuvem, deixando seu foco em sistemas operacionais, e cria então o .NET Foundation, que gerencia projetos open source.

Em 2014 é introduzido o conceito de ASP.NET, em que o .NET Framework possui uma parte de desenvolvimento Web, que é o ASP.NET vNext, posteriormente chamado de ASP.NET Core. ASP.NET vNext funcionaria como uma biblioteca de classe base. 

Em 2015 é lançado o .NET Framework 4.6 com C# 6.0 no VS 2015, mas também é lançado o **Visual Studio Code**, que é um editor dee códigos que utiliza diversas linguagens como .NET, java, entre outros, sendo open source e multiplataforma, ou seja, roda em diversos sistemas operacionais. 

Em 2016 a Microsoft adiquire a Xamarin ao .NET como open source. E lança o **Visual Studio for MAC**, rodando então em MAC-OS também e não só Windows. 

E então em 2016 é lançado o .NET Core 1.0, sendo uma plataforma nova, open source e multiplataforma. Lembrando que até então, o .NET Framework não é multiplaforma, somente roda em sistemas operacionais Windows, mas é open source. 

Em 2017 é lançado o .NET Framework 4.7 com C# 7 no VS 2017. E também é lançado o .NET Core 2.0 com C# 7.0 no VS 2017, VSCode e VS for MAC. 

Fazendo um adendo aqui, a necessidade de se criar o VSCode se deu também por motivos do VS ser um programa muito pesado e o VSCode ser algo mais leve e fácil de rodar no sistema. 

Em 2019 foi lançado o .NET Framework 4.8 com C# 7.3 no VS 2019. E o .NET Core 3.0 com C# 8.0 no  VS 2019, VSCode e VS for MAC. 

Em 2020 o .NET Framework é finalizado na versão 4.8. A plataforma ainda existe e é sim utilizada para algumas funcionalidades, no entanto, deixa de ser evoluída constantemente como o .NET 5, que foi posteriomente lançado, atualmente em 2022, estamos no .NET 7. 

# Conceitos e Descrições do .NET 

Mas o que é então o .NET? É uma infraestrutura que desenvolve softwares. O .NET consiste em algumas implementações, como o .NET Framework, .NET Core, Mono, etc.. 

E como essas implementações conversam entre si? Assim que foi sendo criado essas novas versões das plataformas, a Microsoft se viu na necessidade de criar o .NET Standard, que nada mais é do que o contrato entre essas versões. o que significa que, todas as versões e funcionalidades que a plataforma do .NEt Core tem por exemplo, o .NET Framework também terá, para que seja possível que conversem entre sim. 

E todas as implementações possuem o .NET Runtimes, que são os compiladores que convertem os códigos em linguagem de máquina. 

# Comandos do .NET - 1ª aula

Para usar o .NET é necessário que o CMD, ou Prompt de Comando, seja aberto e alguns comando sejam indicados para que o objetivo seja atingido. 

Para se verificar a versão do .NET que foi instalada no seu desenvolvedor local, vamos usar o comando **dotnet --version**. 

Para verificarmos quais aplicações podem ser feitas através do .NET, podemos lançar o comando **dotnet --help**, que irá nos mostrar quais aplicações, comandos e opções temos para a utilização do .NET. Podemos também lançar o **dotnet new console -h** para sabermos mais informações sobre os comandos de console.

Para criarmos um Console, que utiliza a linguagem C#, F# e VB, iremos utilizar o comando **dotnet new console -n "nome da pasta que deseja criar"**, após isso, será criada uma pasta de "Console de Aplicativos" e iremos entrar nessa pasta lançando o comando **cd "nome da pasta criada"**. Feito isso, podemos usar o comando **explorer .** para que a pasta seja aberta no diretório em que foi criada pelo terminal. Então para que ela seja aberta no VSCode. usamos o comando **code .**. 

Em seguida iremos lançar o **dotnet restore** para os restaurar os pacotes, caso tenhamos. Então podemos lançar um **dotnet build** que também restaura os pacotes, porém também pega o código fonte e faz toda a compilação para gerar o bináro, gerando um dll. Depois lança um **dotnet run**, que irá restaurar os pacotes e executar um build e logar do writeline do código. 

