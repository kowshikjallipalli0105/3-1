## Create a data frame with 10 observations and 3 variables and add new rows and columns to it using ‘rbind’ and ‘cbind’ function.

##### 1. Create a new data frame with 5 rows with emp_id, emp_name, salary and start_date as columns 

```
emp.data <- data.frame( 
     emp_id = c (1:5),  
     emp_name = c("Rick","Dan","Michelle","Ryan","Gary"), 
     salary = c(623.3,515.2,611.0,729.0,843.25),  
     start_date = as.Date(c("2012-01-01", "2013-09-23", "2014-11-15", "2014-05-11", 
                            "2015-03-27")), 
     stringsAsFactors = FALSE 
)
```

```
emp.data
```
##### 2. Create a new vector as dept with department names of the employees

```
dept <- c ("IT","Operations","IT","HR","Finance")
```

##### 3. Add this dept vector as a new column to data frame

```
emp.data <- cbind (emp.data, dept)
```

```
emp.data
```
##### 4. Create a new data frame with 3 more records

```
emp.newdata <- data.frame( 
emp_id = c (6:8),  
emp_name = c("Rasmi","Pranab","Tusar"), 
salary = c(578.0,722.5,632.8),  
start_date = as.Date (c ("2013-05-21","2013-07-30","2014-06-17")), 
dept = c("IT", "Operations", "Finance"), 
stringsAsFactors = FALSE 
)
```

##### 5. Add these new records to the existing data frame emp.data

```
emp.finaldata <- rbind (emp.data, emp.newdata) 
print(emp.finaldata)
