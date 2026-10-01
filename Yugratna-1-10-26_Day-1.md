QUESTION:-  
PROBLEM 14A  
A boy Bob likes to draw. Not long ago he bought a rectangular graph (checked) sheet with n rows and m columns. 
Bob shaded some of the squares on the sheet. Having seen his masterpiece, he decided to share it with his elder brother, who lives in Flatland. 
Now Bob has to send his picture by post, but because of the world economic crisis and high oil prices, he wants to send his creation, but to spend as little money as possible. 
For each sent square of paper (no matter whether it is shaded or not) Bob has to pay 3.14 burles. 
Please, help Bob cut out of his masterpiece a rectangle of the minimum cost, that will contain all the shaded squares. The rectangle's sides should be parallel to the sheet's sides.
SOLUTION:-

#include <iostream>
#include <vector>
#include <string>
#include <algorithm>
using namespace std;  

int main() {
    int n, m;  
    cin >> n >> m;  

    vector<string> grid(n);

    for (int i = 0; i < n; i++) {
        cin >> grid[i];
    }

    int minRow = n;
    int maxRow = -1;
    int minCol = m;
    int maxCol = -1;

    for (int i = 0; i < n; i++) {
        for (int j = 0; j < m; j++) {
            if (grid[i][j] == '*') {
                minRow = min(minRow, i);
                maxRow = max(maxRow, i);
                minCol = min(minCol, j);
                maxCol = max(maxCol, j);
            }
        }
    }

    for (int i = minRow; i <= maxRow; i++) {
        for (int j = minCol; j <= maxCol; j++) {
            cout << grid[i][j];
        }
        cout << '\n';
    }

    return 0;
}

<img width="1173" height="95" alt="image" src="https://github.com/user-attachments/assets/95e081ad-2d2b-445c-aaac-e254e3bf6947" />
