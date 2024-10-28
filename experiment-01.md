## R Commands and Examples

| Command                | Description                                                              |
|------------------------|--------------------------------------------------------------------------|
| `help()`               | Obtain documentation for a given R command.                             |
| `example()`            | View some examples on the use of a command.                             |
| `c()`, `scan()`        | Enter data manually into a vector in R.                                 |
| `seq()`                | Make an arithmetic progression vector.                                  |
| `rep()`                | Create a vector of repeated values.                                     |
| `data()`               | Load (often into a data frame) a built-in dataset.                      |
| `view()`               | View dataset in a spreadsheet-type format.                              |
| `str()`                | Display the internal structure of an R object.                          |
| `read.csv()`, `read.table()` | Load an existing data file into a data frame.                |
| `library()`, `require()` | Make an R add-on package available for use.                        |
| `dim()`                | See the dimensions (number of rows and columns) of a data frame.        |
| `length()`             | Get the length of a vector.                                             |
| `ls()`                 | List memory contents.                                                   |
| `rm()`                 | Remove an item from memory.                                             |


### Create a heartDeck vector representing 13 hearts (1) and 39 non-hearts (0)
```heartDeck = c(rep(1, 13), rep(0, 39)) ```
```heartDeck ```
