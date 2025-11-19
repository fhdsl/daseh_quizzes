{quiz, id: Reproducibility, attempts: 10}

## Reproducibility quiz

{choose-answers: 4}
? What does it mean for your work to be reproducibible?

C) It means that another researcher will obtain the same results using the original data, code and methods in their own computer.
m) It means that you can re-run the code and get the same results in a different R session in the same computer.
m) It means that another researcher will obtain similar results with a different data but the same code and methods.
m) It means that another researcher will obtain the same results if they re-run your code in your computer.


{choose-answers: 4}
? What does it mean for your work to be replicable?
C) It means that a new researcher will derive the same inferences than the ones you got using the same code but new data.
m) It means that you can re-run the code and get the same results in a different R session in the same computer.
m) It means that another researcher will obtain the same results if they run the analysis using the same code and the same data in their own computer.
m) It means that a new researcher will obtain the same results if they re-run your code in your computer.


{choose-answers: 4}
? What should you do if a new researcher tries to reproduce your analysis and fails?
m) Panic, shut everything off and run!
C) Compare your session info with theirs to see if different versions could be the culprit.
m) Repeat the entire analysis in your computer.
m) Better document your code.


{choose-answers: 4}
? Select one reason for why do we recommend using R Markdown for your data science analysis?

C) R Markdown allows you to easily document your work so that others (and your future self) can follow and understand it.
m) R Markdown allows you to put colorful parentheses.
m) R Markdown creates output that is easily shareable.
m) R Markdown allows you to create publication-quality figures.


{choose-answers: 4}
? Why is setting the starting state of the random number generator important? 

m) Because it makes everything look better.
C) Because it allows you to reproduce the exact same results if we use the same seed in another session.
m) Because it allows you to choose your favorite number as the seed.
m) Because it allows you to use the results for other projects.

{choose-answers: 4}
? How do you set the the starting state of the random number generator in R?

m) `set.rng(any_number_you_want_here)`
C) `set.seed(any_number_you_want_here)`
m) `rng(any_number_you_want_here)`
m) `myseed = any_number_you_want_here`


{/quiz}