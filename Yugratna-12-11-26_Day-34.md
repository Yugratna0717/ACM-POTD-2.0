QUESTION:-  
PROBLEM 705A  
Dr. Bruce Banner hates his enemies (like others don't). As we all know, he can barely talk when he turns into the incredible Hulk.   
That's why he asked you to help him to express his feelings.  
Hulk likes the Inception so much, and like that his feelings are complicated.   
They have n layers. The first layer is hate, second one is love, third one is hate and so on...  
For example if n = 1, then his feeling is "I hate it" or if n = 2 it's "I hate that I love it", and if n = 3 it's "I hate that I love that I hate it" and so on.  

ANSWER:-  

#include<iostream>  
#include<string>  
using namespace std;  
int main(){    
    int n;  
    cin >> n;    
    string even = "I hate";  
    string odd = "I love";  
    string ans = "";  
    if(n==1){  
        cout << "I hate it";  
        return 0;    
    }  
    for(int i=0; i<n-1; i++){  
        if(i%2 == 0) ans += "I hate ";  
        else ans += "I love ";  
        ans += "that ";  
    }  
    if(n%2 == 0) ans += "I love ";  
    else ans += "I hate ";  
    ans += "it";  
    cout << ans;  
    return 0;  
}  

<img width="1182" height="85" alt="image" src="https://github.com/user-attachments/assets/3c5014eb-f0b7-46d6-9418-dc5290ffef17" />
