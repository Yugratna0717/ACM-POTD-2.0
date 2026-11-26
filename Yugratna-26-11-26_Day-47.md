QUESTION:-  
PROBLEM 275A  

Lenny is playing a game on a 3 × 3 grid of lights. In the beginning of the game all lights are switched on.   
Pressing any of the lights will toggle it and all side-adjacent lights.  
The goal of the game is to switch all the lights off.  
We consider the toggling as follows: if the light was switched on then it will be switched off, if it was switched off then it will be switched on.  
Lenny has spent some time playing with the grid and by now he has pressed each light a certain number of times.  
Given the number of times each light is pressed, you have to print the current state of each light.  

ANSWER:-  

#include <iostream>  
using namespace std;    
int main() {  
    int a[3][3];  
    for(int i = 0; i < 3; i++) {  
        for(int j = 0; j < 3; j++) {  
            cin >> a[i][j];    
        }  
    }  
    int dx[] = {0, 0, 0, -1, 1};  
    int dy[] = {0, -1, 1, 0, 0};  
    for(int i = 0; i < 3; i++) {  
        for(int j = 0; j < 3; j++) {  
            int sum = 0;  
            for(int k = 0; k < 5; k++) {  
                int x = i + dx[k];  
                int y = j + dy[k];  
                if(x >= 0 && x < 3 && y >= 0 && y < 3) {  
                    sum += a[x][y];  
                }  
            }  
            cout << 1 - (sum % 2);  
        }  
        cout << endl;  
    }  
    return 0;  
}  

<img width="1175" height="83" alt="image" src="https://github.com/user-attachments/assets/9aaaefe3-fd34-4210-bb12-47206af03664" />

