QUESTION:-  
PROBLEM 678A  
Johny likes numbers n and k very much. Now Johny wants to find the smallest integer x greater than n, so it is divisible by the number k.  

ANSWER:  

#include <iostream>  
using namespace std;  
int main() {  
    int n, k;  
    cin >> n >> k;  
    int x = (n / k + 1) * k;  
    cout << x << endl;  
    return 0;  
}  

<img width="1177" height="81" alt="image" src="https://github.com/user-attachments/assets/2c68e759-2e28-4ae6-95d7-af29d530afd3" />
