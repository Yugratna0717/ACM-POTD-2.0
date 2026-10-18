QUESTION:-  
PROBLEM 266A  
There are n stones on the table in a row, each of them can be red, green or blue.   
Count the minimum number of stones to take from the table so that any two neighboring stones had different colors.   
Stones in a row are considered neighboring if there are no other stones between them.  

SOLUTION:-  

#include <iostream>  
#include <string>  
using namespace std;  
int main() {  
    int n;  
    cin >> n;  
    string s;  
    cin >> s;  
    int cnt = 0;  
    for (int i = 0; i < n - 1; i++) {  
        if (s[i] == s[i + 1]) {  
            cnt++;  
        }  
    }  
    cout << cnt << endl;  
    return 0;  
}  

<img width="1172" height="84" alt="image" src="https://github.com/user-attachments/assets/4ee25473-644e-4baf-822a-3aab52cb8cd3" />

