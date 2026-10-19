QUESTION:-  
PROBLEM 271A  
It seems like the year of 2013 came only yesterday.   
Do you know a curious fact? The year of 2013 is the first year after the old 1987 with only distinct digits.  
Now you are suggested to solve the following problem: given a year number,  
find the minimum year number which is strictly larger than the given one and has only distinct digits.  

SOLUTION:-  

#include<iostream>  
#include<set>  
using namespace std;  
bool distinct(int x){  
    set<int> st;  
      while(x > 0){  
        st.insert(x%10);    
        x = x/10;  
    }  
    return st.size() == 4;  
}  
int main(){  
    int n;  
    cin >> n;  
    for(int i = n+1; ; i++){  
        if(distinct(i)){  
            cout << i << endl;  
            return 0;  
        }  
    }  
    return 0;  
}  

<img width="1172" height="81" alt="image" src="https://github.com/user-attachments/assets/39b7d0d1-9390-4ccb-b78e-3f0a347a1488" />


