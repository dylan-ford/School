Lecture
- ![[Pasted image 20261006233146.png]]
	- We can stack vectors via rbind() (bind by row, top to bottom)
		- mat1 <- rbind(c(1, 2, 3, 4), c(5, 6, 7, 8), c(9, 10, 11, 12))
		- mat1 <- cbind(c(1, 2, 3, 4), c(5, 6, 7, 8), c(9, 10, 11, 12)) - bind by column, left to right
- Navigating matrices
	- mat1[1, 3] returns first row, third column
	- mat1[2, ] returns second row, all columns
	- mat[ , 3] returns all rows, third column
	- can be used with <- to modify values
		- mat1[2, ] <- mat1[2, ] + 4 results in each item in row 2 increasing by 4
	- we can assign names for the rows and columns of a matrix:
		- rownames(mat1) <- c("Row1", "Row2", "Row3")
		- colnames(mat1) <- c("Col1", "Col2", "Col3", "Col4")
- Data frame:
	- Matrix where each column/row can contain various data types
		- Do have the restriction where all columns must have the same length
	- created with data.frame()
	- Tibbles are created with tibble()
		- Tibbles are data frames with nicer defaults
	- summary() gets a statistical overview of each variable
- Lists:
	- like a vector but each of its components can be items of different data types
	- can use str() to look at structure of any container object
- T test
	- t.test(extra ~ group, data = sleep)
		- 'extra' is the outcome variable (y) 'group' is the predictor variable (x)
		- ~ tells R we are giving it a formula
Ch 12
Ch 13
Ch 14
Ch 15
Ch 16
Ch 17
Ch 18
Ch 19