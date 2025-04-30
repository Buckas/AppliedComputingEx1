# Applied Computing - Task 1: Simple Calculator
 
## Description: 
 
Create a console application that acts as a simple calculator. It should allow users to perform basic arithmetic operations (addition, subtraction, multiplication, and division) on two numbers.
 
## Analysis:
 
- **Scope:** The calculator will handle basic arithmetic operations.
- **Constraints:**
    - Only two input numbers at a time.
    - No support for complex expressions.
- **Requirements:**
    - User input for two numbers and an operator.
    - Display the result of the operation.

## Design:

- **UI:**
    - Prompt the user to enter two numbers and an operator.
    - Display the result.
- **Algorithm:**

    1. Read two numbers and an operator from the user.
    2. Perform the corresponding operation.
    3. Display the result.

<details>
  <summary>Sample Solution:</summary>
 
  ### Complete C# Code:
```
using System;

namespace SimpleCalculator
{
    class Program
    {
        static void Main(string[] args)
        {
            Console.WriteLine("Simple Calculator");
            Console.Write("Enter the first number: ");
            double num1 = Convert.ToDouble(Console.ReadLine());

            Console.Write("Enter an operator (+, -, *, /): ");
            char op = Convert.ToChar(Console.ReadLine());

            Console.Write("Enter the second number: ");
            double num2 = Convert.ToDouble(Console.ReadLine());

            double result = 0;
            switch (op)
            {
                case '+':
                    result = num1 + num2;
                    break;
                case '-':
                    result = num1 - num2;
                    break;
                case '*':
                    result = num1 * num2;
                    break;
                case '/':
                    result = num1 / num2;
                    break;
                default:
                    Console.WriteLine("Invalid operator.");
                    break;
            }

            Console.WriteLine($"Result: {result}");
        }
    }
}
```
</details>
