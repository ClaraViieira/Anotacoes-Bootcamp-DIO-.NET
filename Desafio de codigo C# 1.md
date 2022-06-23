# Desafios Iniciais - GFT Start #4 .NET

## Desafio 1/3 - Mês

Leia um valor inteiro entre 1 e 12, inclusive. Correspondente a este valor, deve ser apresentado como resposta o mês do ano por extenso, em inglês, com a primeira letra maiúscula.

**Entrada**

A entrada contém um único valor inteiro.

**Saída**

Imprima por extenso o nome do mês correspondente ao número existente na entrada, com a primeira letra em maiúscula.

 
Exemplo de Entrada	| Exemplo de Saída
--------------------|-----------------
4                   | April

## Resolução do Desafio 1/3 - Mês

<


        int mes = int.Parse(Console.ReadLine());

        switch (mes) 
        {
            case 1:
                Console.WriteLine("January");
                break;
            case 2:
                Console.WriteLine("February");
                break;
            case 3:
                Console.WriteLine("March");
                break;
            case 4: 
                Console.WriteLine("April");
                break;
            case 5: 
                Console.WriteLine("May");
                break;
            case 6:
                Console.WriteLine("June");
                break;
            case 7: 
                Console.WriteLine("July");
                break;
            case 8:
                Console.WriteLine("August");
                break;
            case 9: 
                Console.WriteLine("September");
                break; 
            case 10: 
                Console.WriteLine("October");
                break;
            case 11: 
                Console.WriteLine("November");
                break;
            case 12: 
                Console.WriteLine("December");
                break;
            default:
                Console.WriteLine("Digite um número válido de 1 a 12");
                break;
        }
        
>

## Desafio 2/3 - Quadrado e ao Cubo

Você terá o desafio de escrever um programa que leia um valor inteiro N (1 < N < 1000). Este N é a quantidade de linhas de saída que serão apresentadas na execução do programa.

**Entrada**

O arquivo de entrada contém um número inteiro positivo N.

**Saída**

Imprima a saída conforme o exemplo fornecido.

 
Exemplo de Entrada | Exemplo de Saída
-------------------|-----------------
5                  | 1 1 1
Not                | 2 4 8
Not                | 3 9 27
Not                | 4 16 64 
Not                | 5 25 125 

## Resolução do Desafio 2/3 - Quadrado e ao Cubo

<

            int n = int.Parse(Console.ReadLine());

            int inicio = 1;
            
            for (int i = 1; i <= n; i++)
            {
              Console.WriteLine($"{i} {i*i} {i*i*i}");
            }
              
>

## Desafio 3/3 - Soma de Pares Consecutivos

O programa deve ler um valor inteiro D indefinidas vezes, ele só irá parar quando o valor de D for igual a 0. Para cada D lido, imprima a soma dos 5 pares consecutivos a partir de D, inclusive ele mesmo , se for par. Se o valor de entrada for 4, por exemplo, a saída deve ser 40, que é o resultado da operação: 4+6+8+10+12, enquanto que se o valor de entrada for 11, por exempo, a saída deve ser 80, que é a soma de 12+14+16+18+20.

**Entrada**

O arquivo de entrada contém muitos valores inteiros. O último valor do arquivo é zero.

**Saída**

Imprima a saida conforme a explicação acima e o exemplo abaixo.

 
Exemplo de Entrada | Exemplo de Saída
-------------------|----------------
4                  | 40
11                 | 80

## Resolução do Desafio 3/3 - Soma de Pares Consecutivos

<

            int soma = 0, cont = 1, armazenaX = 0;
            
            while (true)
            {
              int x = int.Parse(Console.ReadLine());
              armazenaX = x;
              
              if (x % 2 == 0)
              {
                soma += x;
              }
              else
              {
                armazenaX = x + 1;
                soma += armazenaX;
              }
              while (cont < 5)
              {
                armazenaX += 2;
                soma += armazenaX;
                cont++;
              }
              if (x == 0) break;
              
              Console.WriteLine(soma);
              cont = 1;
              soma = 0;
            }
>
