QUESTION:-  
George has recently entered the BSUCP (Berland State University for Cool Programmers).  
George has a friend Alex who has also entered the university. Now they are moving into a dormitory.  
George and Alex want to live in the same room. The dormitory has n rooms in total.   
At the moment the i-th room has pi people living in it and the room can accommodate qi people in total (pi ≤ qi).    
Your task is to count how many rooms has free place for both George and Alex.  

AMSWER:-  

#include <iostream>  
using namespace std;  
int main() {    
    int n;  
    cin >> n;    
    int count = 0;  
    for(int i = 0; i < n; i++) {  
        int x, y;  
        cin >> x >> y;  
        if(y - x >= 2) {  
            count++;  
        }  
    }  
    cout << count;  
    return 0;  
}  

<img width="1175" height="87" alt="image" src="https://github.com/user-attachments/assets/8532a040-ba9d-4a1d-a366-ac029b959d71" />
