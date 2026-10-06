QUESTION:-   
PROBLEM 34A  
n soldiers stand in a circle. For each soldier, his height ai is known.   
A reconnaissance unit can be made of such two neighbouring soldiers, whose height difference is minimal, i.e. |ai - aj| is minimal.  
So each of them will be less noticeable with the other. Output any pair of soldiers that can form a reconnaissance unit.  

SOLUTION:-   

#include<iostream>  
#include<vector>  
#include<cmath>    
#include<climits>  
using namespace std;  
int main(){  
    int n;  
    cin >> n;  
    vector<int> soldiers(n);  
    for(int i=0; i<n; i++){  
        cin >> soldiers[i];  
    }  
    int x = 0;  
    int y = 1;  
    int minDiff = INT_MAX;  
    for(int i=0; i < n ; i++){  
        int diff = abs(soldiers[i] - soldiers[(i+1) % n]);  
        if(diff < minDiff){  
            minDiff = diff;  
            x = i;  
            y = (i+1) % n;  
        }  
    }  
    cout << x + 1 << " " << y + 1 << endl;  
    return 0;  
}  

<img width="1176" height="85" alt="image" src="https://github.com/user-attachments/assets/51e971b0-4ef9-47c8-89d4-70040725c29c" />
