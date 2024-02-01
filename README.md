# Task2
    using System;

    class Chess
    {
    static void Main()
    {
        int rows = 8;
        int cols = 8;
        
        int[,] matrix = new int[rows, cols];
        
        int startRow = 0;
        int startCol = 3;
        
        matrix[startRow, startCol] = 2;
        
        int[] rowMoves = {1,2,3,4,5,6,7,8,1,2,3,4,1,2,3,0,0 };
        int[] colMoves = {0,0,0,0,0,0,0,0,1,2,3,4,-1,-2,-3,-1,1 };
        
        for (int i = 0; i < 17; i++)
        {
            int newRow = startRow + rowMoves[i];
            int newCol = startCol + colMoves[i];

           
            if (newRow >= 0 && newRow < rows && newCol >= 0 && newCol < cols)
            {
                matrix[newRow, newCol] = 1;
            }
        }
        
        for (int i = 0; i < rows; i++)
        {
            for (int j = 0; j < cols; j++)
            {
                Console.Write(matrix[i, j] + " ");
            }
            Console.WriteLine();
        }
    }
    }

