# Handson 1
## Create a database , give it name like "Human_Resource". Create a collection inside this named "employee"
```
use Human_Resource
db.employee.insertMany({})
```
## Question No 1 => Query the collection "employee" and list all the documents
```
db.employee.find()
```

## Question No 2 => Query the collection "employee" and list the employees who are having salary more than 30000
```
db.employee.find({salary:{$gt:"30000"}})
```

## Question No 3 => Query the collection "employee" and list the employees who are having experience more than 2 years.
```
db.employee.find({overallExp:{$gt:"2"}})
```

## Question No 4 => Query the collection "employee" and list the employees who are graduated after 2015 and having experience more than 1 year
```
db.employee.find({yearGrad:{$gt:"2"},overallExp:{$gt:"1"}})
```

## Question No 5 => Query the collection "employee" and update the salary of the employee whose salary is greater than 70000 to 65000.
```
db.employee.updateMany({salary:{$gt:"70000"}},{$set:{salary:"65000}})
```

## Question No 6 => Delete all the documents from "employee" where last company is Y
```
db.employee.deleteMany({lastCompany:"Y"})
```