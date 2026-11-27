QUESTION:-  
PROBLEM 299B  
Ksusha the Squirrel is standing at the beginning of a straight road, divided into n sectors.   
The sectors are numbered 1 to n, from left to right. Initially, Ksusha stands in sector 1.  
Ksusha wants to walk to the end of the road, that is, get to sector n.   
Unfortunately, there are some rocks on the road. We know that Ksusha hates rocks, so she doesn't want to stand in sectors that have rocks.  
Ksusha the squirrel keeps fit. She can jump from sector i to any of the sectors i + 1, i + 2, ..., i + k.  
Help Ksusha! Given the road description, say if she can reach the end of the road (note, she cannot stand on a rock)?  

ANSWER:-  

#include <iostream>  
#include<string>  
using namespace std;  
int main() {  
    int n, k;  
    cin >> n >> k;  
    string s;      
    cin >> s;  
    int prev = 0;  
    for (int i = 1; i < n; i++) {  
        if (s[i] == '.') {  
            if (i - prev > k) {  
                cout << "NO" << endl;  
                return 0;  
            }  
            prev = i;  
        }    
    }  
    cout << "YES" << endl;    
    return 0;  
}  

<img width="1175" height="84" alt="image" src="https://github.com/user-attachments/assets/f9d4cef0-49ff-4416-a364-0fe51f04dc2c" />



