QUESTION:-  
PROBLEM 32B  
Ternary numeric notation is quite popular in Berland. To telegraph the ternary number the Borze alphabet is used.  
Digit 0 is transmitted as «.», 1 as «-.» and 2 as «--».   
You are to decode the Borze code, i.e. to find out the ternary number given its representation in Borze alphabet.  

SOLUTION:  

#include<iostream>  
using namespace std;  
int main(){  
    string borze;  
    cin >> borze;  
    string ans;  
    for(int i=0; i<borze.size(); i++){  
        if(borze[i] == '.') ans.push_back('0');  
        else if(borze[i] == '-'){  
            if(i < borze.size()-1 && borze[i+1] == '.'){  
                ans.push_back('1');  
            }  
            else{  
                ans.push_back('2');  
            }  
            i++;  
        }  
    }  
    cout << ans << endl;  
    return 0;  
}  

<img width="1175" height="84" alt="image" src="https://github.com/user-attachments/assets/3c2e9859-4c98-4a64-bff0-e08e3d0291b9" />


