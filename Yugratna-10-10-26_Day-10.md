QUESTION:-  
PROBLEM 49A  
Vasya plays the sleuth with his friends.  
The rules of the game are as follows: those who play for the first time, that is Vasya is the sleuth, he should investigate a "crime" and find out what is happening.   
He can ask any questions whatsoever that can be answered with "Yes" or "No".     
All the rest agree beforehand to answer the questions like that: if the question’s last letter is a vowel, they answer "Yes"  
and if the last letter is a consonant, they answer "No". Of course, the sleuth knows nothing about it and his task is to understand that.  
Unfortunately, Vasya is not very smart.   
After 5 hours of endless stupid questions everybody except Vasya got bored.   
That’s why Vasya’s friends ask you to write a program that would give answers instead of them.  
The English alphabet vowels are: A, E, I, O, U, Y  
The English alphabet consonants are: B, C, D, F, G, H, J, K, L, M, N, P, Q, R, S, T, V, W, X, Z  

SOLUTION :   

#include<iostream>  
#include<string>  
using namespace std;  
int main() {  
    string s;    
    getline(cin, s);  

    int n = s.size();  

    int i = n - 2;  // Skip the question mark  

    while (i >= 0 && s[i] == ' ') {  
        i--;  
    }  

    char ch = tolower(s[i]); // to lower helps to reduce the number of conditions from 12 to 6  
  
    if (ch == 'a' || ch == 'e' || ch == 'i' ||  
        ch == 'o' || ch == 'u' || ch == 'y') {  
        cout << "YES" << endl;  
    }  
    else {  
        cout << "NO" << endl;  
    }  

    return 0;  
}  

<img width="1179" height="82" alt="image" src="https://github.com/user-attachments/assets/b9d6b72e-a70b-42a4-9092-342402402cf3" />

