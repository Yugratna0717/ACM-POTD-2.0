QUESTION:  
PROBLEM 411A  
You have probably registered on Internet sites many times. And each time you should enter your invented password.   
Usually the registration form automatically checks the password's crypt resistance.  
If the user's password isn't complex enough, a message is displayed.   
Today your task is to implement such an automatic check.  
Web-developers of the company Q assume that a password is complex enough, if it meets all of the following conditions:  
the password length is at least 5 characters;  
the password contains at least one large English letter;  
the password contains at least one small English letter;  
the password contains at least one digit.  
You are given a password. Please implement the automatic check of its complexity for company Q.  

ANSWER:-  

#include <iostream>  
#include <string>  
using namespace std;  
int main() {  
    string s;  
    cin >> s;  
    bool hasUpper = false;    
    bool hasLower = false;  
    bool hasDigit = false;    
    for (int i = 0; i < s.length(); i++) {  
        if (s[i] >= 'A' && s[i] <= 'Z') {    
            hasUpper = true;  
        }  
        else if (s[i] >= 'a' && s[i] <= 'z') {  
            hasLower = true;    
        }  
        else if (s[i] >= '0' && s[i] <= '9') {  
            hasDigit = true;  
        }    
    }  
    if (s.length() >= 5 && hasUpper && hasLower && hasDigit) {  
        cout << "Correct" << endl;  
    }  
    else {  
        cout << "Too weak" << endl;  
    }  
    return 0;  
}  

<img width="1166" height="79" alt="image" src="https://github.com/user-attachments/assets/dca7a47a-7065-4cc3-ab04-0c1b9974d429" />

  

