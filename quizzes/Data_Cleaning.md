{quiz, id: Data Cleaning, attempts: 10}

## Data Cleaning

{choose-answers: 4}
? Select the statement that does NOT help you to find missing data:
o) `is.na()`
m) `is.nan()`
C) `is.numeric()`
o) `is.infinite()`
m) `miss_var_summary()`
o) `gg_miss_var()`

{choose-answers: 4}
? The following statements describe potential issues when dealing with missing data. Select the one statement that is not a true issue.

o) Mathematical operations (e.g. sum, min, max) result in `NA` when an NA is present.
m) Elemental arithmetic operations (e.g. computing percentages) will have different results depending on the inclusion or exclusion of `NAs`.
m) Logical evaluations will evaluate an `NA` as a 0.
o) The filter function will remove all the missing values (unless you add the conditional `is.na()`).
C) NAs in a data set are always random.

{choose-answers: 4}
? Assuming you have a dataframe called `mydata` , which of the following statements would replace all the `NA` values with -1 in the column `Emisions`?

m) `mydata <- mydata %>% mutate(is.na(Emissions), -1)`
m) `mydata <- mydata %>% select(Emissions, drop_na(Emissions), -1))`
m) `mydata <- mydata %>% mutate(case_when(Emissions == 'NA' ~ -1))`
C) `mydata <- mydata %>% mutate(Emissions = replace_na(Emissions, -1))`

{choose-answers: 4}
? Assuming you have a dataframe called `mydata` , which of the following statements would replace all the rows having negative value in the column `Temperature` with NA?

m) `mydata <- mydata %>% mutate(Temperature = replace_na(Temperature < 0))`
C) `mydata <- mydata %>% mutate(Temperature = na_if(Temperature < 0))`
m) `mydata <- mydata %>% select(Temperature = na_if(Temperature < 0))`
m) `mydata <- mydata %>% mutate(Temperature = rem_na(Temperature < 0))`


{choose-answers: 4}
? Which of the following statements would remove all the missing values from a data set?

C) `new_data <- mydata %>% drop_na()`
m) `new_data <- mydata %>% drop_na(all)`
m) `new_data <- mydata %>% filter(is.na())`
m) `new_data <- mydata %>% mutate(!is.na)`


{choose-answers: 4}
? Assuming you have a dataframe called `mydata`, which of the following statements would re-code the column `allergens` to `outdoor_allergens` if the values are `pollen`, `mold` or `dust_mites`; `indoor_allergens` if the values are `pet_dander`, `food`, `latex`; and `chemical` for everything else?

C) `mydata <- mydata %>% mutate(allergens = case_when(allergens %in% c("pollen", "mold", "dust_mites") ~ "outdoor_allergens",
													 allergens %in% c("pet_dander", "food", "latex") ~ "indoor_allergens",
													.default = "chemical"))`
m) `mydata <- mydata %>% mutate(allergens = case_when(allergens %in% c("pollen", "mold", "dust_mites") ~ "outdoor_allergens",
													allergens %in% c("pet_dander", "food", "latex") ~ "indoor_allergens",
													allergens == "chemical" ~ "chemical"))`
m) `mydata <- mydata %>% select(allergens = case_when(allergens == c("pollen", "mold", "dust_mites") ~ "outdoor_allergens",
													allergens == c("pet_dander", "food", "latex") ~ "indoor_allergens",
													allergens == "chemical" ~ "chemical"))`
m) `mydata <- mydata %>% mutate(allergens = case_when(allergens == c("pollen", "mold", "dust_mites") ~ "outdoor_allergens",
													allergens == c("pet_dander", "food", "latex") ~ "indoor_allergens",
													.default = SAME))`



questions about working with strings
{choose-answers: 4}
? Assuming you have column named `allergen`, which of the following statements would replace all the occurrences of the string `Smoke` by the word `smoke` in this column?


m) `str_replace(string = allergen, pattern = "S", replacement = "s")`
m) `str_detect(string = allergen, pattern = "S")`
C) `str_replace_all(string = allergen, pattern = "S", replacement = "s")`
m) `str_sub(string = allergen, 1, replacement = "s")`


{choose-answers: 4}
? Assuming you have a dataframe called `mydata`, which of the following statements would subset the data set to obtain only the rows containing the strings `eggs`, `Eggs`, `egg_allergy`, `egg_yolk` or `egg_white` in the column `common_allergens`?

m) `mydata %>% mutate(str_detect(string =  common_allergens, pattern = "^e|^E"))`
C) `mydata %>% filter(str_detect(string = common_allergens, pattern = "^e|^E"))`
m) `mydata %>% filter(common_allergens == str_detect(string = common_allergens, pattern = "^e|^E"))`
m) `mydata %>% filter(common_allergens == "egg*")`


{choose-answers: 4}
? Assuming you have a dataframe called `mydata`, which of the following statements would separate the column `site_number` into two new columns `site` and `number` using the underscore `_` as the separator?
m) `mydata %>% mutate(separate(site_number, (site, number), "_"))`
m) `mydata %>% mutate(site = separate(site_number, (site, number), "_", 1), number= separate(site_number, (site, number), "_", 2))`
m) `mydata %>% separate(site_number, "_", 2)`
C) `mydata %>% separate(site_number, into=c("site", "number"), sep="_")`

{choose-answers: 4}
? Assuming you have a dataframe called `mydata`, which of the following statements would combine the columns `State` and `zipcode` into a single column named `location`?

m) `mydata %>% mutate(unite(State, zipcode, location))`
m) `mydata %>% mutate(location=unite(State, zipcode))`
C) `mydata %>% unite(State, zipcode, col = "location")`
m) `mydata %>% mutate(col1 = State, col2 = zipcode, intol="location")`


{choose-answers: 4}
?  Assume you want to create a string named `myfilename` by combining the string `results` and today's date (given by the function `Sys.Date()`) with no space in between. Which of the following statements would do that?

m) `myfilename <- paste(results, mydate, sep="")`
C) `myfilename <- paste0(results, Sys.Date())`
m) `myfilename <- paste(results, Sys.Date(), sep="_")`
m) `myfilename <- paste0(results, Sys.Date(), sep="_")`


{choose-answers: 4}
? Assume you have a dataframe called `mydata`, which of the following statements would reflect the following operations: 1) split the column called `region` into two a list. 2) Assign the values of the first element of the list to a new column called `country` and the second element of the list to a new column called `state` 3) Drop the column `region`?

C) `mydata %>% mutate(country = unlist(str_split(region, " "))[1], state = unlist(str_split(region, " "))[2]) %>% select(!region)`
m) `mydata %>% select(country = unlist(str_split(region, " "))[1], state = unlist(str_split(region, " "))[2]) %>% mutate(!region)`
m) `mydata %>% mutate(country = str_split(region, " "), state = str_split(region, " ")) %>% select(!region)`
m) `mydata %>% mutate(country = separate(region, " ", 1), state = separate(region, " ", 2)) %>% select(!region)`

{/quiz}