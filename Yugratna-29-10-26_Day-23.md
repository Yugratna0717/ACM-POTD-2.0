QUESTION:-  
PROBLEM 454A  
Twilight Sparkle once got a crystal from the Crystal Mine.   
A crystal of size n (n is odd; n > 1) is an n × n matrix with a diamond inscribed into it.  
You are given an odd integer n.   
You need to draw a crystal of size n.   
The diamond cells of the matrix should be represented by character "D".   
All other cells of the matrix should be represented by character "*".   
Look at the examples to understand what you need to draw.  

ANSWER:-  

#include <iostream>  
using namespace std;    
int main() {      
    int n;  
    cin >> n;  
    for (int i = 0; i < n; i++) {  
        int stars = abs(n / 2 - i);  
        int diamonds = n - 2 * stars;  
        for (int j = 0; j < stars; j++) {    
            cout << "*";  
        }  
        for (int j = 0; j < diamonds; j++) {  
            cout << "D";    
        }
        for (int j = 0; j < stars; j++) {    
            cout << "*";  
        }    
        cout << endl;    
    }  
    return 0;  
}  

<img width="1175" height="85" alt="image" src="https://github.com/user-attachments/assets/4df5f9bd-c167-4bd6-8aab-3368af8e0896" />


