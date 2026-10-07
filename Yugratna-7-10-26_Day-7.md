QUESTION:-  
PROBLEM 38A  
The Berland Armed Forces System consists of n ranks that are numbered using natural numbers from 1 to n, where 1 is the lowest rank and n is the highest rank.  
One needs exactly di years to rise from rank i to rank i + 1. Reaching a certain rank i having not reached all the previous i - 1 ranks is impossible.  
Vasya has just reached a new rank of a, but he dreams of holding the rank of b.  
Find for how many more years Vasya should serve in the army until he can finally realize his dream.  

SOLUTION :-  

#include<iostream>  
#include<vector>  
using namespace std;  
int main(){  
    int n;  
    cin >> n;  
    vector<int> days(n);  
    for(int i=0; i<n-1; i++){  
        cin >> days[i];  
    }  
    int a, b;  
    cin >> a >> b;  
    int rise = 0;  
    if(a == b){  
        cout << 0 <<endl;  
        return 0;    
    }  
    // question follows 1 based indexing  
    for(int i = a-1; i < b-1; i++){    
        rise += days[i];  
    }  
    cout << rise << endl;  
    return 0;    
}  

<img width="1176" height="82" alt="image" src="https://github.com/user-attachments/assets/7cfcc523-6332-4227-b803-82d538f66445" />
