QUESTION:-
PROBLEM 615A  
Vasya wants to turn on Christmas lights consisting of m bulbs. Initially, all bulbs are turned off.   
There are n buttons, each of them is connected to some set of bulbs.   
Vasya can press any of these buttons. When the button is pressed, it turns on all the bulbs it's connected to.   
Can Vasya light up all the bulbs?  
If Vasya presses the button such that some bulbs connected to it are already turned on, they do not change their state, i.e. remain turned on.  

ANSWER:-  

#include<iostream>  
#include<vector>  
using namespace std;    
int main(){  
    // input code  
    int n;  
    int m;    
    cin >> n >> m;  
    vector<int> bulbs(m, 0);    
    for(int i=0; i<n; i++){  
        int x;  
        cin >> x;  
        for(int j=0; j<x; j++){  
            int y;  
            cin >> y;  
            bulbs[y-1] = 1;    
        }  
    }  
    // output logic  
    bool flag = true;  
    for(int i=0; i<m; i++){  
        if(bulbs[i] != 1) flag = false;  
    }  
    if(flag){  
        cout << "YES" <<endl;  
        return 0;  
    }  
    cout << "NO" << endl;  
    return 0;  
}  

<img width="1175" height="89" alt="image" src="https://github.com/user-attachments/assets/e122f646-1da7-4218-b352-9287626444be" />
