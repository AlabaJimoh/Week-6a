Query to retrieve employee details and their office information
SELECT
    e.firstName,
    e.lastName,
    e.email,
    e.officeCode
FROM
    employees e
JOIN
    offices o ON e.officeCode = o.officeCode;

Query to retrieve product details and their product line information
SELECT
    p.productName,
    p.productVendor,
    pl.productLine
FROM
    products p
LEFT JOIN
    productlines pl ON p.productLine = pl.productLine;

Query to retrieve order details for the first 10 orders
SELECT
    o.orderDate,
    o.shippedDate,
    o.status,
    o.customerNumber
FROM
    customers c
RIGHT JOIN
    orders o ON c.customerNumber = o.customerNumber
LIMIT 10;
