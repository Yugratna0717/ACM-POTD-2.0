QUESTION:-  
PROBLEM 581A  
One day Vasya the Hipster decided to count how many socks he had. It turned out that he had a red socks and b blue socks.  
According to the latest fashion, hipsters should wear the socks of different colors: a red one on the left foot, a blue one on the right foot.  
Every day Vasya puts on new socks in the morning and throws them away before going to bed as he doesn't want to wash them.  
Vasya wonders, what is the maximum number of days when he can dress fashionable and wear different socks, and after that,   
for how many days he can then wear the same socks until he either runs out of socks or cannot make a single pair from the socks he's got.  
Can you help him?  

ANSWER:-  

#include<iostream>  
#include<algorithm>  
using namespace std;  
int main(){  
    int a; // no of red socks  
    int b; // no of blue socks  
    cin >> a >> b;  
    // number of days he can dress fashionably  
    int x = min(a,b); // number of days he can dress fashionably  
    int y = max(a,b);  
    int single = y-x;  
    int days = single/2;  
    cout << x << " " << days << endl;  
    return 0;  
}  

<img width="1173" height="87" alt="image" src="https://github.com/user-attachments/assets/e56a6c28-79df-41cf-9e61-8a4f921a7a9a" />
