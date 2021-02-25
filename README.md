# Record Table Database
#### Designer: Andrew Vien
#### Concepts: C++ Fundamentals of Data Structures  
#### Made with: Qt Creator editor.

Executable C++ application that creates records database based on user command input. Database includes elements which can be dynamically modified, and efficient search algorithms for conditional values. Additional database tables can be created through user-defined search filtering. 
Program involves SQL command parsing, custom multi maps (without multi map plugin) through linked lists and BPlus Trees, and file reading/writing.  

How to use:  
1. Download app folder  
2. Run _.exe_ file
3. Enter command  
4. Press _return_  

#### Commands
•	**create table _table name_ (_element 1[,element 2,element 3,...]_)**  
  o	Creates named table, which can then be printed, modified, loaded, and selected. Table file is automatically written after creation.  
  o	Example: **_create table classmates (lname,fname,age,gender,grade)_** creates a table with respective element names  
•	**create table _table name_ as [select command]**  
  o	Creates named table from table defined by select command (see select command)  
  o	Example: **_create table roll_call as select fname,lname from classmates_** will create a new table _roll_call_ with only first and last names of elements from _classmates_  
  
•	**insert into _table name_ values _element1,element2,..._**  
  o	Inserts custom values into _table_name_'s respective table elements. Number of elements MUST be exactly the same as defined by table  
  o	Example **_insert into classmates Smith,Billy,14,male,9_**  
•	**select _element1[,element2,…]_ from _tablename_ [where _element_ _conditional_symbol_ “_value_”]**  
  o	creates temporary table with elements from existing table with elements in custom order  
  o	Additional conditional statement filter (i.e. adding _where fname > “A”_ will select only elements where fname is greater than value “A”)  
  o	Example: _select fname from classmates_ will display a table with only first names of all elements in table _classmates_  
•	**load _table_name_**  
  o	Loads saved table into program database. Error message will display if table doesn't exist.

