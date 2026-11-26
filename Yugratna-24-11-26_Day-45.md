QUESTION:-  
PROBLEM 263B  
Vasya has found a piece of paper with a coordinate system written on it.   
There are n distinct squares drawn in this coordinate system.  
Let's number the squares with integers from 1 to n.   
It turned out that points with coordinates (0, 0) and (ai, ai) are the opposite corners of the i-th square.  
Vasya wants to find such integer point (with integer coordinates) of the plane, that belongs to exactly k drawn squares.  
We'll say that a point belongs to a square, if the point is located either inside the square, or on its boundary.  
Help Vasya find a point that would meet the described limits.  

ANSWER:-  

#include <iostream>  
#include <algorithm>    
using namespace std;  
int main() {  
    int n, k;  
    cin >> n >> k;  
    int a[55];  
    for (int i = 0; i < n; i++) {  
        cin >> a[i];  
    }  
    sort(a, a + n);  
    if (k == n) {  
        cout << "0 0" << endl;  
        return 0;  
    }  
    int t = a[n - k];  
    if (a[n - k - 1] < t) {  
        cout << t << " 0" << endl;  
    }  
    else {  
        cout << -1 << endl;  
    }  
    return 0;  
}  

<img width="1191" height="80" alt="image" src="https://github.com/user-attachments/assets/ca3259a9-6b91-4a78-b9e7-c944df62614c" />

