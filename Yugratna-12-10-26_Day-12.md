QUESTION:-  
PROBLEM 59A  
Vasya is very upset that many people on the Net mix uppercase and lowercase letters in one word.   
That's why he decided to invent an extension for his favorite browser   
that would change the letters' register in every word so that it either only consisted of lowercase letters or, vice versa, only of uppercase ones.  
At that as little as possible letters should be changed in the word.     
For example, the word HoUse must be replaced with house, and the word ViP — with VIP.   
If a word contains an equal number of uppercase and lowercase letters, you should replace all the letters with lowercase ones.   
For example, maTRIx should be replaced by matrix. Your task is to use the given method on one given word.  

SOLUTION:-  

#include<iostream>  
#include<string>    
#include<cctype>
using namespace std;  
int main(){    
    string str;  
    cin >> str;  
    int upper = 0;  
    int lower = 0;  
    int n = str.size();  
    for(int i=0; i<n; i++){    
        if(isupper(str[i])) upper++;  
        else if(islower(str[i])) lower++;  
    }  
    if(upper > lower){  
        for(int i=0; i<n; i++){  
            if(islower(str[i])) str[i] = toupper(str[i]);  
        }  
    }  
    else{  
        for(int i=0; i<n; i++){  
            if(isupper(str[i])) str[i] = tolower(str[i]);  
        }  
    }  
    cout << str << endl;  
    return 0;  
}  

<img width="1173" height="80" alt="image" src="https://github.com/user-attachments/assets/79e14abb-ce9c-42a9-99ed-a76470687970" />

