using System;

namespace ConsoleApp1
{
    class Program
    {
        static void Main(string[] args)
        {

            int mymove;


            string[] fieldStates = new string[9];

            for (int i = 0; i < 9; i++)
            {
                fieldStates[i] = " ";
            }


            Console.WriteLine("Welcome to tic-tac-toe!");

            int moves = 9;
            while (moves > 0)
            {
                Console.WriteLine();
                Console.WriteLine($" {fieldStates[0]} | {fieldStates[1]} | {fieldStates[2]}");
                Console.WriteLine("---+---+---");
                Console.WriteLine($" {fieldStates[3]} | {fieldStates[4]} | {fieldStates[5]}");
                Console.WriteLine("---+---+---");
                Console.WriteLine($" {fieldStates[6]} | {fieldStates[7]} | {fieldStates[8]}");

                if (moves % 2 == 1)
                {
                    Console.Write("X's move >");
                }
                else
                {
                    Console.Write("O's move >");
                }

                mymove = Convert.ToInt32(Console.ReadLine());
                while ((mymove < 0 || mymove > 8) || fieldStates[mymove] != " ")
                {
                    Console.WriteLine("Illegal move! Try again.");

                    if (moves % 2 == 1)
                    {
                        Console.Write("X's move >");
                    }
                    else
                    {
                        Console.Write("O's move >");
                    }

                    mymove = Convert.ToInt32(Console.ReadLine());
                }

                if (moves % 2 == 1)
                {
                    fieldStates[mymove] = "X";
                }
                else
                {
                    fieldStates[mymove] = "O";
                }

                moves -= 1;

            }

            Console.WriteLine();
            Console.WriteLine($" {fieldStates[0]} | {fieldStates[1]} | {fieldStates[2]}");
            Console.WriteLine("---+---+---");
            Console.WriteLine($" {fieldStates[3]} | {fieldStates[4]} | {fieldStates[5]}");
            Console.WriteLine("---+---+---");
            Console.WriteLine($" {fieldStates[6]} | {fieldStates[7]} | {fieldStates[8]}");

            Console.WriteLine("Game Over!");


        }



    }
    
}

