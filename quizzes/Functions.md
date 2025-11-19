{quiz, id: Functions, attempts: 10}

## Functions

? How do you write a function that takes a name `X` as an output and prints "X is cool"?

m) `function(x) {print("x is cool")}`
m) `print("x is cool")`
C) `function(x) {print(paste(x, "is cool", sep=" "))}`
m) `function(x) {mutate(x, " is cool"))}`

{choose-answers: 4}

? How do you write a function called `areaOfaCircle`that takes two numbers `x` and `y`, gives `y` the default value of 3.14, squares the number `x` and multiplies it by `y`?

m) `areaOfaCircle <- function(x) {x * y}`
C) `areaOfaCircle <- function(x, y=3.14) {x^2 * y}`
m) `areaOfaCircle <- function(x, y) {x^2 * y}`
m) `function(x, y) {3.14 * x * y}`



? Which of the following statements will correctly define a function named `count_Word` that takes three arguments: a dataframe `dataset`, a column name `col_name`, and a string `my_str`. The function `count_Word` will then return the number of the rows in that column that contain that string?

m) `count_Word <- function(dataset, col_name, my_str) {dataset %>% filter(stringr::str_detect({{col_name}}, my_str))}`
m) `count_Word <- function(dataset, col_name, my_str) {dataset %>% pull({{col_name}}) %>% stringr::str_detect( my_str)}`
m) `count_Word <- function(dataset, col_name, my_str) {dataset %>% summarize(count())}`
C) `count_Word <- function(dataset, col_name, my_str) {dataset %>% filter({{col_name}} == my_str) %>% count()}`


{choose-answers: 4}

? Suppose you have a tibble called `us_temp` with columns US states, and rows monthly precipitation for each state. Which of the following statements selects the states Washington, Oregon and California and returns a new tibble with the maximum temperature for each of them? 

m) `us_temp %>% select(c(Washington, Oregon,California)) %>% filter(max(na.rm = T))`
m) `us_temp %>% filter(c(Washington, Oregon,California)) %>% mutate(max_temp = max(x, na.rm=T))`
m) `us_temp %>% select(c(Washington, Oregon,California)) %>% mutate(max_temp = max(x, na.rm=T))`
C) `us_temp %>% summarize(across(c(Washington, Oregon,California), function(x) max(x, na.rm = T))`

{choose-answers: 4}

? Which of the following statements would round to two decimal places all numeric columns in a tibble called `mydat`?

m) `mydat %>% filter(is.numeric) %>% round(digits=2)`
m) `mydat %>% round(x, digits=2)`
m) `mydat %>% across(is.numeric, round(x, digits=2))`
C) `mydat %>% select_if(is.numeric) %>% sapply(function(x) round(x, digits=2))`


{choose-answers: 4}

? Suppose you have a tibble called `roaster`. Which of the following statements will group the roaster by grade and compute the standard deviation of all columns ending with `test`?

C) `roaster %>% group_by(grade) %>% summarize(across(ends_with("test"), function(x) sd(x, na.rm = T)))`
m) `roaster %>% group_by(grade) %>% filter(ends_with("test")) %>% mutate(function(x) sd(x, na.rm = T))`
m) `roaster %>% group_by(grade) %>% select(ends_with("test")) %>% mutate(function(x) sd(x, na.rm = T))`
m) `roaster %>% group_by(grade) %>% across(select(ends_with("test"))) %>% summarize()`

{choose-answers: 4}

? Suppose you have a list called `mylist` with 3 different tibbles representing the amount of CO2 levels at  the county, state and national level. Which of the following statements will apply a function returning all the observations above the indoor healthy level of 800 ppm in all tibles at once?

m) `mylist %>% filter(CO2 > 800)`
m) `mylist %>% select(CO2) %>% sapply(function(x) x>800)`
C) `mylist %>% sapply(function(x) filter(CO2>800))`
m) `mylist %>% select(CO2 > 800)`

{choose-answers: 4}

? Suppose you have a list called `soil` with different tibbles representing data of different soil samples and a user-made function called `compute_micro_proportion` computing proportion of micro plastics in a given sample. Which of the following statements will return the proportion of micro plastics for sample in the dataset?

m) `microplastic_proportions <- select(soil) %>% mutate(compute_micro_proportion)`
C) `microplastic_proportions <- sapply(soil, compute_micro_proportion)`
m) `microplastic_proportions <- compute_micro_proportion`
m) `soil %>% compute_micro_proportion`

{choose-answers: 4}

? Which of the following is an anonymous function?

m) `myfun <- function(x){mean(x)}`
m) `myfun <- function_anonymous(x){mean(x)}`
m) `anonymous(x) {mean(x)}`
C) `function(x) {mean(x)}`

{choose-answers: 4}

? Why do you need to use curly braces when defining functions for columns of tibbles?

m) Because it helps clarify which part is the input and which part is the output.
C) Because it helps R understand that it needs to treat that input as the column of the tibble.
m) Because it looks nicer.
m) Because it makes computations faster.


{/quiz}