# CPP-Practice
These are basic C++ practice problems which I solved during my first year in university.
Task # 1: Program to calculate the age of a person.
Code:
#include<iostream>
using namespace std;

void birth_year(int year, int current_year)
{	
	cout << "Enter the year of your birth: " << endl;
	cin >> year;	
	cout << "Enter the current year: " << endl;
	cin >> current_year;
	cout << "Your age is " << current_year - year << ".";
}

int main (){
	int y;
	int cy;
	birth_year(y, cy);
	return 0;
}
Output:
Enter the year of your birth: 
2005
Enter the current year: 
2025
Your age is 20.

Task # 2:  Create a program that calculates the average of a series of numbers entered by the user until they input a sentinel value (e.g., 0). 
Use a while loop to sum the numbers and count how many were entered.

Code:
