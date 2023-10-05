# Ex-No-4-Creating-Procedures-using-PL-SQL

# AIM: To create a procedure using PL/SQL.

# Steps:
```
1.Create employee table with following attributes (empid NUMBER, empname VARCHAR(10), dept VARCHAR(10),salary NUMBER);
2.Create a procedure named as insert_employee data.
3.Inside the procdure block, write the query for inserting the values into the employee table.
4.End the procedure.
5.Call the insert_employee data procedure to insert the values into the employee table.
6.Display the employee table
```

# Program:
```
CREATE TABLE ep4(
       empid NUMBER,
       empname VARCHAR(10),
       dept VARCHAR(10),
       salary NUMBER
       );
       CREATE OR REPLACE PROCEDURE emp_data AS
       BEGIN
       INSERT INTO ep4(empid,empname,dept,salary)
       values(1,'thanika','MD',10000000);
       INSERT INTO ep4(empid,empname,dept,salary)
       values(2,'priya','HR',500000);
       INSERT INTO ep4(empid,empname,dept,salary)
       values(3,'swetha','IT',200000);
       COMMIT;
       FOR emp_rec IN (SELECT * FROM ep4)LOOP
       DBMS_OUTPUT.PUT_LINE('EMPLOYEE ID:'||emp_rec.empid||',EMPLOYEE NAME:'|| emp_rec.empname||
       ',DEPARTMENT:'||emp_rec.dept||',SALARY:'||emp_rec.salary);
       END LOOP;
       END;
```
# Output:
![Screenshot (48)](https://github.com/Thanikasreeb/Ex-No-4-Creating-Procedures-using-PL-SQL/assets/119557910/1347fd01-4b7a-4451-8d31-589b5fafa1e6)

# Result:
Thus,the output has been successfully verified!



