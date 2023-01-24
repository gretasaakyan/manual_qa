# SQL

 1. Вывести все поля и все строки.
 SELECT * from classicmodels.employees;
 2. Вывести все имена в таблице
SELECT firstName from classicmodels.employees;
 3. Вывести только employeeNumber пользователей
SELECT employeeNumber from classicmodels.employees;
 4. Вывести только фамилии пользователей
SELECT lastName from classicmodels.employees;
 5. Вывести только email пользователей
SELECT email from classicmodels.employees;
 6. Вывести имя и email пользователей
SELECT firstName, email from classicmodels.employees;
 7. Вывести employeeNumber, имя, email и extension пользователей
SELECT employeeNumber, lastName, email, extension from classicmodels.employees;
 8. Вывести пользователей где extension -   'x101'
SELECT firstName, extension from classicmodels.employees where extension = 'x101';
 9. Вывести пользователей у которых reportsTo равен 1102
SELECT firstName, reportsTo from classicmodels.employees where reportsTo = '1102';
 10. Вывести пользователей где в имени есть слово  Leslie
 SELECT firstName, lastName from classicmodels.employees where firstName = 'Leslie'
11. Вывести пользователей где в имени в конце есть Yue  в таблице employees
SELECT firstName from classicmodels.employees where firstName like '%Yue';
 12. Вывести пользоватеей где в имени в есть буква а
SELECT firstName from classicmodels.employees where firstName like '%a%';
 13. Вывести пользователей у которых officeCode равен 6
SELECT firstName, officeCode from classicmodels.employees where officeCode = '6';

 14. Вывести customerNumber у которых paymentDate создан '2004-03-01' и имеет checkNumber - 'NM916675'
SELECT customerNumber, paymentDate from classicmodels.payments where paymentDate = '2004-03-01' or checkNumber = 'NM916675';
15. Вывести всё по отдельности из каждой таблицы

SELECT * from classicmodels.customers; 
SELECT * from classicmodels.employees;
SELECT * from classicmodels.offices;
SELECT * from classicmodels.orderdetails;
SELECT * from classicmodels.orders;
SELECT * from classicmodels.payments;
SELECT * from classicmodels.productlines;
SELECT * from classicmodels.products;
