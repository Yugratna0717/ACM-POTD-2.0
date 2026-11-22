QUESTION:-
PROBLEM 96A  
Petya loves football very much. One day, as he was watching a football match, he was writing the players' current positions on a piece of paper.  
To simplify the situation he depicted it as a string consisting of zeroes and ones.  
A zero corresponds to players of one team; a one corresponds to players of another team.   
If there are at least 7 players of some team standing one after another, then the situation is considered dangerous.  
For example, the situation 00100110111111101 is dangerous and 11110111011101 is not.   
You are given the current situation. Determine whether it is dangerous or not.  

ANSWER:-  

#include <iostream>  
#include <string>  
using namespace std;    
int main() {    
    string s;  
    cin >> s;  
    int count = 1;  
    for(int i = 1; i < s.length(); i++) {  
        if(s[i] == s[i-1]) {  
            count++;  
        }  
        else {  
            count = 1;  
        }  
        if(count >= 7) {  
            cout << "YES";  
            return 0;  
        }  
    }  
    cout << "NO";  
    return 0;  
}  

<img width="1173" height="79" alt="image" src="https://github.com/user-attachments/assets/46f75b06-a9bd-441f-aafd-a9e67ddd3402" />

