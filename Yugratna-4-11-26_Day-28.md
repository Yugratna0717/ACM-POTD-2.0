QUESTION:-  
PROBLEM 520A  
A word or a sentence in some language is called a pangram if all the characters of the alphabet of this language appear in it at least once.  
Pangrams are often used to demonstrate fonts in printing or test the output devices.  
You are given a string consisting of lowercase and uppercase Latin letters.  
Check whether this string is a pangram.  
We say that the string contains a letter of the Latin alphabet if this letter occurs in the string in uppercase or lowercase.  

ANSWER:-  

#include <iostream>  
#include <string>  
#include <map>  
#include <cctype>  
using namespace std;  
int main() {  
    int n;  
    cin >> n;      
    string s;  
    cin >> s;  
    map<char, int> freq;  
    for (int i = 0; i < n; i++) {  
        char ch = tolower(s[i]);  
        freq[ch]++;  
    }  
    if (freq.size() == 26)  
        cout << "YES" << endl;  
    else  
        cout << "NO" << endl;  
    return 0;  
}  

<img width="1171" height="82" alt="image" src="https://github.com/user-attachments/assets/3836182e-6146-4c8a-b780-3cece32d6806" />


