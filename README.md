Final-project
=============

programming excersie 3 
#include <iostream>
#include <string>
#include <fstream>
#include <iomanip>
#include <vector>


using namespace std;

const int NUM_STUDENTS = 29;
const int NUM_QUIZZES = 10;
const int NUM_EXAMS = 5;

void DisplayGrade(int);
int averageQuiz(int, int);
int averageTest(int, int);
int lowestQuizAverage(int, int);
int lowestTestaverage(int, int);




struct Student
{
	string firstName;
	string lastName;
	int quizzes[NUM_QUIZZES];
	int exams[NUM_EXAMS];
};




int main()
{

	Student cop1334[NUM_STUDENTS];

	ifstream inputfile;
	inputfile.open("C:/Users/Mimi/Desktop/simple.txt");


	if (!inputfile)
	{
		cout << " Could not open file." << endl;
		exit(2);
	}



	for (int index = 0; index < NUM_STUDENTS; index++)
	{

		inputfile >> cop1334[index].firstName;

		inputfile >> cop1334[index].lastName;




		for (int i = 0; i < NUM_QUIZZES; i++)
		{

			inputfile >> cop1334[index].quizzes[i];
		}


		for (int i = 0; i < NUM_EXAMS; i++)
		{

			inputfile >> cop1334[index].exams[i];
		}


	}






		inputfile.close();
		system("pause");
		return 0;
}



