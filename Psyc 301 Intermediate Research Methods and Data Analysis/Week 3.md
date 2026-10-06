Lecture
- nominal - categories
- ordinal - categorical variable with order
- interval - continuous number - true 0
- ratio - hard cap at 0 = absence of trait

- If you make an qmd to export to word, and the person you send the word to edits it, those changes are only saved locally
- in .qmd files, rode code lives inside r chunks(triple backtick + {} + triple backtick)
- you can name chunks of code, which allows us to navigate to specific code chunks (no spaces in names, and do not reuse names)
	- ![[Pasted image 20261006004645.png]]
	- can give code chunks flags: '# | flagname'. These flags signal to r to perform some function as the code executes
		- the 'echo' flag shows the executed code as well as the output
		- 'eval' flag tells R whether or not to run the code chunk (useful if it installs packages and you dont want it to run in the future)
- variable types
	- dbl = double
	- ord = ordinal: R knows these are categorical
- Basic R chunks:
	- mean(diamonds$carat)
		- the mean function takes a data set as a variable, with a parameter to return the mean of. In this case its returning the mean of the column 'carat' in the diamonds data set
	- functions can be nested:
		- round(x = mean(diamonds$carat), digits = 3) 
			- or round(mean(diamonds$carat), 3)
		- rounds the output to 3 digits
- Pipe | character:
	- means: when this, then do that:
		- diamonds$carat |> mean() |> round(3) - will execute the following code in succession
	- makes it easier to read rather than reading inside out of brackets
- Vectors
	- ![[Pasted image 20261006012900.png]]
		- specifying L after a number denotes to R that its an integer
- Scalar: technically a vector with a size of 1 - just a variable

Ch 5
Ch 20