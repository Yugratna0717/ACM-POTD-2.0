QUESTION:-  
PROBLEM 16B  
A burglar got into a matches warehouse and wants to steal as many matches as possible.  
In the warehouse there are m containers, in the i-th container there are ai matchboxes, and each matchbox contains bi matches.   
All the matchboxes are of the same size.   
The burglar's rucksack can hold n matchboxes exactly.   
Your task is to find out the maximum amount of matches that a burglar can carry away.  
He has no time to rearrange matches in the matchboxes,   
that's why he just chooses not more than n matchboxes so that the total amount of matches in them is maximal.  

ANSWER:-  

#include <iostream>  
#include <vector>  
#include <algorithm>  
using namespace std;    
int main() {  
    int n, m;  
    cin >> n >> m;  
    vector<pair<int,int>> v;  
    for(int i = 0; i < m; i++) {  
        int a, b;  
        cin >> a >> b;  
        v.push_back({b, a});  
    }  
    // Sort according to matches per box (descending)  
    sort(v.rbegin(), v.rend());  
    long long ans = 0;  
    for(int i = 0; i < m; i++) {  
        int matches = v[i].first;  
        int boxes = v[i].second;  
        int take = min(n, boxes);  
        ans += 1LL * take * matches;  
        n -= take;  
        if(n == 0) {  
            break;  
        }  
    }  
    cout << ans << endl;  
    return 0;  
}  

<img width="1169" height="89" alt="image" src="https://github.com/user-attachments/assets/e01d1b9d-3fba-41bf-96d7-301ad643b722" />

