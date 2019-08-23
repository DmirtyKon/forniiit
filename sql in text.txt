/* предполагается, что база данных и таблица в ней уже выбраны */

/* 1.1 */
SELECT id, name, city  
FROM employee
ORDER BY name
WHERE city LIKE "А*" ;

/* 1.2 */
SELECT id, name, birthday
FROM employee
ORDER BY name
WHERE city LIKE "А*" ;

/* 1.3 */
select id, name, MAX(salary) from employee 
WHERE salary NOT IN (select MAX(salary) from employee );
select MIN(salary) from employee 
WHERE salary NOT IN (select MAX(salary) from employee );

/* 1.4 */
SELECT department_id, MAX(salary) 
FROM employee  
GROUP BY department_id