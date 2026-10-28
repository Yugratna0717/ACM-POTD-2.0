QUESTION:-  
PROBLEM 443A  
Recently, Anton has found a set. The set consists of small English letters.   
Anton carefully wrote out all the letters from the set in one line, separated by a comma.  
He also added an opening curved bracket at the beginning of the line and a closing curved bracket at the end of the line.  
Unfortunately, from time to time Anton would forget writing some letter and write it again.   
He asks you to count the total number of distinct letters in his set.  

ANSWER:-

#include <iostream>  
#include <string>  
#include <set>  
using namespace std;  
int main() {  
    string s;    
    getline(cin, s); // getline is important as it not used it will just take one character  
    set<char> st;  
    for (int i = 0; i < s.size(); i++) {  
        if (s[i] >= 'a' && s[i] <= 'z') {  
            st.insert(s[i]);  
        }  
    }  
    cout << st.size() << endl;  
    return 0;    
}  

<img width="1171" height="79" alt="image" src="https://github.com/user-attachments/assets/4a207d58-4f1f-46b7-930f-d5322665954a" />


