QUESTION:-
PROBLEM 492A  
Vanya got n cubes. He decided to build a pyramid from them.   
Vanya wants to build the pyramid as follows:  
the top level of the pyramid must consist of 1 cube,  
the second level must consist of 1 + 2 = 3 cubes,   
the third level must have 1 + 2 + 3 = 6 cubes, and so on.   
Thus, the i-th level of the pyramid must have 1 + 2 + ... + (i - 1) + i cubes.    
Vanya wants to know what is the maximum height of the pyramid that he can make using the given cubes.  

ANSWER:-  

#include <iostream>  
using namespace std;    
int main() {  
    int n;  
    cin >> n;  
    int height = 0;  
    int cubes = 0;  
    int level = 1;  
    while (true) {  
        int required = level * (level + 1) / 2;  
        if (cubes + required > n) {  
            break;  
        }  
        cubes += required;  
        height++;  
        level++;  
    }  
    cout << height << endl;    
    return 0;  
}  

<img width="1168" height="80" alt="image" src="https://github.com/user-attachments/assets/b2ba5b0e-4a57-46ea-9e69-fa9d3d1584b7" />
