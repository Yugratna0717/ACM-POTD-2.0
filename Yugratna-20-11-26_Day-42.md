QUESTION:-  
PROBLEM 44A  
Indian summer is such a beautiful time of the year!   
A girl named Alyona is walking in the forest and picking a bouquet from fallen leaves.  
Alyona is very choosy — she doesn't take a leaf if it matches the color and the species of the tree of one of the leaves she already has.  
Find out how many leaves Alyona has picked  

ANSWER:-  

#include <iostream>  
#include <set>  
#include <string>    
using namespace std;  
int main() {  
    int n;  
    cin >> n;  
    set<pair<string, string>> s;  
    for (int i = 0; i < n; i++) {  
        string tree, color;  
        cin >> tree >> color;  
        s.insert({tree, color});  
    }  
    cout << s.size() << endl;  
    return 0;  
}  

<img width="1177" height="83" alt="image" src="https://github.com/user-attachments/assets/083306c1-e2b5-43fd-a95d-76bcb6e4960b" />

