QUESTION:-  
PROBLEM 710A  
The only king stands on the standard chess board.   
You are given his position in format "cd", where c is the column from 'a' to 'h' and d is the row from '1' to '8'.  
Find the number of moves permitted for the king.  

ANSWER:-  

#include <iostream>  
using namespace std;    
int main() {  
    string s;    
    cin >> s;  
    int col = 3;  
    int row = 3;  
    if (s[0] == 'a' || s[0] == 'h') {  
        col = 2;  
    }  
    if (s[1] == '1' || s[1] == '8') {  
        row = 2;  
    }  
    cout << col * row - 1 << endl;  
    return 0;  
}  

<img width="1169" height="84" alt="image" src="https://github.com/user-attachments/assets/756daf32-3107-49cd-8d84-8255b370f889" />

