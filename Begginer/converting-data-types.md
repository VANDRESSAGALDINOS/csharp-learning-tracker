# Conversão de Tipos em C#

A conversão de tipos em C# é o processo de transformar um valor de um tipo de dado em outro. Ela pode ser classificada em dois tipos principais:

- **Conversão implícita**: ocorre automaticamente quando não há risco de perda de dados. Por exemplo, ao converter um valor `int` em um `double`, o C# realiza a conversão sem a necessidade de intervenção explícita, já que o tipo `double` pode armazenar todos os valores que um `int` pode conter.

- **Conversão explícita (casting)**: exige o uso de um operador de conversão, pois pode ocorrer perda de dados. Um exemplo seria converter um `double` em um `int`, onde as partes decimais são truncadas.

## Exemplo Prático de Conversão de Tipos em C#

Abaixo, temos um código em C# que demonstra os dois tipos de conversão:

```csharp
using System;

class Program
{
    static void Main(string[] args)
    {
        // Exemplo de números com casas decimais
        double positiveDouble = 3.75;
        double negativeDouble = -3.75;

        // Conversão explícita de double para int
        // Aqui a parte decimal é truncada
        int positiveInt = (int)positiveDouble; // Resultado: 3
        int negativeInt = (int)negativeDouble; // Resultado: -3

        Console.WriteLine($"Positive double: {positiveDouble}, converted to int: {positiveInt}");
        Console.WriteLine($"Negative double: {negativeDouble}, converted to int: {negativeInt}");

        // Uso do método Convert para conversões mais flexíveis
        // Pedir um número favorito ao usuário
        Console.Write("Enter your favorite number: ");
        
        // Ler a entrada do usuário como string e converter para int
        int faveNumber = Convert.ToInt32(Console.ReadLine());
        Console.WriteLine($"Your favorite number is: {faveNumber}");
    }
}
