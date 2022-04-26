# sql-practice---02-by-chhavi-raj-singh


create database project use project

create table emp(emp_ID int primary key identity not null, emp_Name varchar(20) , emp_Salary money ,emp_Dept varchar(20),emp_Gender varchar(20) )

insert into emp values ('Rohan',20000,'IT','Male'), ('Mohan',25000,'HR','Male'), ('Shweta',30000,'IT','Female'), ('Sita',35000,'CS','Female'), ('Gita',40000,'IT','Female'), ('Jack',45000,'HR','Male')

select * into emp1 from emp

select * from emp where emp_salary between 20000 and 40000

create table dept (dept_ID int primary key identity not null,dept_Name varchar(20),dept_No int )

insert into dept values ('IT',2), ('HR',1), ('CS',4), ('IT',3), ('HR',6), ('IT',5)

select * from emp union select * from emp1

select emp_Name,dept_No , emp_salary from emp group by dept_No,emp_Name ,emp_salary order by emp_salary desc

select * from emp except select * from emp1

select * from emp union select * from emp1

select * from dept select * from emp select * from emp1

insert emp values ('deepak',10000,'mc','male',8)

select dept_No,sum(emp_salary) as totalsal from emp group by dept_No having sum(emp_id)>=2

select count(emp_salary) totalemp from emp

select min(emp_salary) totalsal from emp

select max(emp_salary) totalsal from emp

select sum(emp_salary) totalsal from emp

select avg(emp_salary) totalsal from emp
