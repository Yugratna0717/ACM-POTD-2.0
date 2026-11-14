QUESTION:-  
PROBLEM 710A  
Anton likes to play chess, and so does his friend Danik.    
Once they have played n games in a row. For each game it's known who was the winner — Anton or Danik. None of the games ended with a tie.  
Now Anton wonders, who won more games, he or Danik? Help him determine this.  

ANSWER:-  

#include <iostream>  
#include <string>  
using namespace std;  
int main() {  
    int n;  
    cin >> n;      
    string s;  
    cin >> s;  
    int cnt1 = 0;  
    int cnt2 = 0;  
    for(int i = 0; i < n; i++) {  
        if(s[i] == 'A')  
            cnt1++;  
        else  
            cnt2++;  
    }  
    if(cnt1 > cnt2) {  
        cout << "Anton";    
    }  
    else if(cnt2 > cnt1) {  
        cout << "Danik";  
    }  
    else {  
        cout << "Friendship";  
    }  
    return 0;  
}  

<img width="1175" height="89" alt="image" src="https://github.com/user-attachments/assets/2e12886c-158e-4ac5-bb4e-90991cbb285d" />


  
