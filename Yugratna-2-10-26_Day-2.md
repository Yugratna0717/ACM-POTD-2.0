QUESTION:-  
PROBLEM 16A  
According to a new ISO standard, a flag of every country should have a chequered field n × m, each square should be of one of 10 colours,  
and the flag should be «striped»: each horizontal row of the flag should contain squares of the same colour,   
and the colours of adjacent horizontal rows should be different.   
Berland's government asked you to find out whether their flag meets the new ISO standard.  

SOLUTION :-  

#include <iostream>  
#include <string>  
using namespace std;  

int main() {  
    int n, m;  
    cin >> n >> m;  

    string prev, curr;  
    cin >> prev;  

    for (int j = 1; j < m; j++) {  
        if (prev[j] != prev[0]) {  
            cout << "NO";  
            return 0;  
        }  
    }  

    for (int i = 1; i < n; i++) {  
        cin >> curr;  

        for (int j = 1; j < m; j++) {  
            if (curr[j] != curr[0]) {  
                cout << "NO";  
                return 0;  
            }  
        }  

        if (curr[0] == prev[0]) {  
            cout << "NO";  
            return 0;  
        }  

        prev = curr;  
    }  

    cout << "YES";  
    return 0;  
}
// read each row as a string and check it's characters directly  

<img width="1171" height="80" alt="image" src="https://github.com/user-attachments/assets/597eaac0-24e1-4afb-899a-6940aaa6ffb4" />

