# DATA-CLEANING-UPDATE-DAN-TRANSFORMASI-TIPE-DATA-DALAM-SQL
Proyek ini bertujuan untuk menerapkan teknik data cleaning, update, dan transformasi tipe data menggunakan SQL guna memastikan kualitas dan integritas data dalam database customer. 
Pada proyek ini terdapat 3 tabel utama, yaitu Customers, Orders, dan Products:
- Customers: Menyimpan data pelanggan.
- Orders: Menyimpan data pesanan pelanggan.
- Products: Menyimpan data produk yang dijual.
- Kolom-kolom dari masing-masing tabel adalah sebagai berikut:

Tabel Customers:
CustomerID, FirstName, LastName, Email, Phone, Address, City, ZipCode, SignupDate.

Tabel Orders:
OrderID, CustomerID, ProductID, OrderDate, Quantity, OrderStatus, TotalAmount.

Tabel Products:
ProductID, ProductName, Category, Price, StockQuantity.

Dataset https://www.kaggle.com/datasets/aymenberkani/data-cleaning-for-a-customer-database

## Transformasi Tipe Data
### Tabel Customer
``` sql
ALTER TABLE e_customers
ALTER COLUMN CustomerID INT;

ALTER TABLE e_customers
ALTER COLUMN FirstName VARCHAR (50);

ALTER  TABLE e_customers
ALTER COLUMN LastName VARCHAR (50);

ALTER  TABLE e_customers
ALTER COLUMN Email VARCHAR (100);

ALTER  TABLE e_customers
ALTER COLUMN Phone VARCHAR (20);

ALTER  TABLE e_customers
ALTER COLUMN Address VARCHAR (150);

ALTER  TABLE e_customers
ALTER COLUMN City VARCHAR (200);

ALTER  TABLE e_customers
ALTER COLUMN ZipCode INT;
```
### Tabel Orders
``` sql
ALTER TABLE e_orders
ALTER COLUMN OrderID INT;

ALTER TABLE e_orders
ALTER COLUMN CustomerID INT;

ALTER TABLE e_orders
ALTER COLUMN ProductID INT;

ALTER TABLE e_orders
ALTER COLUMN OrderDate DATE;

ALTER TABLE e_orders
ALTER COLUMN Quantity INT

ALTER TABLE e_orders
ALTER COLUMN OrderStatus VARCHAR (50);

ALTER TABLE e_orders
ALTER COLUMN TotalAmount DECIMAL (10 , 2);
```
### Tabel Product
``` sql ALTER TABLE [e_products (1)]
ALTER COLUMN ProductID INT;

ALTER TABLE [e_products (1)]
ALTER COLUMN ProductName VARCHAR (100);

ALTER TABLE [e_products (1)]
ALTER COLUMN Category VARCHAR (50);

ALTER TABLE [e_products (1)]
ALTER COLUMN Price DECIMAL (10, 2);

ALTER TABLE [e_products (1)]
ALTER COLUMN StockQuantity INT;
```



