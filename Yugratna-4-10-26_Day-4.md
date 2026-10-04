QUESTION:-  
PROBLEM 32A  
According to the regulations of Berland's army, a reconnaissance unit should consist of exactly two soldiers.  
Since these two soldiers shouldn't differ much, their heights can differ by at most d centimeters.   
Captain Bob has n soldiers in his detachment. Their heights are a1, a2, ..., an centimeters.   
Some soldiers are of the same height. Bob wants to know, how many ways exist to form a reconnaissance unit of two soldiers from his detachment.  

Ways (1, 2) and (2, 1) should be regarded as different.  

SOLUTION: -   

#include <iostream>  
#include <vector>  
#include <algorithm>  
using namespace std;  

int main() {  
    int n, d;  
    cin >> n >> d;  

    vector<int> arr(n);  
    for (int i = 0; i < n; i++) {  
        cin >> arr[i];  
    }  

    sort(arr.begin(), arr.end());  

    int i = 0;  
    long long ans = 0;  

    for (int j = 0; j < n; j++) {  
        while (arr[j] - arr[i] > d) {  
            i++;  
        }  

        ans += (j - i);  
    }  

    cout << ans * 2 << endl;  

    return 0;  
}  

<img width="1173" height="86" alt="image" src="https://github.com/user-attachments/assets/b27f86ae-8857-4711-8405-a2ebff7f0f01" />


