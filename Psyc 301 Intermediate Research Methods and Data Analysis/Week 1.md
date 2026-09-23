Ch 1
- glimpse() lets you see the attributes of the variables in the dataset
- ggplot() is the function that creates the plot and accepts several arguments:
	- first argument is the dataset to use in the graph
	- second argument: is how the variables in the data will be mapped to aesthetics of the plot 
		- mapping = aes(x = ..., y = ..., colour = ..., )
		- colour variable groups the specified variables by colour
- geom: a geometrical object that a plot uses to represent data 
	- geom_bar() for bar graphs, line charts use geom_line(), boxplots use geom_boxplot(), scatterplots use geom_point()
	- geom() is appended post closing bracket to the ggplot() function with +
	- geom_smooth() appended after the ggplot() creates a visual curve of best fit displaying the relationship between x and y axes
		- geom_smooth(method = "lm") = linear model gives us straight lines
	- geom arguments can also take mapping arguments, which allows for aesthetic mapping at the local level added to those inherited from the global level
		-   geom_point(mapping = aes(color = species)) + ...
		- can also take a "shape" parameter
- labs(): adds text to corresponding variables:
	- labs(
    title = "Body mass and flipper length",
    subtitle = "Dimensions for Adelie, Chinstrap, and Gentoo Penguins",
    x = "Flipper length (mm)", y = "Body mass (g)",
    color = "Species", shape = "Species"
  ) + scale_color_colorblind()

- Categorical variables: can take one small set of variables
	- ex: [ggplot](https://ggplot2.tidyverse.org/reference/ggplot.html)(penguins, [aes](https://ggplot2.tidyverse.org/reference/aes.html)(x = species)) + [geom_bar](https://ggplot2.tidyverse.org/reference/geom_bar.html)() produces a bar chart of number of each species of penguin
		- good practices reorders the bars in order of frequency: [ggplot](https://ggplot2.tidyverse.org/reference/ggplot.html)(penguins, [aes](https://ggplot2.tidyverse.org/reference/aes.html)(x = [fct_infreq](https://forcats.tidyverse.org/reference/fct_inorder.html)(species))) + [geom_bar](https://ggplot2.tidyverse.org/reference/geom_bar.html)()
- Numerical variables: can take a wide range of numerical values, and you can add, subtract, or take averages with those values.
	- Can be continuous or discrete
	- Histograms divides the x-axis into equally spaced bins and uses the height of a bar to display the number of observations that fall into each bin
		- [ggplot](https://ggplot2.tidyverse.org/reference/ggplot.html)(penguins, [aes](https://ggplot2.tidyverse.org/reference/aes.html)(x = body_mass_g)) + [geom_histogram](https://ggplot2.tidyverse.org/reference/geom_histogram.html)(binwidth = 20) [ggplot](https://ggplot2.tidyverse.org/reference/ggplot.html)(penguins, [aes](https://ggplot2.tidyverse.org/reference/aes.html)(x = body_mass_g)) + [geom_histogram](https://ggplot2.tidyverse.org/reference/geom_histogram.html)(binwidth = 2000)
	- Density plot: a smoothed out histogram: [ggplot](https://ggplot2.tidyverse.org/reference/ggplot.html)(penguins, [aes](https://ggplot2.tidyverse.org/reference/aes.html)(x = body_mass_g)) + [geom_density](https://ggplot2.tidyverse.org/reference/geom_density.html)()
- Visualizing relationships:
	- need at least 2 variables mapped to aesthetics of a plot
	- To visualize a reltionship between a categorical and and numerical variables we can use side-by-side box plots
	- ex Distributions of body mass by species: ggplot(penguins, aes(x = species, y = body_mass_g)) + geom_boxplot()
		- density plot: ggplot(penguins, aes(x = body_mass_g, color = species)) +   geom_density(linewidth = 0.75) 
			- the alpha adds transparency to the filled density curves
	- Can stack categorical variables:
		- ggplot(penguins, aes(x = island, fill = species)) + geom_bar()
	- Scatterplots are the best way to visualize relationships between two numerical variables (each at an axis)
- ggsave() saves your plot
	- Generally, however, we recommend that you assemble your final reports using Quarto, a reproducible authoring system that allows you to interleave your code and your prose and automatically include your plots in your write-ups
	- ggplot(mpg, aes(x = class)) + geom_bar() ggplot(mpg, aes(x = cty, y = hwy)) +   geom_point() ggsave("mpg-plot.png")
Ch 6
- 1. Press Cmd/Ctrl + Shift + 0/F10 to restart R.
2. Press Cmd/Ctrl + Shift + S to re-run the current script.

- getwd()
	- `getwd` returns an absolute filepath representing the current working directory of the **R** process; `setwd(dir)` is used to set the working directory to `dir`.
	- #> [1] /Users/hadley/Documents/r4ds

- library(tidyverse)
- ggplot(diamonds, aes(x = carat, y = price)) + 
  geom_hex()
- ggsave("diamonds.png")
- write_csv(diamonds, "data/diamonds.csv")
Ch 27
Ch 28
Ch 29

Prof questions 
- perspective shift that made him like statistics/coding stuff
- high dimensional modelling

Lecture
- linear-regression: line through scatter plot points
- multiple regression: plane through multiple dimensions
- main issue of linear regression: lines have to be straight, and straight lines don't always fit data well
	- may go straight for a bit and curve off later - so a straight line wont fit the data well
- Non-linear regression: the shape of the regression line can change to more accurately represent the data