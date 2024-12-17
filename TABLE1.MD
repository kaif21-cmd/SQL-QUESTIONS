# Table 1 

```jsx
CREATE TABLE Manufacturers (
	Code INTEGER PRIMARY KEY NOT NULL,
	Name CHAR(50) NOT NULL 
);

CREATE TABLE Products (
	Code INTEGER PRIMARY KEY NOT NULL,
	Name CHAR(50) NOT NULL ,
	Price REAL NOT NULL ,
	Manufacturer INTEGER NOT NULL 
		CONSTRAINT fk_Manufacturers_Code REFERENCES Manufacturers(Code)
);

1. Select the names of all the products in the store.

mysql> select *from products;

+------+-----------+--------+--------------+
| Code | Name      | Price  | Manufacturer |
+------+-----------+--------+--------------+
|  101 | Product X |  99.99 |            1 |
|  102 | Product Y |  149.5 |            2 |
|  103 | Product Z |    200 |            3 |
|  104 | Product W | 120.75 |            1 |
+------+-----------+--------+--------------+
```jsx


