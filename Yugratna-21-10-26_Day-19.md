QUESTION:-  
PROBLEM 339A  
Xenia the beginner mathematician is a third year student at elementary school. She is now learning the addition operation.  
The teacher has written down the sum of multiple numbers. Pupils should calculate the sum.   
To make the calculation easier, the sum only contains numbers 1, 2 and 3. Still, that isn't enough for Xenia.   
She is only beginning to count, so she can calculate a sum only if the summands follow in non-decreasing order.   
For example, she can't calculate sum 1+3+2+1 but she can calculate sums 1+1+2 and 3+3.  
You've got the sum that was written on the board. Rearrange the summans and print the sum in such a way that Xenia can calculate the sum.  

ANSWER:  


#include <iostream>  
#include <string>  
#include <vector>  
#include <algorithm>  
using namespace std;    
int main() {  
    string str;    
    cin >> str;
    vector<int> arr;  
    int n = str.size();  
    for(int i = 0; i < n; i++) {  
        if(str[i] != '+') {  
            arr.push_back(str[i] - '0');  
        }  
    }  
    sort(arr.begin(), arr.end());  
    int x = arr.size();  
    for(int i = 0; i < x; i++) {  
        cout << arr[i];  
        if(i < x - 1) {  
            cout << '+';  
        }    
    }  
    cout << endl;  
    return 0;    
}  

<img width="1173" height="81" alt="image" src="https://github.com/user-attachments/assets/de172f50-c3cd-4d97-8fb0-141301adb776" />

