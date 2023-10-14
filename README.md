# EX-2-Data-Manipulation-Language-DML-and-Data-Control-Language-DCL-Commands


# AIM:

To create a manager database and execute DML queries using SQL.


# DML(Data Manupulation Language)


The SQL commands that deal with the manipulation of data present in the database belong to DML or Data

Manipulation Language and this includes most of the SQL statements. It is the component of the SQL statement that

controls access to data and to the database. Basically, DCL statements are grouped with DML statements.


# List of DML commands:


INSERT: It is used to insert data into a table.


UPDATE: It is used to update existing data within a table.


DELETE: It is used to delete records from a database table.


# Create the table as given below:
```

create table manager(enumber number(6),ename char(15),salary number(5),commission number(4),annualsalary number(7),Hiredate date,designation char(10),deptno number(2),reporting char(10));
```

# insert the following values into the table

```
insert into manager values(7369,'Dharsan',2500,500,30000,'30-June-81','clerk',10,'John');
insert into manager values(7839,'Subu',3000,400,36000,'1-Jul-82','manager',null,'James');
insert into manager values(7934,'Aadhi',3500,300,42000,'1-May-82','manager',30,NULL);
insert into manager values(7788,'Vikash',4000,0,48000,'12-Aug-82','clerk',50,'Bond');
```

# Q1) Update all the records of manager table by increasing 10% of their salary as bonus.


# QUERY:
```
SQL> update manager set salary = (salary*0.10)+ salary ;
```

# OUTPUT:

<img width="622" alt="271330834-ff9576d8-3bbb-4a1c-9cb7-30e5ad3734e2" src="https://github.com/surrey-78/EX-2-Data-Manipulation-Language-DML-and-Data-Control-Language-DCL-Commands/assets/119559366/2a5a370e-f508-4870-99de-43c6335e7a3d">



# Q2) Delete the records from manager table where the salary less than 2750.

# QUERY:

```
SQL> delete worker where salary<2750;
```
# OUTPUT:

<img width="623" alt="271331269-84d0df87-a35f-4664-b0ec-6aca8c0022e2" src="https://github.com/surrey-78/EX-2-Data-Manipulation-Language-DML-and-Data-Control-Language-DCL-Commands/assets/119559366/f32bb5bd-4507-441d-9ab6-519657ac5738">



# Q3) Display each name of the employee as “Name” and annual salary as “Annual Salary” (Note: Salary in emp table is the monthly salary)


# QUERY:

```
SQL> SELECT
2  ename AS "name",

3  salary * 12 AS "Annual Salary" 

4  FROM

5  manger ;

```
# OUTPUT:


<img width="379" alt="271331676-674dae99-3c3f-4984-ad14-dcec30197783" src="https://github.com/surrey-78/EX-2-Data-Manipulation-Language-DML-and-Data-Control-Language-DCL-Commands/assets/119559366/3d96a8c4-e15d-44f7-8320-d7e1b4f08e65">

# Q5) List the names of Clerks from emp table.

# QUERY:
```
SQL> select ename from empn where designation='clerk' ;

```
# OUTPUT:

<img width="337" alt="271332012-df0633ba-f55c-4774-b553-173e224ad9bb" src="https://github.com/surrey-78/EX-2-Data-Manipulation-Language-DML-and-Data-Control-Language-DCL-Commands/assets/119559366/be7af646-5090-480c-b43d-f296b6c37ad5">


# Q6) List the names of employee who are not Managers.

# QUERY:

```
SQL> select ename from empn where designation !='manager' ;

```

# OUTPUT:

<img width="295" alt="271332434-b8dc1f41-6812-4766-8a99-446a523e86a8" src="https://github.com/surrey-78/EX-2-Data-Manipulation-Language-DML-and-Data-Control-Language-DCL-Commands/assets/119559366/5f9fff69-9b6b-4191-a408-d5bae8c9f0d0">




# Q7) List the names of employees not eligible for commission.

# QUERY:
```
SQL> select ename from empn where commission=0;

```

# OUTPUT:
<img width="275" alt="271332903-097b4782-ae25-4931-af81-e1df1f0d6f64" src="https://github.com/surrey-78/EX-2-Data-Manipulation-Language-DML-and-Data-Control-Language-DCL-Commands/assets/119559366/92bf58a7-ae91-4cd7-a065-e440d28f6444">




# Q8) List employees whose name either start or end with ‘s’.

# QUERY:
```
SQL> select ename from empn where ename LIKE 'S%' OR ename LIKE '%s';

```
# OUTPUT:

<img width="278" alt="271333234-24b10315-f682-4407-a478-9a83f5b934b2" src="https://github.com/surrey-78/EX-2-Data-Manipulation-Language-DML-and-Data-Control-Language-DCL-Commands/assets/119559366/88e20f8d-bbaf-4807-ad82-f97cbd594e0b">


# Q9) Sort emp table in ascending order by hire-date and list ename, job, deptno and hire-date.

# QUERY:
```
SQL> SELECT ename, designation, deptno, hiredate

2 from empn

3 order by hiredate ASC;


```
# OUTPUT:

<img width="640" alt="271333616-c5f3b867-e455-4fa6-a7f9-9b9f414fa991" src="https://github.com/surrey-78/EX-2-Data-Manipulation-Language-DML-and-Data-Control-Language-DCL-Commands/assets/119559366/22b0cbb5-b6ad-40c6-b2d3-d3537365e111">


# Q10) List the Details of Employees who have joined before 30 Sept 81.

# QUERY:
```
SQL> SELECT * FROM empn WHERE hiredate <'30 sep 81';
```
# OUTPUT:
<img width="600" alt="271334089-c9a4bea4-db4a-4739-b5be-c436386c5001" src="https://github.com/surrey-78/EX-2-Data-Manipulation-Language-DML-and-Data-Control-Language-DCL-Commands/assets/119559366/93ba3bf2-80de-4309-b57c-a83dc37543e7">



# Q11) List ename, deptno and sal after sorting emp table in ascending order by deptno and then descending order by sal.

# QUERY:
```
SQL> SELECT ename, designation, salary from empn ORDER BY deptno ASC, salary DESC;
```
# OUTPUT:

<img width="451" alt="271334565-959263c4-cda3-4239-a011-26dafa63b3f9" src="https://github.com/surrey-78/EX-2-Data-Manipulation-Language-DML-and-Data-Control-Language-DCL-Commands/assets/119559366/ddf76810-73fd-46a4-80ab-505ebf5278f9">


# Q12) List the names of employees not belonging to dept no 30,40 & 10

# QUERY:
```
SQL> SELECT ename from empn WHERE deptno NOT IN (30, 40, 10);

```

# OUTPUT:

<img width="244" alt="271334929-15501d43-2de3-43be-9694-2b11403049c1" src="https://github.com/surrey-78/EX-2-Data-Manipulation-Language-DML-and-Data-Control-Language-DCL-Commands/assets/119559366/17ac060e-b5a8-43f4-9931-8b9ba605eac1">


# Q13) Find number of rows in the table EMP


# QUERY:
```
SQL> SELECT COUNT(*) AS num_rows FROM empn;

```
# OUTPUT:

<img width="138" alt="271335496-378d6d3f-f013-40d9-a420-c9fe1aab0164" src="https://github.com/surrey-78/EX-2-Data-Manipulation-Language-DML-and-Data-Control-Language-DCL-Commands/assets/119559366/cca2df17-ece8-4d88-974d-eb3e458d63c2">


# Q14) Find maximum, minimum and average salary in EMP table.

# QUERY:

<img width="622" alt="271335677-4e51d334-b5b9-419c-8de4-a164bb169aef" src="https://github.com/surrey-78/EX-2-Data-Manipulation-Language-DML-and-Data-Control-Language-DCL-Commands/assets/119559366/66f1777b-401b-44cc-ad5b-48222cf6733b">

# OUTPUT:

<img width="320" alt="271335853-9b08ed54-8647-44f6-8b9a-5f964d563b93" src="https://github.com/surrey-78/EX-2-Data-Manipulation-Language-DML-and-Data-Control-Language-DCL-Commands/assets/119559366/b176837b-4964-4066-97e9-d5ced9bd199f">


# Q15) List the jobs and number of employees in each job. The result should be in the descending order of the number of employees.

# QUERY:

<img width="607" alt="271336118-8fa00bc5-e856-4b32-8250-a51641947a97" src="https://github.com/surrey-78/EX-2-Data-Manipulation-Language-DML-and-Data-Control-Language-DCL-Commands/assets/119559366/e395ad9f-28f5-4787-8344-f486fb85b0c2">

# OUTPUT:

<img width="325" alt="271336256-211a9877-2d0f-40a0-9b9a-b755197f3fe9" src="https://github.com/surrey-78/EX-2-Data-Manipulation-Language-DML-and-Data-Control-Language-DCL-Commands/assets/119559366/cee05be7-6c36-493f-9159-f142f78fabe0">

