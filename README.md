# Java_JPA_Hibernate-lab-02_Case3_Solved

## Exercise

Identity of entity definition

Goal

Learn how to define simple and composite identity of entity in terms of Java Persistence API. 

Subject

There is a Department entity (with fields: companyName, name and description) and 3 cases to defined identity for it:

1.	Single identity

2.	Composite with identity as separate class (using @EmbeddedId)

3.	Composite with identity fields inside the entity class (using @IdClass)

**CASE 3#** :

Composite with identity fields inside the entity class (using @IdClass)

11.	Open class edu.jpa.entity.DepartmentKey

12.	Specify class-level annotation @Embeddable. This lets JPA runtime to know that this class is embeddable one and can be a part of an entity.

13.	Open class edu.jpa.entity.Department_3

14.	Specify class-level annotation @Entity. This lets JPA runtime to know that this particular class should be treated as an entity.

15.	Specify class-level annotation @IdClass with identity class DepartmentKey. This lets JPA runtime to know that DepartmentKey should be used as identity foe this entity (and entity class should contain fields with the same names as in DepartmentKey class).

16.	Specify field-level annotation @Id for any of key fields (companyName or departmentName).

17.	Open the class edu.jpa.Launcher and analyze its content with help of trainer (since EntityManager is not known for you yet).

18.	Run the class edu.jpa.Launcher. There should be no errors if entity is defined correctly.

19.	Open database DB_LAB_02 using MySQL Workbench and look on the created database objects.

## Solution

```
USE JPA_DB_02;

SHOW TABLES;

SELECT companyName, departmentName, description FROM Department_3;
```

<img width="1919" height="1020" alt="image" src="https://github.com/user-attachments/assets/e1980e41-49f4-4dbf-a083-2899db6b22ba" />
