{quiz, id: Basic_R, attempts: 10}

## Basic R Quiz

Choose the best answer for the following questions.

{choose-answers: 4}
? Which of the following statements is the correct way to assign the number 10 to a variable called `myvar`?

C) `myvar <- 10`
m) `10 <- myvar`
m) `myvar -> 10`
m) `myvar <- 55`


choose-answers: 4}
? Select the statement that DOES NOT represent a correct way to combine the strings "favorite" and "number" and the number 7? 

m) `c("favorite", "number", 7)`
m) `c(7, "favorite", "number")`
o) `c("number", 7, "favorite")`
o) `c("number", "favorite", 7)`
o) `c(7, "number", "favorite")`
C) `c(favorite, number, 7)`


{choose-answers: 4}
? What would be the value of the result of the following lines of code:
`x <- c(1, 2, 3)`
`y <- 5`
`z <- x + y`
?

C) `c(6, 7, 8)`
m) `c(1, 2, 3, 5)`
m) `c(5, 5, 5)`
m) 11

{choose-answers: 4}
? What is the class of the object `x <- c("fun", "party")`?

o) decimal
o) integer 
C) character
m) numeric
o) Date
m) float


{choose-answers: 4}
? Which of the following statements would assign the value 3.1415 to the variable pi?

o) `pi <- 3`
C) `pi <- 3.1415`
m) `3.1415 <- pi`
m) `pi <- "3.1415"`
o) `3.1415 = pi`

{choose-answers: 2}
? How do you comment code in R?

C) By putting a `#` before the code you want to comment
m) By putting a `%` before the code you want to comment


{choose-answers: 2}
? Is commented code in R executed?

C) Yes
m) No


{choose-answers: 4}
? Assume `x <- c(6, 7, 8 , 9)`. What is the value of `x` in the following line:
x <- x - c(1, 1, 1, 1)?

o) 26
m) `c(6, 7, 8, 9)`
C) `c(5, 6, 7, 8)`
m) `c(7, 8, 9, 10)`
o) 0

{choose-answers: 4}
? Which of the following would create a random sample of size 3 without replacement from the vector `x` ?

m) `y <- sample(x, size = 3, replace = TRUE)`
C) `y <- sample(x, size = 3, replace = FALSE)`
m) `y <- sample(x, size = 1, replace = FALSE)`
m) `y <- seq(from = x, to = 3, by 1)`


{choose-answers: 4}
? Which function can be used to create a long vector that repeats a particular item??

m) `seq()`
m) `sample()`
o) `class()`
C) `rep()`
o) `length()`
o) `str()`

{choose-answers: 4}
? Assume you have a vector `x<- c("work", "your", "magic")`. How would you create a vector that repeats x three times (so that you get  c("work your magic", "work your magic","work your magic"))?

m) `seq(from=1, to=3, by=x)`
C) `rep(x, times = 3)`
m) `rep(x, each = 3)`
m) `str(x, each = 3)`

{choose-answers: 4}
? What is the difference between using the argument `times` or `each` in the function `rep()`?

m) The argument `times` works for numbers while the argument `each` works for strings.
C) The argument `times` will repeat the entire vector the specified of times while the argument `each` will repeat each element of the vector the specified number of times.
m) Nothing, they both do the same thing.
o) The argument times will repeat each element of the vector the specified number of times while the argument each will repeat the entire vector the specified number of times.


{choose-answers: 4}
? Which of the following statements would load the library `ggplot2`?

m) `install.packages('ggplot2')`
m) `help('ggplot2')`
C) `library(ggplot2)`
m) `import(ggplot2)`

{choose-answers: 4}
? Which function would you use to install a new package called `myawesomepackage` in R?

m) `help(myawesomepackage)`
m) `install(myawesomepackage)`
o) `install.packages(myawesomepackage)`
C) `install.packages("myawesomepackage")`
m) `library(myawesomepackage)`
o) `load(myawesomepackage)`

{/quiz}