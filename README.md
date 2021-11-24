/*
Создать динамическую вещественную матрицу NxM (N и M ввести с клавиатуры).
Размещение в памяти: все строки матрицы располагаются в едином массиве (один запрос на выделение NxM элементов).
Создать функцию, которая формирует массив результатов - возвращает указатели на нулевые элементы в заштрихованной области .
*/

#include <iostream>
#include <ctime>
#include <windows.h>
#include <ctime>
using namespace std;

void incilization(double** A, int N, int M)
{
	for (int i = 0; i < N; i++)
	{
		for (int j = 0; j < M; j++)
		{
			A[i][j] = (double)(rand() % 3 - 1) / 2;
		}
	}
}
void pechati(double** A, int N, int M)
{
	for (int i = 0; i < N; i++)
	{
		for (int j = 0; j < M; j++)
		{
			if ((A[i][j]) >= 0)
			{
				cout << " ";
			}
			if (i < N / 2)
			{
				SetConsoleTextAttribute(GetStdHandle(STD_OUTPUT_HANDLE), 3);
				cout << A[i][j] << '\t';

				SetConsoleTextAttribute(GetStdHandle(STD_OUTPUT_HANDLE), 7);
			}
			else
			{

				cout << A[i][j] << '\t';

			}
		}
		cout << '\n';
	}
}
int f1(double** A, int N, int M)
{/*

Создать динамическую вещественную матрицу NxM (N и M ввести с клавиатуры).

Размещение в памяти: все строки матрицы располагаются в едином массиве (один запрос на выделение NxM элементов).

Создать функцию, которая формирует массив результатов - возвращает указатели на нулевые элементы в заштрихованной области .

*/



#include <iostream>

#include <ctime>

#include <windows.h>

#include <ctime>

using namespace std;



void incilization(double** A, int N, int M)

{

	for (int i = 0; i < N; i++)

	{

		for (int j = 0; j < M; j++)

		{

			A[i][j] = (double)(rand() % 3 - 1) / 2;

		}

	}

}

void pechati(double** A, int N, int M)

{

	for (int i = 0; i < N; i++)

	{

		for (int j = 0; j < M; j++)

		{

			if ((A[i][j]) >= 0)

			{

				cout << " ";

			}

			if (i < N / 2)

			{

				SetConsoleTextAttribute(GetStdHandle(STD_OUTPUT_HANDLE), 3);

				cout << A[i][j] << '\t';



				SetConsoleTextAttribute(GetStdHandle(STD_OUTPUT_HANDLE), 7);

			}

			else

			{



				cout << A[i][j] << '\t';



			}

		}

		cout << '\n';

	}
	int sum = 0;
	{
		cout << "Местоположение нуля(ей) в строке ";
		cout << '\n';
		for (int i = 0; i < N; i++)
		{
			if (i < N / 2)
			{
				cout << "Строка " << i + 1 << '\n';
				cout << "Номер в строке элемента равного нулю: ";
				for (int j = 0; j < M; j++)
				{
					if (A[i][j] == 0)
					{
						SetConsoleTextAttribute(GetStdHandle(STD_OUTPUT_HANDLE), 4);
						cout << j + 1 << ' ';
						SetConsoleTextAttribute(GetStdHandle(STD_OUTPUT_HANDLE), 7);
					}
				}
				cout << '\n';
			}

			sum = 0;

		}
	}
	return sum;
}
int main()
{
	setlocale(LC_ALL, "Russian");
	int N, M;
	cout << "Введите число строк" << endl;
	cin >> N;
	cout << "Введите число столбцов" << endl;
	cin >> M;
	cout << endl;
	double** A = (double**)calloc(N, sizeof(double*));
	for (int i = 0; i < N; i++)
		A[i] = (double*)calloc(M, sizeof(double));
	srand(time(0));
	incilization(A, N, M);
	pechati(A, N, M);
	f1(A, N, M);
	SetConsoleTextAttribute(GetStdHandle(STD_OUTPUT_HANDLE), 6);
	return 0;
	SetConsoleTextAttribute(GetStdHandle(STD_OUTPUT_HANDLE), 7);
}
