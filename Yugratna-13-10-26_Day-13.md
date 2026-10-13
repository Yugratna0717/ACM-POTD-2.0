QUESTION:-  
PROBLEM 112A  
Little Petya loves presents. His mum bought him two strings of the same size for his birthday.   
The strings consist of uppercase and lowercase Latin letters. Now Petya wants to compare those two strings lexicographically.       
The letters' case does not matter, that is an uppercase letter is considered equivalent to the corresponding lowercase letter.   
Help Petya perform the comparison.  

SOLUTION:-  

#include <iostream>  
#include <string>  
using namespace std;  
int main() {    
    string str1, str2;  
    cin >> str1 >> str2;  
    for (int i = 0; i < str1.size(); i++) {  
        if (str1[i] >= 'A' && str1[i] <= 'Z') {  
            str1[i] = str1[i] + 32;  
        }  
        if (str2[i] >= 'A' && str2[i] <= 'Z') {  
            str2[i] = str2[i] + 32;  
        }    
    }
    if (str1 > str2) {    
        cout << 1 << endl;  
    }  
    else if (str1 < str2) {  
        cout << -1 << endl;    
    }  
    else {  
        cout << 0 << endl;  
    }  
    return 0;  
}  

<img width="1177" height="82" alt="image" src="https://github.com/user-attachments/assets/078e4587-a2d8-472a-9149-0cfbcf1160e5" />


