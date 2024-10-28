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


## R Code Examples

#### Create a vector x with values
```
x = c(8, 6, 7, 5, 3, 0, 9)
x
```
###### Output:
8 6 7 5 3 0 9

#### Create a names vector
```
names = c("Owen", "Luke", "Anakin", "Leia", "Jacen", "Jaina")
names
```
###### Output:
"Owen" "Luke" "Anakin" "Leia" "Jacen" "Jaina"

#### Create a heartDeck vector representing 13 hearts (1) and 39 non-hearts (0)
```
heartDeck = c(rep(1, 13), rep(0, 39))
heartDeck
```
###### Output:
1 1 1 1 1 1 1 1 1 1 1 1 1 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0

#### Create a sequence from 7 to 41 with a step of 1.5
```
y = seq(7, 41, 1.5)
y
```
###### Output:
7.0 8.5 10.0 11.5 13.0 14.5 16.0 17.5 19.0 20.5 22.0 23.5 25.0 26.5 28.0 29.5 31.0 32.5 34.0 35.5 37.0 38.5 40.0

```
# Load built-in dataset 'faithful'
data(faithful)

# Plot a histogram of 'eruptions' column from 'faithful' dataset
hist(faithful$eruptions

# Plot histogram with specific number of bins
hist(faithful$eruptions, n = 15)

# Plot histogram with custom breaks and color
hist(faithful$eruptions, breaks = seq(1.5, 5.25, 0.25), col = "red")

# Plot histogram with relative frequencies, title, and x-axis label
hist(
  faithful$eruptions, freq = F, n = 15,
  main = "Histogram of Old Faithful Eruption Times",
  xlab = "Duration (mins)"
)

```
