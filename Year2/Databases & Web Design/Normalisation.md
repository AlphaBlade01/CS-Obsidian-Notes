### 1NF
	The key
- Single cell must not hold more than 1 value **(atomicity)**
- Must be a primary key for identification
- No duplicate rows or columns
- Each column must only have one value for each row in the table
#### Mitigation
- If a column contains multiple values, separate them into different columns
- Ensure every table has a primary key
### 2NF
	The whole key
- Must be in 1NF
- Each non-key attribute must be functionally dependent on the entire primary key
- $X\rightarrow Y$ : X is determinant and Y is dependent
#### Mitigation
- Identify composite primary keys and check if any non-key columns rely only on part of that key
- Move the partially dependent columns into a new table, making that specific part the primary key of the new table
### 3NF
	And nothing but the key
- Must be in 2NF
- Has no transitive functional dependency
	Every non-key attribute depends only on the primary key
#### Mitigation
- Look for columns that depend on columns other than the primary key
- Extract transitively dependent columns into separate table using an intermediate column as a foreign key link