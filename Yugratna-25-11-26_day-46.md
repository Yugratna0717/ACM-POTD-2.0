QUESTION:-
PROBLEM 267A  

You've got two numbers. As long as they are both larger than zero, they go through the same operation: subtract the lesser number from the larger one.  
If they equal substract one number from the another. For example, one operation transforms pair (4,17) to pair (4,13), it transforms (5,5) to (0,5).  
You've got some number of pairs (ai, bi). How many operations will be performed for each of them?  

ANSWER:-  

#include <iostream>  
#include <algorithm>  
using namespace std;    
int main() {  
    int n;  
    cin >> n;  
    while (n--) {  
        long long a, b;  
        cin >> a >> b;  
        long long ans = 0;  
        while (a > 0 && b > 0) {  
            if (a > b) {  
                ans += a / b;  
                a %= b;  
            }  
            else {  
                ans += b / a;  
                b %= a;  
            }  
        }  
        cout << ans << endl;  
    }  
    return 0;  
}  

<img width="1176" height="87" alt="image" src="https://github.com/user-attachments/assets/6a6ff785-d0f0-4766-9468-fc880bd104f2" />


