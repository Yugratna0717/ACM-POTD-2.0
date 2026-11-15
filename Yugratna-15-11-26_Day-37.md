QUESTION:-  
PROBLEM 6A  
Johnny has a younger sister Anne, who is very clever and smart.   
As she came home from the kindergarten, she told his brother about the task that her kindergartener asked her to solve.       
The task was just to construct a triangle out of four sticks of different colours. Naturally, one of the sticks is extra.   
It is not allowed to break the sticks or use their partial length. Anne has perfectly solved this task, now she is asking Johnny to do the same.  
The boy answered that he would cope with it without any difficulty.  
However, after a while he found out that different tricky things can occur.   
It can happen that it is impossible to construct a triangle of a positive area, but it is possible to construct a degenerate triangle.   
It can be so, that it is impossible to construct a degenerate triangle even.   
As Johnny is very lazy, he does not want to consider such a big amount of cases, he asks you to help him.  

ANSWER:-  

#include <iostream>  
#include <algorithm>      
using namespace std;  
int main() {  
    int arr[4];  
    for(int i = 0; i < 4; i++) {    
        cin >> arr[i];  
    }  
    sort(arr, arr + 4);  
    bool segment = false;  
    for(int i = 0; i < 2; i++) {  
        if(arr[i] + arr[i+1] > arr[i+2]) {  
            cout << "TRIANGLE";  
            return 0;  
        }  
        if(arr[i] + arr[i+1] == arr[i+2]) {  
            segment = true;  
        }  
    }  
    if(segment) {  
        cout << "SEGMENT";  
    }  
    else {  
        cout << "IMPOSSIBLE";  
    }  
    return 0;  
}  

<img width="1173" height="85" alt="image" src="https://github.com/user-attachments/assets/7568fbfe-e105-49ba-b79a-67531f558474" />


