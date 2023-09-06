DELIMITER &&
CREATE procedure Salary5000()
BEGIN
SELECT first_name, last_name, job_title, salary
FROM employees 
WHERE salary>5000;
END && 
DELIMITER ;

Call Salary5000 () ;

DELIMITER //
CREATE procedure TOPnSalary (IN var int)
BEGIN
SELECT*
FROM employees
ORDER BY salary desc
LIMIT var;
END //
DELIMITER ;
 Call Topnsalary (5) ;
 
 DELIMITER //
 CREATE procedure Update_Salary(IN emp_name varchar (20), IN New_salary float)
 BEGIN
 UPDATE employees set salary = New_salary
 WHERE first_name = emp_name ;
 END //
 DELIMITER ;
 



