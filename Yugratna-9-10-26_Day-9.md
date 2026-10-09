QUESTION:-  
PROBLEM 47A  
A triangular number is the number of dots in an equilateral triangle uniformly filled with dots.  
For example, three dots can be arranged in a triangle; thus three is a triangular number.     
The n-th triangular number is the number of dots in a triangle with n dots on a side.  

SOLUTION:-  

#include<iostream>  
using namespace std;  
int main(){  
    int n;    
    cin >> n;  
    int low = 1;  
    int high = 500;  
    while(low <= high){  
       int mid = high - (high - low)/2;  
       int nTerm = mid*(mid+1)/2;  
       if(nTerm == n){  
        cout << "YES" << endl;  
        return 0;  
       }  
       else if(nTerm < n){  
        low = mid + 1;  
       }  
       else{  
        high = mid - 1;  
       }  
    }  
    cout << "NO" << endl;  
    return 0;  
}  

<img width="1178" height="82" alt="image" src="https://github.com/user-attachments/assets/7cb8f70b-db0d-4a6a-8f3f-8690e4790b47" />
