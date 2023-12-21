# Library_management-_sys
The Efficient library management system using SQL and C++. Manage library collection, facilitate user interactions, and generate data-driven insights.
ER diagram and schema, including a description of the relationships between the entities:

![image](https://github.com/KRISH7706/Library_management-_sys/assets/92157939/6653d486-10de-4bc8-b559-27e9b8ce6083)
fig - class Diagram

![image](https://github.com/KRISH7706/Library_management-_sys/assets/92157939/b4b8c82c-9e9f-4ad9-b99d-7bbebf920437)
fig- E-R Diagram 

----------
Entities
----------
Student:
Primary Key: Id (string)

Library (Book):
Primary Key: Name (string)
Attribute: Quantity (int)


Relationships:
Borrow: Many-to-Many Relationship between Student and Library

