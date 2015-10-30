# Points-Answer
By flyroof (Blagovesta)
I use C# as a programming language. Here is the program for the task "Points":

using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApplication1
{
    class Program
    {   
   
        
        
        static void Main(string[] args)


        {
            string[] x = Console.ReadLine().Split('(',')',',').ToArray();
            int a = int.Parse(x[1]);
            int b = int.Parse(x[2]);
            string f = Console.ReadLine();
            int sign = 1;
            for (int j = 0; j < f.Length; j++)
            {
                
                switch (f[j])
                {
                    case '~': sign*=-1; break;
                    case '<': a-=sign; break;
                    case '>': a+=sign; break;
                    case '^': b-=sign; break;
                    case 'v': b+=sign; break;
                
                }
            
            }

            Console.WriteLine("({0},{1})",a,b);

        }

    }
}
