using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace Sum_of_Two_Numbers
{
    class Program
    {
        static void Main(string[] args)
        {
            int start = int.Parse(Console.ReadLine());
            int end = int.Parse(Console.ReadLine());
            int check = int.Parse(Console.ReadLine());

            int firstNum = 0;
            int secondNum = 0;
            int sum = 0;
            int count = 0;

            for (int i = start; i <= end; i++)
            {
                for (int j = start; j <= end; j++)
                {
                    count++;
                    firstNum = i;
                    secondNum = j;
                    sum = firstNum + secondNum;

                    if (sum == check)
                    {
                        break;
                    }
                }
                if (sum == check)
                {
                    break;
                }
            }
            if (sum == check)
            {
            Console.WriteLine($"Combination N:{count} ({firstNum} + {secondNum} = {check})");               
            }
            else
            {
                Console.WriteLine($"{count} combinations - neither equals {check}");
            }
        }
    }
}
