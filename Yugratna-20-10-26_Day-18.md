QUESTION:-  
PROBLEM 281A  
Capitalization is writing a word with its first letter as a capital letter. Your task is to capitalize the given word.  
Note, that during capitalization all the letters except the first one remains unchanged.  

SOLUTION:-  

#include<iostream>  
#include<string>  
#include<cctype>  
using namespace std;  
int main(){  
    string s;  
    cin >> s;  
    s[0] = toupper(s[0]);  
    cout << s << endl;  
    return 0;  
}  

<img width="1182" height="87" alt="image" src="https://github.com/user-attachments/assets/592d3d8c-7e96-4b90-8280-de3ab71ed1a7" />


