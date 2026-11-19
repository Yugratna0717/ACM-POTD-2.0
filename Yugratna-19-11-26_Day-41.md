QUESTION:-  
PROBLEM 34B  
Once Bob got to a sale of old TV sets. There were n TV sets at that sale.   
TV set with index i costs ai bellars. Some TV sets have a negative price — their owners are ready to pay Bob if he buys their useless apparatus.   
Bob can «buy» any TV sets he wants.   
Though he's very strong, Bob can carry at most m TV sets, and he has no desire to go to the sale for the second time.  
Please, help Bob find out the maximum sum of money that he can earn.  

ANSWER:-  

#include <iostream>  
#include <vector>  
#include <algorithm>  
using namespace std;    
int main() {  
    int n, m;  
    cin >> n >> m;  
    vector<int> arr(n);  
    for(int i = 0; i < n; i++) {   
        cin >> arr[i];  
    }  
    sort(arr.begin(), arr.end());  
    int sum = 0;  
    for(int i = 0; i < m; i++) {  
        if(arr[i] < 0) {  
            sum += arr[i];  
        }  
        else {  
            break;  
        }  
    }  
    cout << -sum << endl;  
    return 0;  
}  

<img width="1176" height="88" alt="image" src="https://github.com/user-attachments/assets/3b200a1b-94ea-4028-94dc-e0a3aa814a97" />



