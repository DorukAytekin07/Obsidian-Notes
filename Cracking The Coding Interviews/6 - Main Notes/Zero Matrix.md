2024/10/04
19:17

Status: #adult  
Tags: [[question]] [[matrix]]
# Zero Matrix
# Question

Write an algorithm such that if an element in an MxN matrix is 0, its entire row and column are set to 0

# Solution

in this question we will write zero to whole column and whole row if we find a zero in this spot to solve this you have 2 ways first store the x and y coordinate together or store them separately solving from second way is more convenient for us so i chosen this way

```cpp
#include <iostream>
void nullifyColumn(int matrix[100][100], int column, int size) {
  for (int x = 0; x < size; x++) {
    matrix[x][column] = 0;
  }
}

void nullifyRow(int matrix[100][100], int row, int size) {
  for (int y = 0; y < size; y++) {
    matrix[row][y] = 0;
  }
}

int main(int argc, char *argv[]) {
  int X, Y, z;
  std::cin >> X;
  std::cin >> Y;

  int matrix[100][100];

  int column[Y];
  int row[X];

  for (int y = 0; y < Y; y++) {
    for (int x = 0; x < X; x++) {
      std::cin >> z;
      matrix[x][y] = z;
    }
  }
  
  std::cout << "\n \n \n";

  for (int y = 0; y < Y; y++) {
    for (int x = 0; x < X; x++) {
      std::cout << matrix[x][y] << " ";
    }
    std::cout << "\n";
  }
  
  std::cout << "\n \n \n";

  for (int y = 0; y < Y; y++) {
    for (int x = 0; x < X; x++) {
      if (matrix[x][y] == 0) {
        column[y] = 1;
        row[x] = 1;
      }
    }
  }

  for (int y = 0; y < Y; y++) {
    if (column[y] == 1) {
      nullifyColumn(matrix, y, X);
    }
  }

  for (int x = 0; x < X; x++) {
    if (row[x] == 1) {
      nullifyRow(matrix, x, Y);
    }
  }

  for (int y = 0; y < Y; y++) {
    for (int x = 0; x < X; x++) {
      std::cout << matrix[x][y] << " ";
    }
    std::cout << "\n";
  }

  return 0;
}
```

# References

[[📙 Cracking The Coding Interviews]]