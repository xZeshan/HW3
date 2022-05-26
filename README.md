#include <iostream>
using namespace std;

// Function
// Arguments: x and y
// Returns the result of x multiplied with y using the given method
int multiply(int x, int y)
{
    int result=0;
    
    // exit loop if y is 0
    while(y > 0) 
    {
        // If y is a odd number
        if(y%2 == 1)
        {
            // Add x to the result
            result = result + x;
        } 
        
        // Set x = x multiplied with 2
        x = x * 2;
        // Set y = y divided by 2
        y = y / 2;
        
    }
    // return result
    return result;
}

// Driver code
int main()
{
    int n1, n2;
    char choice;
    
    // Repeat the loop until user want to exit the program
    while(true) 
    {
        // Reading first number
        cout << "Enter the first number(positive number): ";
        cin >> n1;
        while(n1 < 0)
        {
            cout << "Enter the first number(positive number): ";
            cin >> n1;
        }
        
        // Reading second number
        cout << "Enter the second number(positive number): ";
        cin >> n2;
        while(n2 < 0)
        {
            cout << "Enter the second number(positive number): ";
            cin >> n2;
        }
        
        // Calling multiply() method
        cout << "Result: (" << n1 << " * "  << n2 << "): " << multiply(n1, n2) << endl;
        
        // Asking user whether he wants to continue or not
        cout << "Do you want to continue (y/n): ";
        cin >> choice;
        if (choice == 'n')
            break;
        
    }

    return 0;
