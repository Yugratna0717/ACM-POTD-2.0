QUESTION:-  
PROBLEM 228A  
Valera the Horse is going to the party with friends. He has been following the fashion trends for a while,     
and he knows that it is very popular to wear all horseshoes of different color.   
Valera has got four horseshoes left from the last year, but maybe some of them have the same color.   
In this case he needs to go to the store and buy some few more horseshoes, not to lose face in front of his stylish comrades.  
Fortunately, the store sells horseshoes of all colors under the sun and Valera has enough money to buy any four of them.   
However, in order to save the money, he would like to spend as little money as possible,  
so you need to help Valera and determine what is the minimum number of horseshoes he needs to buy to wear four horseshoes of different colors to a party.  

SOLUTION:-  

#include<iostream>  
#include <set>  
using namespace std;  
int main(){  
   set<int> st;  
   for(int i=0; i<4; i++){  
      int x;  
      cin >> x;  
      st.insert(x);  
   }  
   cout << 4 - st.size() << endl;  
   return 0;  
}  

<img width="1175" height="83" alt="image" src="https://github.com/user-attachments/assets/99d584b8-5738-4ba7-8634-dda81f2fe448" />


