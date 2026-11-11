QUESTION:-  
PROBLEM 702A  
You are given array consisting of n integers. Your task is to find the maximum length of an increasing subarray of the given array.  
A subarray is the sequence of consecutive elements of the array. Subarray is called increasing if each element of this subarray strictly greater than previous.  

ANSWER:-  

#include <iostream>  
#include <vector>    
using namespace std;  
int main() {  
    int n;  
    cin >> n;  
    vector<int> arr(n);  
    for (int i = 0; i < n; i++) {  
        cin >> arr[i];  
    }  
    int count = 1;  
    int maxLen = 1;  
    for (int i = 1; i < n; i++) {  
        if (arr[i] > arr[i - 1]) {  
            count++;  
        }  
        else {  
            count = 1;  
        }  
        maxLen = max(maxLen, count);  
    }  
    cout << maxLen << endl;  
    return 0;  
}  

<img width="1179" height="95" alt="image" src="https://github.com/user-attachments/assets/3b300513-3aed-4456-b388-5a82b6b65512" />

