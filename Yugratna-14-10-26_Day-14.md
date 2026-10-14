QUESTION:-  
PROBLEM 158A  
"Contestant who earns a score equal to or greater than the k-th place finisher's score will advance to the next round,   
as long as the contestant earns a positive score..." — an excerpt from contest rules.  
A total of n participants took part in the contest (n ≥ k), and you already know their scores.   
Calculate how many participants will advance to the next round.  

SOLUTION:  

#include<iostream>  
#include<vector>  
using namespace std;    
int main(){  
    int n;      
    int k;  
    cin >> n >> k;  
    vector<int> arr(n);  
    for(int i=0; i<n; i++){  
        cin >> arr[i];  
    }  
    int cnt = 0;  
    int threshold = arr[k-1];  
    for(int i=0; i<n; i++){  
        if(arr[i] > 0 && arr[i] >= arr[k-1]) cnt++;  
    }  
    cout << cnt << endl;  
    return 0;  
}  

<img width="1178" height="82" alt="image" src="https://github.com/user-attachments/assets/78087418-ce58-4357-8320-336bb06e421a" />
