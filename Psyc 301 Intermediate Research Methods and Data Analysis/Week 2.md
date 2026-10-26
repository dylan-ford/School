Lecture 
- Function: an operation that takes in some variable and returns some output
- c(): combine function; creates a column of variables - takes in comma separated variables
- Assignment:
	- create variable with some name followed by: <- x, where x is the value to assign
	- can use '=' as well but when math is involved repeated glyphs can be confusing. Some packages may not be fully integrated with '=' 
- '#' denotes comments in R
- 'Packages' tab informs you which packages are installed on your system
	- System library: packages that ship with R
	- User library: packages that we've added to R
- install.packages("NAME") programmatically installs the package you request by name
	- installing a package downloads it but does not tell the current script that it requires it; put library(car) command to load the package with its associated dependencies
- ? (followed by function name) in the console shows documentation for that EXACT function 
- ?? is a more loosey regex search 
	- searches your computer for any packages with the name following the ??
- Quarto: R markdown language
	- takes in all of our notes, titles, and formatting, and put them together
	- new file > Quarto document/presentation
- Markdown formatting for plaintext
	- * for italics
	- ** for bold
	- '#' for headings
- LaTeX
	- provides a way of entering math equations in text
	- $ for inline and $ $(beside each other) for centered equations
	- $H_1 \rightarrow \mu \neq 0 produces $H_1 \rightarrow \mu \neq 0$ 
- linear-regression: line through scatter plot points
- multiple regression: plane through multiple dimensions
- main issue of linear regression: lines have to be straight, and straight lines don't always fit data well
	- may go straight for a bit and curve off later - so a straight line wont fit the data well
- Non-linear regression: the shape of the regression line can change to more accurately represent the data
- Document formatting in quarto markdown:
	- * for italics
	- ** for bold
	- *  # for headings
	-  $ for in-line
	- 2x$ for centered equations
	- $H_1 \rightarrow \mu \neq 0$ produces
- The "Pipe" operator: |> reads as "and then" and allows you to daisy chain functions together:
	- x <- c(1,2,3,4)
	- x |>
		- var() |>
		- round(3)
	- this finds the variance of the vector x and rounds that number to 3 decimal places
- Fancy vectors:
	- Factors
		- useful at encoding levels of a categorical variable
		- groups similar values:
		- group1 <- factor(x = c("control", "control", "experimental", "experimental"))
		- output: 
			- [  1] control control experimental experimental4
			- Levels: control experimental
		- group2 <- factor(x = c(0,0,1,1), 
			- labels = c("control", "experimental"))
			- Factor w/ 2 levels "control","experimental": 1 1 2 2
	- Matrices
		- two-dimensional vectors
		- elements must be of the same type
		- mat <- matrix(data = c(1,2,3,4,1
							- 5,6,7,8,2
							- 9,10,11,12), nrow = 3)
		- can stack vectors via rbind() (binds by row, top to bottom)"
			- mat1 <- rbind(c(1, 2, 3, 4), c(5, 6, 7, 8), c(9, 10, 11, 12))
			- mat1
			-      [,1]  [,2]  [,3]  [,4]
			- [1,] 1     2     3    44
			- [2,] 5     6     7    85
			- [3,] 9    10   11   12
		- can stack vectors via cbind(binds by column, left to right)
			- mat2 <- cbind(c(1, 2, 3, 4), c(5, 6, 7, 8), c(9, 10, 11, 12))
			- mat2
			-      [,1]  [,2]  [,3] 
			-  [1,] 1   5   94
			-  [2,] 2   6   105
			-  [3,] 3   7   116
			-  [4,] 4   8   12
- Navigating data frames
	- dim() returns the # of rows and columns

Tutorial
- 


Ch 2
Ch 3
Ch 4
Ch 7
Ch 8