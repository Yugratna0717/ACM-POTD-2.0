QUESTION:  
PROBLEM 472A  
One way to create a task is to learn from math.   
You can generate some random math statement or modify some theorems to get something new and build a new task from that.  
For example, there is a statement called the "Goldbach's conjecture".   
It says: "each even number no less than four can be expressed as the sum of two primes".   
Let's modify it. How about a statement like that: "each integer no less than 12 can be expressed as the sum of two composite numbers."  
Not like the Goldbach's conjecture, I can prove this theorem.  
You are given an integer n no less than 12, express it as a sum of two composite numbers.  

ANSWER:-  

#include <iostream>  
using namespace std;    
bool isComposite(int n) {  
    if (n < 4) return false;  
    for (int i = 2; i * i <= n; i++) {  
        if (n % i == 0) {  
            return true;    
        }  
    }  
    return false;  
}  
int main() {  
    int n;  
    cin >> n;  
    for (int i = 4; i < n; i++) {  
        int j = n - i;  
        if (isComposite(i) && isComposite(j)) {  
            cout << i << " " << j << endl;  
            return 0;  
        }  
    }  
    return 0;  
}  

<img width="1174" height="84" alt="image" src="https://github.com/user-attachments/assets/bde8e843-2665-4fa5-9eba-bf1d5e128a33" />


