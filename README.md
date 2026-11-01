# Challenge8

Problem Statement:
Campus security has divided a high-traffic area into an N × N grid. Each cell stores a risk score from a sensor: 0 means no risk and 100 means the highest risk. You must build a C program called GRIDWATCH that traverses the grid in different ways to identify risky zones and recommend a response. This is not just a maximum-value problem: your solution must correctly analyse rows, columns, diagonals, boundaries, and neighbouring cells.

Algorithm:
1. Start.
2. Read the grid size N and validate that it is between 3 and 6. If invalid, ask again.
3. Read N × N risk scores into a 2D array. Validate each score is between 0 and 100.
4. Read the warning threshold T and validate that it is between 1 and 100.
5. Row Traversal:
•	Calculate the total of each row.
•	Find the highest row total.
•	Display all row numbers having the highest total.
6. Column Traversal:
•	Calculate the total of each column.
•	Find the highest column total.
•	Display all column numbers having the highest total.
7. Full Grid Traversal:
•	Find the highest risk score in the grid.
•	Display all positions where the highest score occurs.
•	Count the cells whose values are greater than or equal to T.
8. Diagonal Traversal:
•	Calculate the main diagonal sum.
•	Calculate the secondary diagonal sum.
•	Check whether both diagonal sums are equal.
•	Display whether the diagonals are balanced or not.
9. Boundary Traversal:
•	Check every cell in the grid.
•	Add the cell value if it belongs to the first row, last row, first column, or last column.
•	Display the boundary total.
10. Neighbour Traversal:
•	Check only the interior cells of the grid.
•	Compare each cell with its top, bottom, left, and right neighbours.
•	If its value is greater than all four neighbours and greater than or equal to T, identify it as a local hotspot.
•	Count and display all hotspots.
•	If no hotspot exists, display a suitable message.
11. Final Decision:
•	If at least one local hotspot exists, display CRITICAL.
•	Otherwise, if the number of cells meeting the threshold is greater than or equal to N, display WARNING.
•	Otherwise, display NORMAL.
12. Stop.
