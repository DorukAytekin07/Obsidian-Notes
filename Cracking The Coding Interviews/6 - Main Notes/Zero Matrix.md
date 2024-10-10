2024/10/04
19:17

Status: #adult  
Tags: [[question]] [[matrix]]
# Zero Matrix
# Question

Write an algorithm such that if an element in an MxN matrix is 0, its entire row and column are set to 0

# Solution

in this question we will write zero to whole column and whole row if we find a zero in this spot to solve this you have 2 ways first store the x and y coordinate together or store them separately solving from second way is more convenient for us so i chosen this way

```Java
void setZeros(int[][] matrix) {
	boolean[] row = new boolean[matrix .length];
	boolean[] column = new boolean[matrix[0].length];
	//II Store the row and column index with value 0
	for (int i= 0; i < matrix.length; i++) {
		for (int j = 0; j < matrix[0].length;j++) {
			if (matrix[i][j] == 0) {
				row[i] = true;
				column[j] = true;
			}
		}
	}
	// Nullify rows 
	for (inti= 0; i < row.length; i++) { 
		if (row[i]) nullifyRow(matrix, i); 
	} 
	// Nullify columns 
	for (int j = 0; j < column.length; j++) { 
		if (column[j]) nullifyColumn(matrix, j); 
		} 
	} 
}
void nullifyRow(int[][] matrix, int row) { 
	for (int j = 0; j < matrix[0].length; j++) { 
		matrix[row][j] = 0; 
	} 
} 

void nullifyColumn(int[][] matrix, int col) { 
	for (int i= 0; i < matrix.length; i++) { 
		matrix[i][col] = 0; 
	} 
}

```

# References

[[📙 Cracking The Coding Interviews]]