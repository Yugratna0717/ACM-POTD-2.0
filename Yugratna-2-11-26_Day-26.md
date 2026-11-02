QUESTION:-  
PROBLEM 486A  
For a positive integer n let's define a function f:  
f(n) =  - 1 + 2 - 3 + .. + ( - 1)nn  
Your task is to calculate f(n) for a given integer n.  

ANSWER:-  

#include <iostream>  
using namespace std;      
int main() {  
    long long n;  
    cin >> n;  
    if (n % 2 == 0) {  
        cout << n / 2 << endl;  
    } else {  
        cout << -(n + 1) / 2 << endl;  
    }  
    return 0;  
}  

<img width="1170" height="79" alt="image" src="https://github.com/user-attachments/assets/c4a7c755-20fa-476c-a46b-441aeed36254" />
