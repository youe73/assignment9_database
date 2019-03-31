# assignment9_database


select customers.customerName, offices.city as office_city from customers, employees, offices where customers.salesRepEmployeeNumber = employees.employeeNumber and employees.officeCode = offices.officeCode and customers.city = offices.city;

1. Rewrite it as an expression in relational algebra
2. Add row counts to the subexpressions
3. Rewrite to a better expression

1. ρofficecity/office.city(σsalesRepEmployeeNumber=employeeNumber(customers122×(employees23⋈offices7)))ρofficecity/office.city(σsalesRepEmployeeNumber=employeeNumber(customers122×(employees23⋈offices7)))

![image](https://user-images.githubusercontent.com/40825848/55295765-4d536900-5411-11e9-9200-71a88af0af82.png)

2 and 3
\Pi_{customerName,office\_city}(\rho_{office\_city/office.city}(\sigma_{salesRepEmployeeNumber=employeeNumber}(customers^{122}\times (employees^{23}\bowtie offices^{7})^{23} )^{2806} )^{14})


