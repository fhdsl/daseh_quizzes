{quiz, id: Data_Summarization and Classes, attempts: 10}

## Data_Summarization and Classes

{choose-answers: 4}
? Assuming you have a dataframe called `mydata` with a column named `population`, which of the following statements would compute the total population?
C) `mydata %>% summarize(total_population = sum(population))`
m) `mydata %>% summarize(total_population = mean(population))`
m) `mydata %>% summarize(total_population = max(population))`
m) `mydata %>% summarize(total_population = sum(county))`


{choose-answers: 4}
? Which function do you use if you want to save a summary statistic as a new column in the original data?

m) `summarize()`
m) `filter`
m) `rename`
C) `mutate()`


{choose-answers: 4}
? Assuming you have a dataframe called `mydata` with columns `temperature`, `month` and `State`, which of the following statements would compute the mean monthly temperature in Illinois?

m) `mydata %>% mutate(mean_temperature = mean(temperature, na.rm=True)`
m) `mydata %>% mutate(mean_temperature = mean(temperature, na.rm=True) & State == "Illinois") %>% group_by(month)` 
C) `mydata %>% filter(State == "Illinois") %>% group_by(month) %>% summarize(mean_temperature = mean(temperature, na.rm=True))`
m) `mydata %>% group_by(month) %>% summarize(mean_temperature = mean(temperature, na.rm=True) & State == "Illinois")`

{choose-answers: 4}
? Assuming you have a dataframe called `mydata` with columns `temperature`, `month` and `State`, which of the following statements would compute the minimum monthly temperatures in each state?

m) `mydata %>% group_by(month) %>% filter(State) %>% summarize(min_temperature = min(temperature, na.rm= TRUE))`
m) `mydata %>% group_by(month) %>% summarize(min_temperature = min(temperature, na.rm= TRUE))`
m) `mydata %>% group_by(State) %>% summarize(min_temperature = min(temperature, na.rm= TRUE))`
C) `mydata %>% group_by(State, month) %>% summarize(min_temperature = min(temperature, na.rm= TRUE))`

{choose-answers: 4}
? Assuming you have a dataframe called `mydata` with columns `CO2`, `month`, `State`, `site` which of the following statements would compute the number of distinct C02 observations by site, month and state?

C) `mydata %>% group_by(State, month, site) %>% distinct(CO2) %>% summarize(n())`
m) `mydata %>% group_by(State, month, site, CO2) %>%  summarize(n())`
m) `mydata %>% group_by(State, month, site) %>% summarize(n())`
m) `mydata %>% group_by(State, month, site) %>% summarize(n()) %>% distinct()`

{choose-answers: 4}
? Which function do you use to determine the class of an object in R?

m) `str()`
m) `as()`
C) `class()`
m) `typeof()`

{choose-answers: 4}
? How can you coerce a numeric vector to become a character vector?

m) Using the `class()` function.
C) Using the `as.character()` function.
m) Using the `date()` function.
m) Using the `as.integer()` function.


{choose-answers: 4}
?  How do you convert a string into a date object?
m) Using the function `mutate_to_date` from `dplyr`.
C) Using any of functions `ymd()`, `mdy()` or `dmy()` from the package `lubridate`.
m) Using the function `as.character()` from base R.
m) Using the function `as.numeric()` from base R.

{choose-answers: 4}
?  Which of the following types of objects would you use to perform operations in several files at once?

m) tibbles.
C) lists 
m) dataframes
m) character vectors

{choose-answers: 4}
?  What is an advantage of using lists in R?
m) Lists can be ordered alphabetically.
m) Lists look nice.
C) Lists allow you to hold different types of objects (e.g. strings and numbers).
m) Lists operate at the bit scale.


{choose-answers: 4}
?  What is an advantage of using lists in R?

m) Lists are easier to use.
m) Lists are faster to use.
m) All the functions from the `dplyr` package can be used in lists.
C) Lists can hold other lists.

{choose-answers: 2}
? Where do indexes start in R?
C) 1
m) 0


{/quiz}

