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

Task no # 3: Calculator using functions
#include<iostream>
using namespace std;
	
double Addition (double num_1 ,double num_2){	
	return num_1 + num_2;	
}

double Subtraction (double num_1 , double num_2){
	return num_1 - num_2;
}

double Multiplication (double num_1 , double num_2){
	return num_1 * num_2;
}

double Division (double num_1 , double num_2){	
		if (num_2 == 0 || num_1 == 0){
			cout << "Error division is not defined. " << endl;
			return 0;
		}
	return num_1 / num_2;
}
int main(){	
	double num_1;
	double num_2;
	char choice;
	cout << "Enter num_1: " << endl;
        cin >> num_1;
        cout << "Enter num_2: " << endl;
        cin >> num_2;
    cout << "-------------------------------------------" << endl;
	cout << "Select any of the following operations: " << endl;
	cout << "1.Addition" << endl;
	cout << "2.Subtraction" << endl;
	cout << "3.Multiplication" << endl;
	cout << "4.Division" << endl;
	cout << "-------------------------------------------" << endl;
	cout << "Enter your choice: " << endl;
    cin >> choice;
    cout << "-------------------------------------------" << endl;
	switch (choice){
		case '1':
			cout << "Addition: " << Addition(num_1 , num_2) << endl;
			break;
		case '2':
			cout << "Subtraction: " << Subtraction(num_1 , num_2) << endl;
			break;
		case '3':
			cout << "Multiplication: " << Multiplication(num_1 , num_2) << endl;
			break;
		case '4':
			cout << "Division: " << Division(num_1 , num_2) << endl;
			break;
		default:
			cout << "Invalid operations.";
	}
}
Output:
Enter num_1: 
3
Enter num_2: 
4
-------------------------------------------
Select any of the following operations: 
1.Addition
2.Subtraction
3.Multiplication
4.Division
-------------------------------------------
Enter your choice: 
3
-------------------------------------------
Multiplication: 12

Task no # 4:
#include <iostream>
using namespace std;

// (Call by Value)
void value(int valueCopy) {
    valueCopy = 20; 
}

// (Call by Reference)
void change_val(int &valueRef) {
    valueRef = 20; 
}

int main() {
    int original = 10;
    // (Call by Value)
    cout << "Original value: " << original << endl;
    value(original);
    cout << "After calling by value: " << original << endl; // Original unchanged
    cout << endl;
    // (Call by Reference)
    cout << "Original value: " << original << endl;
    change_val(original);
    cout << "After calling by refernce: " << original << endl; // Original changed
    return 0;
}

Output:
Original value: 10
After calling by value: 10

Original value: 10
After calling by refernce: 20

Task no # 5: 
// Write a program that count down a number entered.

#include<iostream>
using namespace std;
int main(){
	int number;
	cout << "Enter a number: " << endl;
	cin >> number;
	cout << "Now I will count down from " << number << " to 0: " << endl;
	while (number >= 0){
		if (number > 0){
		cout << number << ",";
		number--;
	}
	else if (number == 0){
		cout << number << ".";
		number--;
	}	
}
    return 0;
    
}
Output:
Enter a number: 
6
Now I will count down from 6 to 0: 
6,5,4,3,2,1,0.
