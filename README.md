# Sql1

1. Problem 1: Big Countries (https://leetcode.com/problems/big-countries/)

select name, population, area from World where area >= 3000000 or population >= 25000000;

2. Problem 2: Nth Highest Salary (https://leetcode.com/problems/nth-highest-salary/)

CREATE FUNCTION getNthHighestSalary(N INT) RETURNS INT
BEGIN
    DECLARE M INT;
    SET M = N-1;
  RETURN (
     # Write your MySQL query statement below.
       SELECT DISTINCT SALARY FROM EMPLOYEE ORDER BY SALARY DESC LIMIT M,1
 );
END

3. Problem 3: Delete Duplicate Emails (https://leetcode.com/problems/delete-duplicate-emails/)

DELETE T1 FROM PERSON T1 CROSS JOIN PERSON T2 WHERE T1.email = T2.email AND T1.id > T2.id
