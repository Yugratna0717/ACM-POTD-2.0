QUESTION:-  
PROBLEM 41A  
The translation from the Berland language into the Birland language is not an easy task.   
Those languages are very similar: a Berlandish word differs from a Birlandish word with the same meaning a little: it is spelled (and pronounced) reversely.  
For example, a Berlandish word code corresponds to a Birlandish word edoc.   
However, making a mistake during the "translation" is easy. Vasya translated the word s from Berlandish into Birlandish as t.   
Help him: find out if he translated the word correctly.  

SOLUTION:  

#include<iostream>  
#include<string>  
#include<algorithm>  
using namespace std;  
int main(){  
    string s;  
    cin >> s;  
    string t;  
    cin >> t;  
    reverse(s.begin(), s.end());  
    if(s == t){  
        cout << "YES" << endl;  
        return 0;  
    }  
    cout << "NO" << endl;    
    return 0;  
}  

<img width="1173" height="85" alt="image" src="https://github.com/user-attachments/assets/0fcc71c5-53fe-4238-83a2-fee6e7c62174" />
