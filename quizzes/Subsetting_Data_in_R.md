{quiz, id: Subsetting_Data_in_R, attempts: 10}

## Subsetting_Data_in_R

{choose-answers: 4}
? Which statement would produce a random sample of 10 rows of a data set called `mydata`?

m) `slice_sample(mydata, n = 2)`
m) `tail(mydata, n = 10)`
m) `head(mydata, n = 10)`
o) `filter(mydata, n = 10)`
C) `slice_sample(mydata, n = 10)`
o) `select(mydata, n = 10)`


{choose-answers: 4}
? Which of the following statements is FALSE?

m) A tibble is a fancier version of a data frame.
m) Previewing a tibble prints more information than a data frame (e.g dimensions and classes of each column).
C) The function `tibble(my_data_frame)` access all entries of a dataframe.
m) Dataframes are used to store data in tables.



{choose-answers: 4}
? Which of the following statements would rename the columns `A` and `B` of a dataframe `datadf` to `Adress` and `DoB` and assign the new data frame to one named `new_datadf`?

C) `new_datadf <- datadf %>% rename(Address = A, DoB = B)`
m) `new_datadf <- datadf %>% rename(A = Address, B = DoB)`
m) `new_datadf <- datadf %>% select(Address = A, DoB = B)`
m) `new_datadf <- datadf %>% colnames(Address = A, DoB = B)`


{choose-answers: 4}
?  Which of the following column names use standard names?
m) Number of particles / kg
C) NumberOfParticlesPerKg
m) Number_of_particles/kg
m) Number of particles.kg


{choose-answers: 4}
? How can you rename all your columns at once? 
C) Using the function `rename_with` from the `Tidiverse` package.
m) Using the function `clear_columns` from the `Metaverse` package.
m) Using the function `list` from standard R.
m) Using the function `as.character` from standard R

{choose-answers: 4}
? How can you rename all your columns at once? 

m) Using the function `clear_columns` from the `Metaverse` package.
m) Using the function `list` from standard R.
C) Using the function `rename` from the `Tidiverse` package and listing all the column names.
m) Using the function `as.character` from standard R

{choose-answers: 4}
? How can you rename all your columns at once? 

m) Using the function `clear_columns` from the `Metaverse` package.
C) Using the function `clean_names` from the `janitor` package.
m) Using the function `list` from standard R.
m) Using the function `as.character` from standard R


{choose-answers: 4}
? Which function do you use if you want to subset a column of your tibble as a vector?
m) `filter()`
m) `select()`
m) `mutate()`
C) `pull()`



{choose-answers: 4}
? Which of the following statements subsets the column `Age` of a tibble and return it as a tibble?

m) `pull(mydata, Age)`
m) `filter(mydata, Age)`
C) `select(mydata, Age)`
m) `rename(mydata, Age)`


{choose-answers: 4}
? Which of the following statements subsets all the columns of a tibble but the columns `Age` and `DoB`?

C) `select(mydata, -c(Age, DoB))`
m) `select(mydata, c(Age, DoB))`
m) `pull(mydata, -c(Age, DoB))`
m) `subset(mydata, -c(Age, DoB))`


{choose-answers: 4}
? Which of the following statements subsets all the columns that end with `er` and the rows for which Year >= 2025?

o) `filter(Year>= 2025, ends_with("er"))`
m) `filter(select(mydata, Year >= 2025), ends_with("er"))`
C) `select(filter(mydata, Year >= 2025), ends_with("er"))`
0) `select(pull(mydata, Year >= 2025), ends_with("er"))`
m) `select(Year >= 2025, ends_with("er"))`

{choose-answers: 4}
? Which of the following statements subsets all the rows for which `color` is `red` or `rainbow` and `animal` is `unicorn`?

m) `select(color %in% (red, rainbow) & animal == unicorn)`
C) `filter(color %in% ("red", "rainbow") & animal == "unicorn")`
m) `filter("color" %in% ("red", "rainbow") & "animal" == "unicorn")`
m) `select(color %in% ("red", "rainbow") & animal == "unicorn")`

{choose-answers: 4}
? Which of the following statements gives you the number of rows and columns of a dataframe called `mydata`?

m) `class(mydata)`
o) `str(mydata)`
m) `nrow(mydata)`
C) `dim(mydata)`
o) `colnames(mydata)`


{choose-answers: 4}
? Select the statement that creates a subset called `mydata2` of a dataframe called `mydata` that contains only rows for which the `city` is `New York`,  the `CO2` levels are less than or equal to 1000, and the columns are numeric?

m) `mydata2 <- mydata %>% select(city == "New York" & CO2 <= 1000) %>% filter(where(is.numeric))`
T) `mydata2 <- mydata %>% select(where(is.numeric)) %>% filter(city == "New York" & CO2 <= 1000)`
m) `mydata2 <- mydata %>% filter(city <=1000 & CO2 == "New York") %>% select(where(is.numeric))`
m) `mydata2 <- mydata %>% select(where(is.numeric)) %>% filter(city == "New York" | CO2 <= 1000)`

{choose-answers: 4}
? Select the statement that creates a subset called `mydata2` of a dataframe called `mydata` that contains only rows for which the `city` is `New York`,  the `CO2` levels are less than or equal to 1000, and the columns are numeric?

m) `mydata2 <- mydata %>% select(city == "New York" & CO2 <= 1000) %>% filter(where(is.numeric))`
m) `mydata2 <- mydata %>%  filter(city == "New York" & CO2 <= 1000)`
C) `mydata2 <- mydata %>% filter(city == "New York" & CO2 <= 1000) %>% select(where(is.numeric))`
m) `mydata2 <- mydata %>% select(where(is.numeric)) %>% filter(city == "New York" | CO2 <= 1000)`

{choose-answers: 4}
? Which of the following statements will add a column called `CO2_per_capita` to a dataframe called `mydata`  that computes the CO2 levels per capita (assume there are columns named `CO2` and `population`)?

m) `mydata <- mydata %>% select(C02 / population)`
m) `mydata <- mydata %>% mutate(C02 / population)`
m) `mydata <- mydata %>% mutate(CO2_per_capita = CO2 * population)`
C) `mydata <- mydata %>% mutate(CO2_per_capita = C02 / population)`


{choose-answers: 4}
? Which of the following statements arranges the rows of a dataframe called `mydata` by CO2 levels in descending order and then by year in ascending order?

m) `arrange(mydata, desc(CO2), desc(year))`
m) `arrange(mydata, year, CO2)`
C) `arrange(mydata, desc(CO2), year)`
m) `select(mydata, desc(CO2), year)`


? Which of the following statements that will create a new data frame called `mydata2` from a dataframe called `mydata` by doing: 1) subsetting all the columns but  `experiment`, 2) subseting all rows for which Year >= 2010, 3) adding a new column called `percent_recycled` that computes the percentage of tons of plastic recycled, assuming you have columns named `total_plastic` and `plastic_recycled` and 4) arranging the dataset by the column `percent_recycled`?

C) `mydata2 <- mydata %>% select(!experiment) %>% filter(Year >= 2010) %>% mutate(percent_recycled = 100*(plastic_recycled/total_plastic)) %>% arrange(percent_recycled)`
m) `mydata2 <- mydata %>% select(!experiment) %>% filter(Year >= 2010) %>% arrange(percent_recycled) %>% mutate(percent_recycled = 100*(plastic_recycled/total_plastic))`
m) `mydata2 <- mydata %>% mutate(percent_recycled = plastic_recycled/total_plastic) %>% arrange(percent_recycled) %>% filter(Year >= 2010) %>% select(!percent_recycled)`
m) `mydata2 <- mydata %>% mutate(percent_recycled = plastic_recycled/total_plastic) %>% arrange(percent_recycled)`


{/quiz}