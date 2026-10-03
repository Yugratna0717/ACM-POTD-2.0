QUESTION:-  
PROBLEM 22A  
Once Bob needed to find the second order statistics of a sequence of integer numbers.   
Lets choose each number from the sequence exactly once and sort them. The value on the second position is the second order statistics of the given sequence.   
In other words it is the smallest element strictly greater than the minimum. Help Bob solve this problem.  

SOLUTION :-  

#include<iostream>  
#include<vector>  
#include<climits>    
using namespace std;  
int main(){  
    int n;  
    cin >> n;  
    int s = INT_MAX;  
    int ss = INT_MAX;  
    for(int i=0; i<n; i++){  
        int x;  
        cin >> x;  
        if(x < s){  
            ss = s;  
            s = x;  
        }  
        else if(x > s && x < ss){  
            ss = x;  
        }  
    }  
    if(ss == INT_MAX){  
        cout << "NO" << endl;  
        return 0;  
    }  
    else{  
        cout << ss << endl;  
    }  
    return 0;  
}  

<img width="1179" height="85" alt="image" src="https://github.com/user-attachments/assets/aa0ea25f-6f48-48f1-b32f-6ca14a4e6f2c" />
