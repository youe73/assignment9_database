# assignment9_database


select customers.customerName, offices.city as office_city from customers, employees, offices where customers.salesRepEmployeeNumber = employees.employeeNumber and employees.officeCode = offices.officeCode and customers.city = offices.city;

1. Rewrite it as an expression in relational algebra
2. Add row counts to the subexpressions
3. Rewrite to a better expression

1. Rewritting the query to algebra relation in jupyter notebook. Select the markdown and put the query between 2 dollarsign $.

ρofficecity/office.city(σsalesRepEmployeeNumber=employeeNumber(customers122×(employees23⋈offices7)))ρofficecity/office.city(σsalesRepEmployeeNumber=employeeNumber(customers122×(employees23⋈offices7)))

![image](https://user-images.githubusercontent.com/40825848/55295765-4d536900-5411-11e9-9200-71a88af0af82.png)


2 The row account is added.
\Pi_{customerName,office\_city}(\rho_{office\_city/office.city}(\sigma_{salesRepEmployeeNumber=employeeNumber}(customers^{122}\times (employees^{23}\bowtie offices^{7})^{23} )^{2806} )^{14})

![image](https://user-images.githubusercontent.com/40825848/55295798-acb17900-5411-11e9-8779-7db888d611b0.png)

3 Rewritting the query to a better expression.
\Pi_{customerName,office_city}(\rho_{office_city/office.city}((\sigma_{salesRepEmployeeNumber=employeeNumber}(customers^{122}\times employees^{23}))^{14}\bowtie offices^{7})^{14})

![image](https://user-images.githubusercontent.com/40825848/55295808-c9e64780-5411-11e9-9d22-7730932477e9.png)


