# Ex. No: 4 Creating Procedures using PL/SQL

### AIM: To create a procedure using PL/SQL.

### Steps:
1. Create employee table with following attributes (empid NUMBER, empname VARCHAR(10), dept VARCHAR(10),salary NUMBER);
2. Create a procedure named as insert_employee data.
3. Inside the procdure block, write the query for inserting the values into the employee table.
4. End the procedure.
5. Call the insert_employee data procedure to insert the values into the employee table.
6. Display the employee table

### Program:
```
SQL> CREATE TABLE employ4( empid NUMBER,empname VARCHAR(10),dept VARCHAR(10), salary NUMBER);
set serveroutput on
SQL> CREATE OR REPLACE PROCEDURE emp_data AS
  2  BEGIN
  3  INSERT INTO employ4(empid,empname,dept,salary)
  4  values(1,'DAMON','MD',90000);
  5  INSERT INTO employ4(empid,empname,dept,salary)
  6  values(2,'STEPHAN','HR',70000);
  7  INSERT INTO employ4(empid,empname,dept,salary)
  8  values(3,'BELLA','IT',80000);
  9  COMMIT;
 10  FOR emp_rec IN (SELECT * FROM employ4)LOOP
 11  DBMS_OUTPUT.PUT_LINE('EMPLOYEE ID:'||emp_rec.empid||',EMPLOYEE NAME:'|| emp_rec.empname||',DEPARTMENT:'||emp_rec.dept||',SALARY:'||emp_rec.salary);
 12  END LOOP;
 13  END;
 14  /
```

### Output:
![EX4 OP](https://github.com/varshxnx/Ex-No-4-Creating-Procedures-using-PL-SQL/assets/122253525/c181f5a4-0493-48bb-a5df-d720cbe1101f)


### Result:
THE PROGRAM HAS BEEN IMPLEMENTED SUCCESSFULLY
