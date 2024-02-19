CREATE TABLES :

CREATE TABLE Designation_Masters (Design_code NUMBER(3) NOT NULL, Design_name Varchar2(50) );
DESC Designation_Masters;

CREATE TABLE Department_Masters ( Dept_Code Number(2) NOT NULL , Dept_name Varchar2(50));
DESC Department_Masters;

CREATE TABLE Student_masters ( Student_Code NUMBER(6) NOT NULL , Student_name VARCHAR2(50) NOT NULL , Dept_Code NUMBER(2) , Student_dob Date , Student_Address Varchar2(240));
DESC Student_Masters;

CREATE TABLE Student_Marks (Student_Code NUMBER(6) , Student_Year Number NOT NULL , Subject1 NUMBER(3) , Subject2 NUMBER(3) ,Subject3 NUMBER(3));
DESC Student_Marks;

CREATE TABLE Staff_Masters ( Staff_Code NUMBER(8) NOT NULL , Staff_Name Varchar2(50) NOT NULL , Design_Code NUMBER , Dept_Code NUMBER , HireDate  DATE , Staff_dob DATE , Staff_address VARCHAR2(240) , Mgr_code Number(8) , Staff_sal NUMBER(10,2));
DESC Staff_Masters;

CREATE TABLE Book_Masters ( Book_Code NUMBER(10) NOT NULL , Book_Name Varchar2(50) NOT NULL , Book_pub_year NUMBER , Book_pub_author VARCHAR2(50) NOT NULL);
DESC Book_Masters;

CREATE TABLE Book_Transactions ( Book_Code NUMBER , Student_code NUMBER , Staff_code NUMBER , Book_issue_date DATE NOT NULL , Book_expected_return_date DATE NOT NULL , Book_actual_return_date DATE);
DESC Book_Transactions;

--------------------------
INSERT DATA : 
--------------------------

INSERT INTO designation_masters (DESIGN_CODE, DESIGN_NAME) VALUES (1, 'Professor');
INSERT INTO designation_masters (DESIGN_CODE, DESIGN_NAME) VALUES (2, 'Assistant Professor');
INSERT INTO designation_masters (DESIGN_CODE, DESIGN_NAME) VALUES (3, 'Lecturer');
INSERT INTO designation_masters (DESIGN_CODE, DESIGN_NAME) VALUES (4, 'Research Assistant');
INSERT INTO designation_masters (DESIGN_CODE, DESIGN_NAME) VALUES (5, 'Lab Technician');
INSERT INTO designation_masters (DESIGN_CODE, DESIGN_NAME) VALUES (6, 'Administrator');


-- Inserting into department_masters
INSERT INTO department_masters (DEPT_CODE, DEPT_NAME) VALUES (10, 'Computer Science');
INSERT INTO department_masters (DEPT_CODE, DEPT_NAME) VALUES (20, 'Electrical Engineering');
INSERT INTO department_masters (DEPT_CODE, DEPT_NAME) VALUES (30, 'Mechanical Engineering');
INSERT INTO department_masters (DEPT_CODE, DEPT_NAME) VALUES (40, 'Business Administration');
INSERT INTO department_masters (DEPT_CODE, DEPT_NAME) VALUES (50, 'Finance');
INSERT INTO department_masters (DEPT_CODE, DEPT_NAME) VALUES (60, 'Human Resources');


-- Inserting into student_masters
INSERT INTO student_masters (STUDENT_CODE, STUDENT_NAME, DEPT_CODE, STUDENT_DOB, STUDENT_ADDRESS)
VALUES (1001, 'Alice Johnson', 10, TO_DATE('2000-03-12', 'YYYY-MM-DD'), 'PUNE');


INSERT INTO student_masters (STUDENT_CODE, STUDENT_NAME, DEPT_CODE, STUDENT_DOB, STUDENT_ADDRESS)
VALUES (1002, 'Bob Smith', 10, TO_DATE('2001-05-25', 'YYYY-MM-DD'), 'MUMBAI');


INSERT INTO student_masters (STUDENT_CODE, STUDENT_NAME, DEPT_CODE, STUDENT_DOB, STUDENT_ADDRESS)
VALUES (1003, 'Eva Martinez', 20, TO_DATE('1999-08-18', 'YYYY-MM-DD'), 'HYDREABAD');


INSERT INTO student_masters (STUDENT_CODE, STUDENT_NAME, DEPT_CODE, STUDENT_DOB, STUDENT_ADDRESS)
VALUES (1004, 'David Lee', 20, TO_DATE('2000-11-30', 'YYYY-MM-DD'), 'CHENNAI');


INSERT INTO student_masters (STUDENT_CODE, STUDENT_NAME, DEPT_CODE, STUDENT_DOB, STUDENT_ADDRESS)
VALUES (1005, 'Sophia Brown', 30, TO_DATE('2001-01-15', 'YYYY-MM-DD'), 'DELHI');


INSERT INTO student_masters (STUDENT_CODE, STUDENT_NAME, DEPT_CODE, STUDENT_DOB, STUDENT_ADDRESS)
VALUES (1006, 'Oliver Taylor', 30, TO_DATE('1999-09-08', 'YYYY-MM-DD'), 'PUNE');


-- Inserting into student_marks
INSERT INTO student_marks (STUDENT_CODE, STUDENT_YEAR, SUBJECT1, SUBJECT2, SUBJECT3)
VALUES (1001, 2023, 85, 90, 92);


INSERT INTO student_marks (STUDENT_CODE, STUDENT_YEAR, SUBJECT1, SUBJECT2, SUBJECT3)
VALUES (1002, 2024, 88, 92, 95);


INSERT INTO student_marks (STUDENT_CODE, STUDENT_YEAR, SUBJECT1, SUBJECT2, SUBJECT3)
VALUES (1003, 2025, 90, 94, 96);


INSERT INTO student_marks (STUDENT_CODE, STUDENT_YEAR, SUBJECT1, SUBJECT2, SUBJECT3)
VALUES (1004, 2023, 78, 80, 85);


INSERT INTO student_marks (STUDENT_CODE, STUDENT_YEAR, SUBJECT1, SUBJECT2, SUBJECT3)
VALUES (1005, 2024, 82, 85, 88);


INSERT INTO student_marks (STUDENT_CODE, STUDENT_YEAR, SUBJECT1, SUBJECT2, SUBJECT3)
VALUES (1006, 2025, 85, 88, 90);




-- Inserting into staff_masters
INSERT INTO staff_masters (STAFF_CODE, STAFF_NAME, DESIGN_CODE, DEPT_CODE, HIREDATE, STAFF_DOB, STAFF_ADDRESS, MGR_CODE, STAFF_SAL)
VALUES (20001, 'Michael Adams', 1, 10, TO_DATE('2010-05-15', 'YYYY-MM-DD'), TO_DATE('1975-09-22', 'YYYY-MM-DD'), 'BANER', 801, 80000.00);


INSERT INTO staff_masters (STAFF_CODE, STAFF_NAME, DESIGN_CODE, DEPT_CODE, HIREDATE, STAFF_DOB, STAFF_ADDRESS, MGR_CODE, STAFF_SAL)
VALUES (20002, 'Sarah Brown', 2, 10, TO_DATE('2015-08-10', 'YYYY-MM-DD'), TO_DATE('1980-12-12', 'YYYY-MM-DD'), 'KOTHRUD', 800, 60000.00);


INSERT INTO staff_masters (STAFF_CODE, STAFF_NAME, DESIGN_CODE, DEPT_CODE, HIREDATE, STAFF_DOB, STAFF_ADDRESS, MGR_CODE, STAFF_SAL)
VALUES (20003, 'Emily Davis', 3, 20, TO_DATE('2018-03-20', 'YYYY-MM-DD'), TO_DATE('1985-06-05', 'YYYY-MM-DD'), 'HADAPSAR', 802, 55000.00);


INSERT INTO staff_masters (STAFF_CODE, STAFF_NAME, DESIGN_CODE, DEPT_CODE, HIREDATE, STAFF_DOB, STAFF_ADDRESS, MGR_CODE, STAFF_SAL)
VALUES (20008, 'Rohit', 3, 20, TO_DATE('2018-03-20', 'YYYY-MM-DD'), TO_DATE('1985-06-05', 'YYYY-MM-DD'), 'KHARADI', 803, 15000.00);


INSERT INTO staff_masters (STAFF_CODE, STAFF_NAME, DESIGN_CODE, DEPT_CODE, HIREDATE, STAFF_DOB, STAFF_ADDRESS, MGR_CODE, STAFF_SAL)
VALUES (20004, 'Daniel Wilson', 4, 20, TO_DATE('2019-01-25', 'YYYY-MM-DD'), TO_DATE('1982-11-18', 'YYYY-MM-DD'), 'WAKAD', 805, 50000.00);


INSERT INTO staff_masters (STAFF_CODE, STAFF_NAME, DESIGN_CODE, DEPT_CODE, HIREDATE, STAFF_DOB, STAFF_ADDRESS, MGR_CODE, STAFF_SAL)
VALUES (20005, 'Olivia Taylor', 5, 30, TO_DATE('2016-06-12', 'YYYY-MM-DD'), TO_DATE('1978-04-30', 'YYYY-MM-DD'), 'HINJEWADI', 804, 45000.00);


INSERT INTO staff_masters (STAFF_CODE, STAFF_NAME, DESIGN_CODE, DEPT_CODE, HIREDATE, STAFF_DOB, STAFF_ADDRESS, MGR_CODE, STAFF_SAL)
VALUES (20006, 'Noah Martinez', 6, 40, TO_DATE('2017-09-08', 'YYYY-MM-DD'), TO_DATE('1989-07-20', 'YYYY-MM-DD'), 'KARVE NAGAR', 800, 70000.00);






-- Inserting into book_masters
INSERT INTO book_masters (BOOK_CODE, BOOK_NAME, BOOK_PUB_YEAR, BOOK_PUB_AUTHOR) VALUES (3001, 'Introduction to Computer Science', 2019, 'John Smith');
INSERT INTO book_masters (BOOK_CODE, BOOK_NAME, BOOK_PUB_YEAR, BOOK_PUB_AUTHOR) VALUES (3002, 'Business Ethics', 2020, 'Emily Green');
INSERT INTO book_masters (BOOK_CODE, BOOK_NAME, BOOK_PUB_YEAR, BOOK_PUB_AUTHOR) VALUES (3003, 'Engineering Fundamentals', 2018, 'Emma White');
INSERT INTO book_masters (BOOK_CODE, BOOK_NAME, BOOK_PUB_YEAR, BOOK_PUB_AUTHOR) VALUES (3004, 'Financial Accounting', 2021, 'David Brown');
INSERT INTO book_masters (BOOK_CODE, BOOK_NAME, BOOK_PUB_YEAR, BOOK_PUB_AUTHOR) VALUES (3005, 'Data Structures and Algorithms', 2017, 'James Davis');
INSERT INTO book_masters (BOOK_CODE, BOOK_NAME, BOOK_PUB_YEAR, BOOK_PUB_AUTHOR) VALUES (3006, 'Organizational Behavior', 2019, 'Sophia King');


-- Inserting into book_transactions
INSERT INTO book_transactions (BOOK_CODE, STUDENT_CODE, BOOK_ISSUE_DATE, BOOK_EXPECTED_RETURN_DATE)
VALUES (3001, 1001, TO_DATE('2024-02-17', 'YYYY-MM-DD'), TO_DATE('2024-03-16', 'YYYY-MM-DD'));


INSERT INTO book_transactions (BOOK_CODE, STUDENT_CODE, BOOK_ISSUE_DATE, BOOK_EXPECTED_RETURN_DATE)
VALUES (3002, 1002, TO_DATE('2024-02-17', 'YYYY-MM-DD'), TO_DATE('2024-03-16', 'YYYY-MM-DD'));


INSERT INTO book_transactions (BOOK_CODE, STUDENT_CODE, BOOK_ISSUE_DATE, BOOK_EXPECTED_RETURN_DATE)
VALUES (3003, 1003, TO_DATE('2024-02-17', 'YYYY-MM-DD'), TO_DATE('2024-03-16', 'YYYY-MM-DD'));


INSERT INTO book_transactions (BOOK_CODE, STAFF_CODE, BOOK_ISSUE_DATE, BOOK_EXPECTED_RETURN_DATE)
VALUES (3004, 20002, TO_DATE('2024-02-17', 'YYYY-MM-DD'), TO_DATE('2024-03-16', 'YYYY-MM-DD'));


INSERT INTO book_transactions (BOOK_CODE, STAFF_CODE, BOOK_ISSUE_DATE, BOOK_EXPECTED_RETURN_DATE)
VALUES (3005, 20003, TO_DATE('2024-02-17', 'YYYY-MM-DD'), TO_DATE('2024-03-16', 'YYYY-MM-DD'));


INSERT INTO book_transactions (BOOK_CODE, STAFF_CODE, BOOK_ISSUE_DATE, BOOK_EXPECTED_RETURN_DATE)
VALUES (3006, 20006, TO_DATE('2024-02-17', 'YYYY-MM-DD'), TO_DATE('2024-03-16', 'YYYY-MM-DD'));


1. SELECT Staff_Name , Staff_Sal , Dept_Code from Staff_Masters where Dept_Code in (20,30,40);

2. select staff_name as "employee_name" , staff_sal as"salary" ,dept_code as "Department_Number" from staff_masters;
 
3. SELECT STUDENT_CODE , SUBJECT1 , SUBJECT2 , SUBJECT3 , (SUBJECT1+SUBJECT2+SUBJECT3) AS TOTAL_MARKS FROM STUDENT_MARKS;


3.
select student_code as "code" , subject1 , subject2 , subject3 , subject1+subject2+subject3 as "Total marks" from student_marks;


4.
select sm.staff_name , sm.staff_code , sm.dept_code , dm.design_code , dm.design_name from staff_masters sm join  designation_masters dm on sm.design_code = dm.design_code where dm.design_name in ('Professor','Lecturer');


5.   
 select staff_code , staff_name , dept_code from staff_masters where months_between(current_date,hiredate)/12  > 18 ;


6.
select sm.staff_name , dm.design_name from staff_masters sm join designation_masters dm on sm.design_code = dm.design_code where hiredate < to_date('2003-01-01' , 'YYYY-MM-DD');


7.
select sm.staff_name as "Name" , dm.design_name as "Designation Name", sm.staff_sal*12*10 as "Salary" from staff_masters sm join designation_masters dm on sm.design_code = dm.design_code where sm.dept_code in (10,30);


8.select sm.staff_name as "NAME"  , TRUNC(months_between(current_date , hiredate)/10) as "Experience" from staff_masters sm join designation_masters dm on sm.design_code = dm.design_code where dm.design_name = 'Lecturer';


9. select staff_name || ' , ' || dept_code as "Student_info" from staff_masters;


10.select staff_name as "Name" , staff_sal as "Salary" from staff_masters where staff_sal between 12000 and 25000 order by staff_sal , staff_name;


11.select staff_name as "name" from staff_masters where mgr_code is null;

12. select student_name , dept_code , student_dob from student_masters where student_dob between '01-JAN-1981' and '31-MAR-1983' order by student_dob;


13*.  select sm.dept_code , sum(sm.satff_sal) from staff_masters sm , designation_masters dm where sm.design_code = dm.design_code and dm.design_name != 'MANAGER' and sm.staff_sal > 20000;

14*

15.select student_code , nvl(to_char(dept_code) , 'No Department') as department from student_masters;

16.
select  staff_name ,staff_sal, lpad('X',staff_sal/10000,'X') as salary from staff_masters;




SINGLE ROW FUNCTION :
-----------------------------------------

1. select student_name  , to_char(student_dob,'MONTH D,YYYY') as birth_date from student_masters;

2. select  staff_name , TRUNC(months_between(current_date , hiredate)) as Months_Worked from staff_masters order by Months_Worked;

3.select * from staff_masters where staff_name like 'A%S';

4. select staff_name as name  , design_name  from staff_masters sm join designation_masters dm on sm.design_code = dm.design_code  where staff_name like '_n%s' or staff_name like '__n%s' or staff_name like '_n%n' or staff_name like '__n%n' ;


5. select staff_name , lpad(staff_sal ,15,'$') from staff_masters;

6. select staff_name from staff_masters where staff_name like '%_%';

7. select * from emp where to_char(hiredate , 'MM') = '12';

8. select staff_name as name , staff_sal as salary,
case when staff_sal >= 50000 then 'A'
when staff_sal >= 25000 and staff_sal<50000 then 'B'
when staff_sal <25000 and staff_sal >= 10000 then 'C'
else 'D'
END 
as grade from staff_masters;


9.  select staff_name , hiredate , to_char(hiredate , 'Day') as Day from staff_masters order by to_char(hiredate-1 , 'D');


10  select staff_name , lpad('*',length(staff_name),'*') from staff_masters;

11. select substr(staff_name ,1,1) || lpad('*',length(staff_name)-2,'*') || substr(staff_name , -1,1) from staff_masters;


12 select staff_name , staff_sal , hiredate , to_char(hiredate , 'DD') as day from staff_masters where to_char(hiredate , 'DD') < '16' ;


13. select staff_name , hiredate , to_char(hiredate , 'Day') as Day from staff_masters order by to_char(hiredate-1 , 'D');


14. select instr('mississippi','i',4,4) from dual;

15.	Write a query to find the pay date for the month. Pay date is the last Friday of the month. Display the date in the format “Twenty Eighth of January, 2002”. Label the heading as PAY DATE

15. select  to_char(next_day(last_day(current_date)-7,'Fri'),'DAY "of" FMMonth, YYYY') as Pay_Date from dual;

16 select max(staff_sal) as maximum , min(staff_sal) as minimum, sum(staff_sal) as total, trunc(avg(staff_sal)) as average from staff_masters;

17. select  dm.dept_name , dm.dept_code,  max(sm.staff_sal) as maximum , min(sm.staff_sal) as minimum, sum(sm.staff_sal) as total, trunc(avg(sm.staff_sal)) as average from staff_masters sm inner join department_masters dm on sm.dept_code = dm.dept_code group by dm.dept_code,dm.dept_name;

18. select dm.dept_code , dm.dept_name , count(sm.staff_name) as count from staff_masters sm  inner join  department_masters dm on    sm.dept_code = dm.dept_code group by dm.dept_code,dm.dept_name;


19. SELECT COUNT(MGR_CODE) as "Total Number of Managers" FROM STAFF_MASTERS GROUP BY MGR_CODE;

20. 

