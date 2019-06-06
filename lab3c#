using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;

namespace new_V4_p4
{
    class Program
    {
        static void Main(string[] args)
        {
            int N, M, que = 1;
            Console.WriteLine("Введи размер матрицы стрввок*столбцов:");
            N = int.Parse(Console.ReadLine());
            M = int.Parse(Console.ReadLine());
            Matrix mat = new Matrix(N, M); //Создание матрицы А
            Matrix mat2 = new Matrix(N, M);
            Matrix MAT = new Matrix(N, M);

            Console.WriteLine("Заполни матрицу A");
            for (int i = 0; i < N; i++)
            {
                for (int j = 0; j < M; j++)
                {
                    mat[i, j] = Double.Parse(Console.ReadLine());
                }
            }

            Console.WriteLine("Заполни матрицу B");
            for (int i = 0; i < N; i++)
            {
                for (int j = 0; j < M; j++)
                {
                    mat2[i, j] = Double.Parse(Console.ReadLine());
                }
            }

            Console.WriteLine("Заполни матрицу B");
            for (int i = 0; i < N; i++)
            {
                for (int j = 0; j < M; j++)
                {
                    MAT[i, j] = 3*mat[i,j]*mat2[i,j] + mat2[i,j] - mat[i,j];
                }
            }


            Console.WriteLine("------Матрица A ------");
            mat.Print(); //Вывод матрицы A
            Console.WriteLine("------Матрица B ------");
            mat2.Print(); //Вывод матрицы B
            Console.WriteLine("------Матрица C ------");
            MAT.Print();


            Console.ReadKey();
        }
    }

    class Matrix
    {
        private double[,] matrix;
        private int N, M;

        public Matrix()
        {
            matrix = new Double[0, 0];
            this.N = 0;
            this.M = 0;
        }

        public Matrix(int N, int M)
        {
            matrix = new Double[N, M];
            this.N = N;
            this.M = M;
        }

        public int iN
        {
            get
            {
                return N;
            }
            set
            {
                this.N = value;
            }
        }

        public int iM
        {
            get
            {
                return M;
            }
            set
            {
                this.M = value;
            }
        }

        public double this[int x, int y]
        { //Индексатор

            set
            { //Записывает
                if (N >= x && M >= y && x >= 0 && y >= 0)
                {
                    matrix[x, y] = value;
                }
                else
                {
                    Console.WriteLine("Неверно задан номер ячейки");
                    matrix[x, y] = 0;
                }

            }
            get //Считывает
            {
                if (N >= x && M >= y && x >= 0 && y >= 0)
                {
                    return matrix[x, y];
                }
                else
                {
                    Console.WriteLine("Неверно задан номер ячейки");
                    return 0;
                }
            }
        }


        public void Print()
        {
            for (int i = 0; i < N; i++)
            {
                Console.WriteLine();
                for (int j = 0; j < M; j++)
                {
                    Console.Write(" {0} ", matrix[i, j]);
                }

            }
            Console.WriteLine("    ");
        }
    }

}
