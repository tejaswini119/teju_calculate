# teju_calculate
using System;

namespace ConsoleApp5
{
    class Program
    {
        static void Main(string[] args)
        {
            double num1, num2, ans;
            char op;

            while (true)
            {
                Console.Write("\nEnter first number:");
                num1 = double.Parse(Console.ReadLine());
                Console.Write("Enter second number:");
                num2 = double.Parse(Console.ReadLine());
                Console.Write("enter the operator(+,-,*,/):");
                op = char.Parse(Console.ReadLine());

                try
                {
                    if (num2 == 0 && op == '/')
                    {
                        throw new Exception("the number is zero");
                    }
                    if(op!='+')
                    {
                        if (op != '-')
                        {
                            if(op!='*')
                            {
                                if(op!='/')
                                {
                                    throw new Exception("invalid operator");
                                }
                            }
                        }
                    }
                    

                    switch (op)
                    {
                        case '+':
                            ans = num1 + num2;
                            break;
                        case '-':
                            ans = num1 - num2;
                            break;
                        case '*':
                            ans = num1 * num2;
                            break;
                        case '/':
                            ans = num1 / num2;
                            break;
                        default:
                           
                            return;

                    }
                    

                    Console.Write("The result is as follows\n");
                            Console.Write(num1 + " " + op + " " + num2 + " " + "=" + " " + ans);
                    
                }



                catch (Exception e)
                {
                    Console.WriteLine(e.Message);
                }

            }
            
        }


    }
}

