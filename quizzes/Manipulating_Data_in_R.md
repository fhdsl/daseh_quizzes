{quiz, id: Manipulating_Data_in_R, attempts: 10}

## Manipulating_Data_in_R

{choose-answers: 4}
? Which function do you use if you want to transform your data set from having many columns for a single observation to having many rows for a single observation?

m) `left_join()`
C) `pivot_longer()`
m) `pivot_wider()`
m) `inner_join()`


{choose-answers: 4}
? Which function do you use if you want to transform your data set from having multiple rows for a single observation and a single column for the values to having multiple columns with values for a single observation?

m) `left_join()`
m) `pivot_longer()`
C) `pivot_wider()`
m) `inner_join()`

{choose-answers: 4}
? Suppose you have a tibble called `df` with columns `id`, `site`,  `temperature`, `light`, `water`, and `soil_composition`, which of the following statements would transform this into a new tibble called `df2` with columns `id`, `site`, `variable` and `value`, where the `variable` column has rows for all of the columns but `id`, `site` and the `value` column has the corresponding values?

C) `df2 <- df %>% pivot_longer(cols =!c(id, site) names_to = "variable", values_to="value")`
m) `df2 <- df %>% pivot_wider(cols =!c(id, site) names_from = "variable", values_from="value")`
m) `df2 <- df %>% select(cols =!c(id, site)) %>% group_by(temperature, light, water, soil_composition) %>% mutate(value = sum(.n))`
m) `df2 <- df %>% inner_join(by=c(id, site))`

{choose-answers: 4}
? Suppose you have a tibble called `df` with columns 2020, 2021, 2022, 2023, 2024, 2024, `indicator` and `category`. Which command would create a new data frame called `df2` with one row per year and four columns: `Year`, `indicator`, `category` and `Rate`?

C) `df2 <- df %>% pivot_longer(cols=!c(indicator, category), names_to="Year", values_to= "Rate")`
m) `df2 <- df %>% pivot_longer(cols=!c(indicator, category), names_to="Rate", values_to= "Year")`	
m) `df2 <- df %>% pivot_longer(cols=c(indicator, category), names_to="Year", values_to= "Rate")`
m) `df2 <- df %>% pivot_wider(cols=c(indicator, category), names_from="Year", values_from= "category")`


{choose-answers: 4}
? Suppose you have a tibble called `df` with columns `month`, `average_precipitation`, `state`.Which command would create a new tibble df2 with one column per state and one for the month called `month`, and one row for the average precipitation in each month and each state?

m) `df2 <- df %>% pivot_wider(names_from=average_precipitation, values from=state)`
C) `df2 <- df %>% pivot_wider(names_from=state, values from=average_precipitation)`
m) `df2 <- df %>% pivot_longer(names_from=state, values from=average_precipitation)`
m) `df2 <- df %>% pivot_longer(names_to=state, values_to=average_precipitation)`

{choose-answers: 4}
? Suppose you have two datasets A and B. Which command would you use if you want to create a new dataset C that preserves all the rows in dataset A and only adds the matching values in dataset B?

m) `C <- inner_join(A, B)`
C) `C <- left_join(A, B)`
m) `C <- left_join(B, A)`
m) `C <- right_join(A, B)`

{choose-answers: 4}
? Suppose you have two datasets A and B with a common column named `ID`. Which command would you use to join the two data sets and put all the rows and columns in both data sets by the common column?

m) `C <- pivot_longer(A, B, by="ID")`
m) `C <- inner_join(A, B, by="ID")`
m) `C <- left_join(A, B, by="ID")`
C) `C <- full_join(A, B, by="ID")`

? Select the correct statement: what does the `anti_join` function do?

T) It shows the rows that appear in one data set but not the other.
F) It shows the opposite values of a data set.

{choose-answers: 4}
? What does the command `unloadNamespace(mymodule)` do?

m) renames the module `mymodule` to `Namespace`.
m) erases all the functions previously loaded.
C) unloads the module `mymodule` (the opposite of what library(mymodule) does).
m) restarts the R session.

{choose-answers: 4}
? Which of the following statements is equivalent to `left_join(A, B, by=user_name)`?

m) left_join(A, B)
m) left_join(B, A, by=user_name)
C) right_join(B, A, by=user_name)
m) inner_join(A, B, by=user_name)

{/quiz}