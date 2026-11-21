QUESTION:-  
PROBLEM 52A  
There is a given sequence of integers a1, a2, ..., an, where every number is from 1 to 3 inclusively.   
You have to replace the minimum number of numbers in it so that all the numbers in the sequence are equal to each other.  

ANSWER:-  

#include<iostream>  
#include<vector>  
#include<algorithm>  
using namespace std;    
int main(){  
    int n;  
    cin >> n;  
    vector<int> arr(n);  
    for(int i=0; i<n; i++){    
        cin >> arr[i];  
    }  
    int cnt1 = 0;    
    int cnt2 = 0;  
    int cnt3 = 0;  
    for(int i=0; i<n; i++){  
        if(arr[i] == 1) cnt1++;  
        else if(arr[i] == 2) cnt2++;  
        else cnt3++;  
    }  
    int maxi = max({cnt1, cnt2, cnt3});  
    cout << n - maxi << endl;  
    return 0;  
}  

<img width="1182" height="80" alt="image" src="https://github.com/user-attachments/assets/383f9f6e-fa21-4bde-a923-16b088d077dd" />


