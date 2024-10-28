## Visualize all Statistical measures (Mean, Mode, Median, Range, Inter Quartile Range etc., using  Histograms, Boxplots and Scatter Plots)

#### Summary Statistics Functions in R

##### Commands for Single Value Results
These commands produce a single value as a result and can often handle `NA` values with the `na.rm = TRUE` option.

- **`max(x, na.rm = FALSE)`**  
  Shows the maximum value of `x`. By default, `NA` values are not removed, and `NA` is considered the largest value unless `na.rm = TRUE` is specified.

- **`min(x, na.rm = FALSE)`**  
  Shows the minimum value in the vector `x`. If `x` contains `NA` values, the result will be `NA` unless `na.rm = TRUE` is specified.

- **`length(x)`**  
  Returns the length of the vector `x`, including `NA` values. The `na.rm` option is not applicable for this command.

- **`sum(x, na.rm = FALSE)`**  
  Returns the sum of the elements in `x`. If `x` contains `NA` values, the result will be `NA` unless `na.rm = TRUE` is used.

- **`mean(x, na.rm = FALSE)`**  
  Calculates the arithmetic mean of the elements in `x`. If there are `NA` values, the result will be `NA` unless `na.rm = TRUE` is specified.

- **`median(x, na.rm = FALSE)`**  
  Shows the median value of the vector `x`. By default, `NA` values are not removed unless `na.rm = TRUE` is specified.

- **`sd(x, na.rm = FALSE)`**  
  Calculates the standard deviation of `x`. By default, `NA` values are not removed unless `na.rm = TRUE` is specified.

- **`var(x, na.rm = FALSE)`**  
  Shows the variance of `x`. By default, `NA` values are not removed unless `na.rm = TRUE` is specified.

- **`mad(x, na.rm = FALSE)`**  
  Calculates the median absolute deviation of `x`. By default, `NA` values are not removed unless `na.rm = TRUE` is specified.

  ##### Commands for Multiple Value Results in R

These commands produce multiple values as outputs, providing summaries or transformations of datasets.

- **`log(dataset)`**  
  Computes the natural logarithm for each element in `dataset`, returning a vector of log-transformed values.

- **`summary(dataset)`**  
  Generates a summary of `dataset`, including basic statistics like the minimum, 1st quartile, median, mean, 3rd quartile, and maximum values.

- **`quantile(x, probs = seq(0, 1, 0.25), na.rm = FALSE, names = TRUE)`**  
  Calculates specified quantiles of `x`. By default, it returns the 0%, 25%, 50%, 75%, and 100% quantiles. 

  **Additional Parameters:**
  - **`probs`**: A numeric vector specifying the quantiles to be returned, e.g., `probs = c(0.1, 0.5, 0.9)` for the 10th, 50th, and 90th percentiles.
  - **`na.rm`**: If `TRUE`, `NA` values are removed from `x` before computation.
  - **`names`**: If `TRUE`, displays percentage labels for quantiles; set to `FALSE` to suppress labels.
```
quantile(x, probs = seq(0, 1, 0.25), na.rm = FALSE, names = TRUE) 
```
### Data Visualization
A data visualization is a method of representing data in a graphical format, useful both in 
communicating results of analyses and in exploring datasets to determine what analyses might be 
appropriate. 

#### Histograms

A histogram contains a rectangular area to display the statistical information which is 
proportional to the frequency of a variable and its width in successive numerical intervals.

Syntax: hist(v, main, xlab, xlim, ylim, breaks, col, border) 

##### Parameters for Histogram Plotting in R

When creating histograms in R, several parameters allow customization of the chart's appearance and behavior.

- **`v`**  
  Contains the numerical values used to create the histogram. This data is the basis for the distribution displayed in the histogram.

- **`main`**  
  Sets the main title of the chart.

- **`col`**  
  Specifies the color of the bars in the histogram.

- **`xlab`**  
  Sets the label for the horizontal (x) axis.

- **`border`**  
  Defines the border color for each bar in the histogram.

- **`xlim`**  
  Specifies the range of values for the x-axis, allowing for control over the displayed data range.

- **`ylim`**  
  Specifies the range of values for the y-axis.

- **`breaks`**  
  Controls the width of each bar, influencing the number of bars in the histogram. It can be specified as an integer (number of bins) or a vector of break points.

**Example Usage:**

```
# Creating a histogram with customized parameters
hist(v, 
     main = "Histogram Title", 
     col = "blue", 
     xlab = "X-Axis Label", 
     border = "black", 
     xlim = c(0, 100), 
     ylim = c(0, 30), 
     breaks = 10)

```
```
iris
view(iris)
slength<-iris$Sepal.Length 
hist (slength) 
```
![histogram](https://github.com/user-attachments/assets/6474eaba-1d65-484a-bf0d-c7f8491009b1)


##### Histogram with parameters
```
hist (slength, main=“Sepal Length from IRIS dataset”, xlab=“Length”, xlim=c(3,10), col=“blue”,freq=FALSE)
```
![Histogram with param](https://github.com/user-attachments/assets/54855e59-fb54-453b-b12b-ca504aaf1d3b)

##### Return value from hist() 
```
hreturn <- hist (slength) 
hreturn 
$breaks
```
[1] 4.0 4.5 5.0 5.5 6.0 6.5 7.0 7.5 8.0 
```
$counts
```
[1]  5 27 27 30 31 18  6  6 
```
$density 
```
[1] 0.06666667 0.36000000 0.36000000 0.40000000 0.41333333 
[6] 0.24000000 0.08000000 0.08000000 
```
$mids
```
 
[1] 4.25 4.75 5.25 5.75 6.25 6.75 7.25 7.75 
```
$xname
``` 
[1] “slength” 
```
$equidist
``` 
[1] TRUE 
```
attr(,”class”)
``` 
[1] “histogram”
 #### Boxplots
```
 data <- mtcars 
view (data)
df <- data [mtcars, c(“mpg”, “gear”)] 
df 
boxplot (mpg ~ gear, data=df, xlab=“Number of gears”, ylab=“Miles per Gallon”, main=“Mileage Data”)

```
![Boxplot-1](https://github.com/user-attachments/assets/5a63dded-baf0-45b3-81d4-ed3c3617d215)\

##### Boxplot with notch
```
 boxplot (mpg ~ gear, data=df, xlab=“Number of gears”, ylab=“Miles per Gallon”, main=“Mileage Data”, notch=TRUE, varwidth=TRUE, col=c(“blue”,”chocolate”,”purple”))
```
![Boxplot-2](https://github.com/user-attachments/assets/3f79975e-d2e8-4242-ac6f-5084c8b10523)


##### Scatter plots 
```
plot (x=df$mpg, y=df$cyl, xlab=“Miles per Gallon”,ylab=“Cylinders”, xlim = c(5,30), ylim = c(2,10), main=“MPG vs Cylinders”)
```

![Scatter](https://github.com/user-attachments/assets/3c891a7c-d4d4-4e6b-8335-265cfc75a49b)

