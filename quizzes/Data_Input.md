{quiz, id: Data_Input, attempts: 10}

## Data_Input quiz

{choose-answers: 4}
? What is the first step of any data analysis project?

m) Make yourself a coffee.
m) Write a protocol of the analysis.
C) Read in a data file in your computer.
m) Plot the data.


? How do you import a data set into R after downloading it in your computer (select all the correct statements)?

T) Manually by navigating to File -> Import Dataset -> From Text (readr) in the top menu in R studio, and clicking "Update" and "Import".
T) By using the function `read_csv` from the Tidiverse package and executing the command `dat <- read_csv(
  file = "path_to_downloaded_data_file.csv").
T) By using the built-in function in R, `read.csv` executing the command `dat <- read.csv(
  file = "path_to_downloaded_data_file.csv") with appropriate options.
F) By opening the file in Excel.
F) By double-clicking in the file after downloading it.

{choose-answers: 4}
? What does the function `head` do?

m) Displays the entire data set.
m) Displays the last 5 rows of the data set.
C) Displays the first 5 rows of the data set.
m) Shows your data in a new tab in a spreadsheet format.

{choose-answers: 4}
? Where do you write static code like scripts and R Markdown documents in R Studio??

m) In the console pane.
m) In the environment pane.
C) In the editor pane.
m) In the help pane.


{choose-answers: 4}
? Where do you test your code in R Studio??

C) In the console pane.
m) In the environment pane.
m) In the editor pane.
m) In the help pane.

? Select all correct answers: How do you look for help in R Studio?

T) In the help pane.
T) In the console pane by typing ?name_of_your_function.
F) In the editor pane
F) In the environment pane.

{choose-answers: 4}
? What does the function `View` do?

C) Shows the data in a spreadsheet format in a separate window.
m) Shows the first few lines of your data set.
m) Shows the columns of your data set.
m) Shows the class of each column of your data set.

{choose-answers: 4}
? What does the function `getwd()` do?

m) Shows your data set in a separate window.
m) Changes your working directory to a different one.
m) Imports a data set.
C) Shows you the current working directory.

{choose-answers: 4}
? Which function do you use to set the working directory in R?

m) `getwd()`
m) `mvwd()`
m) `pwd`
C) `setwd()`

{choose-answers: 4}
? How do you write code chunks in an Rmd file?

m) You just put the code and R Markdown knows how to interpret it.
C) You surround your code by ```{r} CODE GOES HERE ```.
m) You precede your code by `{r}`. 
m) You surround your code by `## {r} ##`.


{/quiz}