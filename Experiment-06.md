## Write R Program using ‘apply’ group of functions to create and apply normalization function on each of the numeric variables/columns of iris dataset to transform them into 

## i) 0 to 1 range with min-max normalization. 
 ## ii) a value around 0 with z-score normalization.

 #### Min-Max Normalization
 ```
minmax <- function (x) { (x - min(x)) / (max(x) - min(x)) 
minmax (df$Salary)
```

[1] 0.09090909 0.54545455 1.00000000 0.90909091 0.00000000

#### Z-Score Normalization 

```
 df <- data.frame (EmpId=c(1,2,3,4,5),  
EmpName=c("Satish","Vani","Ramesh","Praveen","Pallavi"), 
Salary=c(5000,7500,10000,9500,4500),  
StartDate = c("01-11-2013", "05-06-2011", "21-09-1999", "13-09-2005", "23-10-2000"))
```

```
df
```
```
m <- mean (df$Salary)

```
```
s <- sd (df$Salary)
```
```
zscores <- (df$Salary - m) / s 

```
```

zscores
```
[1] -0.91452919  0.07952428  1.07357774  0.87476705 -1.11333988






