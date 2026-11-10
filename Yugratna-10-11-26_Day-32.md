QUESTION:-  
PROBLEM 701A  
There are n cards (n is even) in the deck. Each card has a positive integer written on it.  
n / 2 people will play new card game. At the beginning of the game each player gets two cards, each card is given to exactly one player.  
Find the way to distribute cards such that the sum of values written of the cards will be equal for each player.  
It is guaranteed that it is always possible.  

ANSWER:-  

#include <iostream>  
#include <vector>  
#include <algorithm>  
using namespace std;  
int main() {    
    int n;
    cin >> n;  
    vector<pair<int, int>> a(n);  
    for (int i = 0; i < n; i++) {  
        cin >> a[i].first;  
        a[i].second = i + 1;  
    }  
    sort(a.begin(), a.end());  
    int left = 0;  
    int right = n - 1;  
    while (left < right) {  
        cout << a[left].second << " " << a[right].second << endl;  
        left++;  
        right--;  
    }  
    return 0;  
}  

<img width="1174" height="89" alt="image" src="https://github.com/user-attachments/assets/c5cc3f1e-b453-4f7a-ab65-fc3dc8e974b1" />

