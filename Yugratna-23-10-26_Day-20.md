QUESTION:-  
PROBLEM 386A  
In this problem we consider a special type of an auction, which is called the second-price auction.  
As in regular auction n bidders place a bid which is price a bidder ready to pay.   
The auction is closed, that is, each bidder secretly informs the organizer of the auction price he is willing to pay.   
After that, the auction winner is the participant who offered the highest price.  
However, he pay not the price he offers, but the highest price among the offers of other participants (hence the name: the second-price auction).  
Write a program that reads prices offered by bidders and finds the winner and the price he will pay. Consider that all of the offered prices are different.  

SOLUTION:-  

#include <iostream>  
#include <vector>  
using namespace std;      
int main() {    
    int n;  
    cin >> n;  
    vector<int> arr(n);  
    for(int i = 0; i < n; i++) {  
        cin >> arr[i];  
    }  
    int maxi = 0;  
    for(int i = 0; i < n; i++) {  
        if(arr[i] > arr[maxi]) {  
            maxi = i;  
        }  
    }  
    int max2 = -1;  
    for(int i = 0; i < n; i++) {  
        if(maxi == i) continue;  
        if(arr[i] > max2) {  
            max2 = arr[i];  
        }  
    }  
    cout << maxi + 1 << " " << max2 << endl;  
    return 0;  
}  

<img width="1176" height="88" alt="image" src="https://github.com/user-attachments/assets/bdb178ef-02d7-44ca-83dc-48377a8ac32a" />
