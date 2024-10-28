A CSV file (Comma Separated Values file) is a type of plain text file that uses specific 
structuring to arrange tabular data. Because it’s a plain text file, it can contain only actual text 
data—in other words, printable ASCII or Unicode characters. Normally, CSV files use a comma 
to separate each specific data value. Here’s what that structure looks like: 
column 1 name, column 2 name, column 3 name 
first row data 1, first row data 2, first row data 3 
second row data 1, second row data 2, second row data 3 
Normally, the first line identifies each piece of data—in other words, the name of a data column. 
Every subsequent line after that is actual data and is limited only by file size constraints.


#### Create a CSV file
Create a CSV file with the following data 
id,name,salary,start_date,dept 
1,Rick,623.3,2012-01-01,IT 
2,Dan,515.2,2013-09-23,Operations 
3,Michelle,611,2014-11-15,IT 
4,Ryan,729,2014-05-11,HR 
5,Gary,843.25,2015-03-27,Finance 
6,Nina,578,2013-05-21,IT 
7,Simon,632.8,2013-07-30,Operations 
8,Guru,722.5,2014-06-17,Finance 

#### Read a CSV file
> **read.csv()**  function to read a CSV file available in your current working directory.

```
data<-read.csv(“input.csv”) 
print(data)
```
#### Analyzing a CSV file 
> **dim()**  See  dimensions  (#  of  rows/cols)  of  dataframe 
> **ncol()**  Returns number of columns in the dataframe 
> **nrow()** Returns number of rows in the dataframe 
> **max()**  Finds the maximum value in the given numeric field 
> **min()**  Finds the minimum value in the given numeric field


```
print (is.data.frame(data)) 
print (dim(data)) 
print (ncol(data)) 
print (nrow(data)) 
print (max(data$salary)
print (min(data$salary)
```

#### Export to CSV file 
In R, we can read data from files stored outside the R environment. We can also write data 
into files which will be stored and accessed by the operating system. R can read and write into 
various file formats like CSV, EXCEL, XML etc. 

##### Setting the working directory 
```
print (getwd())
```
```
setwd (“/MyPersonal/RLab”)
```
```
print (getwd())
```
#### Create a dataframe 

```
Name<-c(“Nahida”, “Boston”, “Hubey”, “Justin”, “Peter”, “Rossow”, “Duminy”, “Roosevelt”) 
Gender<-c(“Female”, “Male”, “Female”, “Male”, “Male”, “Female”, “male”, “Female”) 
Score<-c(89,76,56,76,78,83,95,61) 
Country<-c(“Argentina”, “USA”,”Britain”, “India”, “Japan”, “South Korea”, “Israel”, “UAE”)
```
```
df<-data.frame(Name, Gender, Score, Country)
df

```

####  Export the data frame to a CSV file 
Export this data frame to a CSV file using write.csv function in R. The syntax used to 
export a DataFrame to CSV in R: 
> write.csv (DataFrame, Filename, Sep= “ “, na= “NA”, row.names = FALSE)

```
write.csv (df, “mycsvdata.csv”)
```
