# assignment9_database


select customers.customerName, offices.city as office_city from customers, employees, offices where customers.salesRepEmployeeNumber = employees.employeeNumber and employees.officeCode = offices.officeCode and customers.city = offices.city;

1. Rewrite it as an expression in relational algebra
2. Add row counts to the subexpressions
3. Rewrite to a better expression

1. ρofficecity/office.city(σsalesRepEmployeeNumber=employeeNumber(customers122×(employees23⋈offices7)))ρofficecity/office.city(σsalesRepEmployeeNumber=employeeNumber(customers122×(employees23⋈offices7)))

