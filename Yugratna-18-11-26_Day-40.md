QUESTION:-  
PROBLEM 26A    
A number is called almost prime if it has exactly two distinct prime divisors.   
For example, numbers 6, 18, 24 are almost prime, while 4, 8, 9, 42 are not.  
Find the amount of almost prime numbers which are between 1 and n, inclusive.  

ANSWER:-  

#include <iostream>  
using namespace std;  
bool isPrime(int x) {  
    if (x < 2) return false;  
    for (int i = 2; i * i <= x; i++) {  
        if (x % i == 0) {  
              return false;  
        }  
    }  
    return true;  
}  
int main() {  
    int n;  
    cin >> n;  
    int ans = 0;  
    for (int i = 2; i <= n; i++) {  
        int cnt = 0;  
        for (int j = 2; j <= i; j++) {  
            if (i % j == 0 && isPrime(j)) {  
                cnt++;  
            }  
        }  
        if (cnt == 2) {  
            ans++;  
        }  
    }  
    cout << ans << endl;  
    return 0;  
}  

<img width="1174" height="83" alt="image" src="https://github.com/user-attachments/assets/c393c1af-b765-4e40-9648-7993d267db7d" />



