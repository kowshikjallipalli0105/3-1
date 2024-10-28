#### Creating the data frame:

```
df <- data.frame (EmpId=c(1,2,3,4,5), 
EmpName=c("Satish","Vani","Ramesh","Praveen","Pallavi"), 
Salary=c(5000,7500,10000,9500,4500),  
StartDate=c("01-11-2013","05-06-2011","21-09-1999","13-09-2005","23-10-2000"))
```
 ##### Printing

 ```
df
```
##### a) Extract two columns using column name. 

```
 df1 <- df [,c(“EmpName”, “Salary”)]
 df1
```
###### Extracting columns using column position 

```
 df2<-df[,c(1,4)] 
df2
```
##### b) Extract the first two rows and then all columns. 

```
 df3<- df[1:2,] 
df3

```

 ##### c) Extract 3rd and 5th row with 2nd and 4th column. 

```
df4<-df[c(3,5),c(2,4)]
df4
```


