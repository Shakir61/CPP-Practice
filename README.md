CPP-Practice
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
#include <iostream>
using namespace std;

int main() { 
    double num, sum = 0;
    cout << "Enter numbers to calculate average ( 0 to stop): " << endl;
    int i = 0;
    while(true)
    {
        i++;
        cout << "Enter integer " << i << ": " << endl;
        cin >> num;
        if (num == 0)
        {
            cout << "You have entered a sentinal value i.e. 0" << endl;
            break;
        }
        else 
        {
            sum += num;
        }
    }
    if (i == 0)
    {
        cout << "You have not entered any integers.." << endl;
    }
    else{
       double avg = sum / (i - 1);
       cout << "The number of integers entered are " << i - 1 << "." << endl;
       cout << "The average of given numbers is " << avg << endl;
    }
    return 0;
}
Output:
Enter numbers to calculate average ( 0 to stop): 
Enter integer 1: 
2
Enter integer 2: 
4
Enter integer 3: 
6
Enter integer 4: 
8
Enter integer 5: 
0
You have entered a sentinal value i.e. 0
The number of integers entered are 4.
The average of given numbers is 5



















Output
