# Experiment 3: DML Commands

## AIM
To study and implement DML (Data Manipulation Language) commands.

## THEORY

### 1. INSERT INTO
Used to add records into a relation.
These are three type of INSERT INTO queries which are as
A)Inserting a single record
**Syntax (Single Row):**
```sql
INSERT INTO table_name (field_1, field_2, ...) VALUES (value_1, value_2, ...);
```
**Syntax (Multiple Rows):**
```sql
INSERT INTO table_name (field_1, field_2, ...) VALUES
(value_1, value_2, ...),
(value_3, value_4, ...);
```
**Syntax (Insert from another table):**
```sql
INSERT INTO table_name SELECT * FROM other_table WHERE condition;
```
### 2. UPDATE
Used to modify records in a relation.
Syntax:
```sql
UPDATE table_name SET column1 = value1, column2 = value2 WHERE condition;
```
### 3. DELETE
Used to delete records from a relation.
**Syntax (All rows):**
```sql
DELETE FROM table_name;
```
**Syntax (Specific condition):**
```sql
DELETE FROM table_name WHERE condition;
```
### 4. SELECT
Used to retrieve records from a table.
**Syntax:**
```sql
SELECT column1, column2 FROM table_name WHERE condition;
```
**Question 1**
--
-- <img width="925" height="454" alt="image" src="https://github.com/user-attachments/assets/05000bd7-c11f-4b2d-948e-c5eca336ff32" />


``` sql-
``UPDATE products
SET reorder_lvl = 40
WHERE category = 'Grocery';

```

**Output:**

<img width="977" height="390" alt="image" src="https://github.com/user-attachments/assets/bc6481f4-281a-4332-aa0f-577ba6871149" />


**Question 2**
---
--<img width="974" height="568" alt="image" src="https://github.com/user-attachments/assets/f570d21e-d154-4274-87fb-80ab9ed04d83" />


```sql
-- <img width="974" height="568" alt="image" src="https://github.com/user-attachments/assets/df559c12-0abb-474c-b37e-eccf113b9f85" />

```

**Output:**

<img width="1022" height="415" alt="image" src="https://github.com/user-attachments/assets/27d6b3e8-4a4a-44eb-8df0-a56d9b78e209" />


**Question 3**
---
-- <img width="885" height="639" alt="image" src="https://github.com/user-attachments/assets/770fe4e3-3e90-407e-9fb8-ca8287f9c434" />


```sql
--UPDATE sales
SET sell_price = sell_price + 3
WHERE product_id IN (
    SELECT product_id
    FROM products
    WHERE supplier_id = 4
);
```

**Output:**

<img width="978" height="386" alt="image" src="https://github.com/user-attachments/assets/17f7a614-5a85-4478-82a5-3d239a860368" />


**Question 4**
---
-- <img width="790" height="285" alt="image" src="https://github.com/user-attachments/assets/5a47df91-a499-4ab5-bcf7-37d77c424bb7" />


```sql
-- UPDATE products
SET quantity = quantity * 1.10;
```

**Output:**

<img width="984" height="564" alt="image" src="https://github.com/user-attachments/assets/cfc1532c-4b92-441d-be8c-dcd5345915c3" />


**Question 5**
---
-- <img width="1034" height="446" alt="image" src="https://github.com/user-attachments/assets/ea0633af-c60d-4fc6-ac1e-d6de9e92c0ab" />


```sql
--UPDATE products
SET reorder_lvl = reorder_lvl * 1.30
WHERE category = 'Food'
AND quantity < reorder_lvl * 0.50;
```

**Output:**

<img width="990" height="400" alt="image" src="https://github.com/user-attachments/assets/ae4bdaeb-2b25-4737-ad62-56c6971461cc" />


**Question 6**
---
--<img width="971" height="422" alt="image" src="https://github.com/user-attachments/assets/d6e69620-e970-40a9-847e-b70fe3f68625" />


```sql
-- DELETE FROM customer
WHERE GRADE % 2 = 1;
```

**Output:**

<img width="1004" height="414" alt="image" src="https://github.com/user-attachments/assets/60814859-6e37-4372-9dad-174edd1ae0cc" />


**Question 7**
---
<img width="982" height="456" alt="image" src="https://github.com/user-attachments/assets/5800bab5-cb18-451b-a372-6f111a08a9f1" />


```sql
--DELETE FROM customer
WHERE GRADE = 2
AND CUST_NAME LIKE 'M%'
AND PAYMENT_AMT < 3000;
```

**Output:**

<img width="1007" height="399" alt="image" src="https://github.com/user-attachments/assets/7e6a27ba-729f-49fd-9823-541b4503a9ff" />


**Question 8**
---
-- <img width="983" height="558" alt="image" src="https://github.com/user-attachments/assets/4951ea89-4347-439c-b715-b12dee22262e" />


```sql
--DELETE FROM customer
WHERE cust_city LIKE 'L%';
```

**Output:**

<img width="1042" height="694" alt="image" src="https://github.com/user-attachments/assets/72f65003-f9b7-43d2-adea-9d620c3c64be" />


**Question 9**
---
-- <img width="1035" height="432" alt="image" src="https://github.com/user-attachments/assets/492df600-d239-4402-b8d4-0c140d836f25" />


```sql
--DELETE FROM Doctors
WHERE Specialization = 'Pediatrics'
AND First_name = 'Michael';
```

**Output:**

<img width="1047" height="286" alt="image" src="https://github.com/user-attachments/assets/a66f1876-6a9e-4117-8aa5-95e73e5c7414" />


**Question 10**
---
-- <img width="1060" height="371" alt="image" src="https://github.com/user-attachments/assets/82f45f79-635f-4c6e-ad06-2a1513148bf1" />
Paste Question 10 here

```sql
-- DELETE FROM customer
WHERE CUST_COUNTRY NOT IN ('UK', 'USA', 'Canada')
AND GRADE >= 3;
```
**Output:**
<img width="1068" height="325" alt="image" src="https://github.com/user-attachments/assets/1b83cb7d-e229-41a0-8aa2-e6a9c912c323" />





## RESULT
Thus, the SQL queries to implement DML commands have been executed successfully.
