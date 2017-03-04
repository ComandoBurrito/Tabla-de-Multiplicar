//# Tabla-de-Multiplicar
//Programa para saber la tabla de multiplicar del 1 al 10 de casi cualquier numero

using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using System.Threading;

namespace Ejercico_Bucles_While_y_For
{
    class Program
    {
        static void Main(string[] args)
        {
            //Ciclo while
            //Parte 1 Valor inicial
            //Parte 2 Condicion
            //Parte 3 Aumento o Decremento

            int x, resultado;
            string reset;
            Console.ForegroundColor = ConsoleColor.Green;
        inicio:
            Console.WriteLine("Ingrese Tabla a calcular");
            x = int.Parse(Console.ReadLine());
            Console.WriteLine("");
            Thread.Sleep(800);
            Console.WriteLine("Resultado");
            
            for (int i = 1; i <= 10; i++)
            { 
                Thread.Sleep(400);
                resultado = x * i;
                
                if (i == 11)
                {
                    Thread.Sleep(800);
                    goto liquidacion;
                }
                Console.WriteLine(x + " x " + i + " = " + resultado);
            }
        liquidacion:
            Console.WriteLine("");
            Thread.Sleep(800);
            Console.WriteLine("Desea continuar?");
            reset = Console.ReadLine();
            switch (reset)
            {
                case "Si":
                    Console.WriteLine("");
                    Thread.Sleep(400);
                    Console.WriteLine("Restaurando");
                    Thread.Sleep(800);
                    Console.Clear();
                    goto inicio;
                case "No":
                    Console.WriteLine("");
                    Thread.Sleep(400);
                    Console.WriteLine("Apagando");
                    Thread.Sleep(800);
                    Console.Clear();
                    break;
            }
        }
    }
}
