QUESTION:-  
PROBLEM 11A  
A sequence a0, a1, ..., at - 1 is called increasing if ai - 1 < ai for each i: 0 < i < t.  
You are given a sequence b0, b1, ..., bn - 1 and a positive integer d.  
In each move you may choose one element of the given sequence and add d to it.  
What is the least number of moves required to make the given sequence increasing?  

ANSWER:-  

#include <iostream>  
#include <vector>  
using namespace std;  
int main() {    
    int n, d;  
    cin >> n >> d;  
    vector<long long> b(n);  
    for(int i = 0; i < n; i++) {  
        cin >> b[i];  
    }  
    long long ans = 0;  
    for(int i = 1; i < n; i++) {    
        if(b[i] <= b[i-1]) {  
            long long moves = (b[i-1] - b[i]) / d + 1;  
            b[i] += moves * d;  
            ans += moves;  
        }  
    }  
    cout << ans << endl;  
    return 0;  
}  

<img width="1174" height="90" alt="image" src="https://github.com/user-attachments/assets/045675d4-a13e-44f9-a00c-07c61b47ba07" />



