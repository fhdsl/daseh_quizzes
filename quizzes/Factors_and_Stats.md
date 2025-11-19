{quiz, id: Factors and Stats, attempts: 10}

## Factors and Stats

{choose-answers: 4}
? What is a factor?

m) A numerical vector
m) A date vector
m) A float vector
C) A character vector

{choose-answers: 4}
? What is a good way to think about what factors are?

C) Categorical variables
m) numerical variables
m) vectors with special properties
m) colors of the rainbow.

{choose-answers: 4}
? How can you convert a variable `var` into a factor?

m) `as.character(var)`
m) `as.float(var)`
m) `as.date(var)`
C) `as.factor(var)`

{choose-answers: 4}
?  What is the difference between transforming a variable `var` to a factor with the function `factor` (var1 <- factor(var)) or the function `as_factor` (`var2 <- as_factor(var)`)from the `forcats` package?

m) The factor() function is faster than as_factor().  
C) Levels using the factor() function will be ordered alphanumerically while levels using as_factor() will be ordered by first appearance.
m) Levels using the factor() function cannot be reordered while levels using as_factor() can be reordered.
m) The factor function allows for arranging and plotting data but the as_factor() function does not.

{choose-answers: 4}
?  Select one thing that the `forcats` package allows us to do?
m) Plot categorical data.
m) Check the values of a column using the function `check()`.
C) Reorder a factor based on the values of another variable using the function `fct_order()`.
m) Run statistical analysis on categorical data.

{choose-answers: 4}
? Which of the following statements will adjust the p-values given in a vector named `my_pvals` when testing multiple hypothesis on the same data?

m) `t.test(my_pvals, adjust=TRUE)`
m) `cor(my_pvals, adjust = TRUE)`
C) `p.adjust(my_pvals, method="bonferroni")`
m) `glm(my_pvals, method="bonferroni")`

{choose-answers: 4}
? Suppose you have measurements of temperature recorded in 50 sites in two different dates and store the results in vectors `x1` and `x2`. Which of the following statements would be  appropriate if we want to use a t-test to test for the difference in means between the two groups?

C) `t.test(x1, x2, paired = TRUE)`
m) `t.test(x1, x2)`
m) `cor(x1, x2, use = "complete.obs")`
m) `cor.test(x1, x2)`

{choose-answers: 4}
? Suppose you have a dataframe `mydf` with variables  `latitude`, `monthly_precipitation`, `CO2_emissions` and `temperature`. Which of the following statements would fit a linear model where the outcome is `temperature` and the predictors are  `latitude`, `monthly_precipitation` and `CO2_emissions`?

m) `fit <- glm(latitude + montly_precipitation + CO2_emissions, data = mydf)`
C) `fit <- glm(temperature ~ latitude + montly_precipitation + CO2_emissions, data = mydf)`
m) `fit <- t.test(outcome=temperature, predictors=c(latitude,montly_precipitation, CO2_emissions), data = mydf)`
m) `fit <- glm(outcome=temperature, predictors=c(latitude,montly_precipitation, CO2_emissions), data = mydf)`


{choose-answers: 4}
? Suppose you have a dataframe `mydf` with variables `age`, `number_asthma_episodes`, `CO2_emissions`, `number_of_allergens`. Which of the following statements would fit a linear model where the outcome is `number_asthma_episodes`, the predictors are `age`, `CO2_emissions`, `number_of_allergens` where we assume that there is an interaction between `age` and `number_of_allergens`?

C) `fit <- glm(number_asthma_episodes ~ age + CO2_emissions + number_of_allergens + age * number_of_allergens, data = mydf)`
m) `fit <- glm(number_asthma_episodes ~ age + CO2_emissions + number_of_allergens, data = mydf)`
m) `fit <- glm(number_asthma_episodes ~ age * CO2_emissions * number_of_allergens, data = mydf)`
m) `fit <- glm(number_asthma_episodes ~ age + CO2_emissions + number_of_allergens, interaction=TRUE, data = mydf)`

{choose-answers: 4}
? Which function was introduced in the course to compute odds ratios?
m) `glm()`
m) `glm(family="oddsratios")`
C) `oddsratio()` from the `epitools` package
m) `ER.oddsratio()` from the `OR` package.


{/quiz}