## Curso - Fundamentos do C# - Balta.io

Números inteiros
- Aceita números positivos e negativos que não possuam casas decimais;
- Quando houver a letra "u" na frente do seletor do campo, significa unsigned, ou seja, sem sinal; 
- Campos iniciados com "u" aceitam somente números positivos.

Tipos:
- short/unshort
- int/uint
- long/ulong

```
  int idade = 25;
```

Numeros reais 
- Números que possuem casas decimais; 
- Possuem assimilação negativa e positiva por padrão, dispensando o uso do signed/unsigned em seus tipos.

Tipos:
- float (Notação F)
- double
- decimal (Notação M)

```
  double salario = 1500.30;
```

Bool 
- Armazena apenas true ou false

```
  bool usuarioLogado = false;
```

Char
- Utilizado para armazenar apenas um caractere no formato Unicode

```
  char sexo = 'm';
```

String
- Armazena uma cadeia de caracteres. 

```
  string texto = "Hello World";
```

Var
- Substitui o nome de um tipo

```
  var idade = 25; //Será do tipo int
  var nome = "Kenny" //Será do tipo string
```

Object
- Tipo genérico que recebe qualquer valor ou objeto; 
- Utilizado quando não souber o tipo da informação ou ela seja de vários tipos diferentes. (Evite usar)

```
  object idade = 25; //Será do tipo object
  object nome = "Kenny"; //Será do tipo object
```

Null
- Significa vazio; 
- Diferente de zero ou uma string vazia;
- Todo tipo primitivo pode receber o valor null;
- Pode-se atribuir null a um objeto desde que o mesmo seja marcado como nullabe usando interrogação na frente do tipo.

  ```
    int? idade = null;
  ```

Alias
- É um apelido que todo tipo no .NET tem
- System.String = string
- O C# é case sensitive, ou seja, ele identifica o maiúsculo do minúsculo;

```
  int idade = 25; //Alias
  Int32 idade = 25; //Sem alias
```

Valores Padrões
- Caso nenhum for informado no tipo escolhido, seu valor padrão será utilizado;
- int = 0;
- float = 0;
- decimal = 0;
- bool = false;
- char = '\0';
- string = "";

Conversão Implícita
- São conversões que podem ser executadas apenas com passagem de dados;
- Possuem tipos compatíveis.

```
  float valor = 25.8f;
  int outro = 25;
  valor = outro; //Conversão implícita
```

Conversão Explícita
- Ocorre quando os tipos não são compatíveis;
- É dada pelo uso do tipo entre parênteses antes da atribuição;
- Segue as mesmas regras anteriores.

```
  int inteiro = 100;
  utin inteiroSemSinal = (uint)inteiro; //Conversão explícita
```

Parse
- Todo tipo primitivo tem .parse;
- Usado para converter um caractere ou string para um tipo qualquer.

```
  int inteiro = int.Parse("100");
```

Convert
- Similar ao parse;
- Permite converter vários tipos de valor, não somente string. 

```
  int inteiro = Convert.ToInt32("100");
```

Operações Aritméticas
- Aceita short, int, float, double e decimal;
- Multiplicação e divisão são executadas primeiro, caso queria outra ordem, usar parênteses.
- Soma +
- Subtração -
- Multiplicação *
- Divisão /

Operações de atribuição
- Utilizamos o = para atribuir um valor.

```
  int x = 0; //Atribuição
  x += 5; // x = x + 5;
  x -= 1; // x = x - 1;
  x *=10; // x = x * 10;
  x /= 2; // x = x / 2;
```

Operações de comparação
- Podemos comparar qualquer tipo de dado;
- A comparação SEMPRE retorna verdadeiro ou falso
- Igual ==
- Diferente !=
- Maior que >
- Menor que <
- Maior ou igual >=
- Menor ou igual <=

Operações Lógicas
- Usado para operações condicionais;
- Retorna sempre true ou false;
- AND (E) && - Deve atender TODAS as condições;
- OR (OU) || - Deve atender PELO MENOS uma condição;
- NOT (NÃO) ! - Negação.

IF
Utilizado quando deseja-se fazer uma comparação.

```
using System;

namespace MeuApp
{
    class Program
    {
        static void Main (string[] args)
        {
            if(25 == 32)
            {
              Console.WriteLine("É diferente");
            } else{
              Console.WriteLine("É igual");
            }
            Console.WriteLine("Finalizou o programa");
        }
    }
}
```

Switch
- Utilizado quando temos muitas decisões;
- Devemos parar manualmente a execução com o comando break;
- Possui execução padrão (Default).

```
using System;

namespace MeuApp
{
    class Program
    {
        static void Main (string[] args)
        {
           string valor = "kenny";
           switch (valor)
           {
              case "joao": 
              Console.WriteLine("Nome errado");
              break
              
              case "marcelo": 
              Console.WriteLine("Nome errado");
              break
              
              case "kenny": 
              Console.WriteLine("Nome certo");
              break
              
              default:
              Console.WriteLine("Nome certo");
              break
           }
        }
    }
}
```
























