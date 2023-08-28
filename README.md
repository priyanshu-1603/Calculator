#include <iostream>
#include <cmath>

using namespace std;

void add();
void sub();
void multi();
void division();
void sqr();
void srt();
void exitProgram();

int main()
{
    int opr;

    do
    {
        cout << "Select any operation from the C++ Calculator"
             << "\n1 = Addition"
             << "\n2 = Subtraction"
             << "\n3 = Multiplication"
             << "\n4 = Division"
             << "\n5 = Square"
             << "\n6 = Square Root"
             << "\n7 = Exit"
             << "\n\nMake a choice: ";
        cin >> opr;

        switch (opr)
        {
        case 1:
            add();
            break;
        case 2:
            sub();
            break;
        case 3:
            multi();
            break;
        case 4:
            division();
            break;
        case 5:
            sqr();
            break;
        case 6:
            srt();
            break;
        case 7:
            exitProgram();
            break;
        default:
            cout << "Something is wrong..!!";
            break;
        }
        cout << "\n------------------------------\n";
    } while (opr != 7);

    return 0;
}

void add()
{
    int n, sum = 0, number;
    cout << "How many numbers you want to add: ";
    cin >> n;
    cout << "Please enter the numbers one by one:\n";
    for (int i = 0; i < n; i++)
    {
        cin >> number;
        sum += number;
    }
    cout << "\nSum of the numbers = " << sum;
}

void sub()
{
    int num1, num2;
    cout << "\nEnter the First number = ";
    cin >> num1;
    cout << "\nEnter the Second number = ";
    cin >> num2;
    int z = num1 - num2;
    cout << "\nSubtraction of the numbers = " << z;
}

void multi()
{
    int num1, num2;
    cout << "\nEnter the First number = ";
    cin >> num1;
    cout << "\nEnter the Second number = ";
    cin >> num2;
    int mul = num1 * num2;
    cout << "\nMultiplication of the numbers = " << mul;
}

void division()
{
    int num1, num2;
    cout << "\nEnter the First number = ";
    cin >> num1;
    cout << "\nEnter the Second number = ";
    cin >> num2;

    if (num2 != 0)
    {
        int div = num1 / num2;
        cout << "\nDivision of the numbers = " << div;
    }
    else
    {
        cout << "\nCannot divide by zero!";
    }
}

void sqr()
{
    int num1;
    cout << "\nEnter a number to find the Square: ";
    cin >> num1;
    int sq = num1 * num1;
    cout << "\nSquare of " << num1 << " is : " << sq;
}

void srt()
{
    int num1;
    cout << "\nEnter the number to find the Square Root: ";
    cin >> num1;
    if (num1 >= 0)
    {
        double q = sqrt(num1);
        cout << "\nSquare Root of " << num1 << " is : " << q;
    }
    else
    {
        cout << "\nCannot calculate square root of a negative number!";
    }
}

void exitProgram()
{
    cout << "\nExiting the program.\n";
    exit(0);
}
