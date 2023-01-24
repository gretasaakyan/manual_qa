# SQL

 1. Вывести все поля и все строки.
 SELECT * from classicmodels.employees;
 ![a66064b015](https://user-images.githubusercontent.com/117518577/214374689-f0c19992-41ec-4f88-a43a-7c4aae04609e.jpg)

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

16. показать всех клиентов в Норвегии
SELECT customerName,country from classicmodels.customers where country = 'Norway'

17. показать всех клиентов в Неваде из таблицы  customers
 SELECT customerName, state from classicmodels.customers where state = 'NV'; 

18. показать всех клиентов с кредитным лимитом от 50 тыс. до 60 
Тыс из таблицы  customers
SELECT customerName,creditLimit from classicmodels.customers where creditLimit between 50000 and 60000;

19. показать номера телефонов офисов в Сан-Франциско и Бостоне из таблицы  offices
SELECT phone, city from classicmodels.offices where city = 'San Francisco' or city = 'Boston'

20. показать город с нулевым штатом из таблицы offices
 SELECT * from classicmodels.offices where state is null;


21. показать номера заказов в порядке наибольшего количества заказанных 
SELECT orderNumber,quantityOrdered from classicmodels.orderdetails order by orderNumber,quantityOrdered DESC;

22. показать заказы > 200 долларов из таблицы orderdetails
SELECT priceEach from classicmodels.orderdetails where priceEach >200;

23. какие статусы существуют в заказах из таблицы orders
SELECT status from classicmodels.orders status;


24. показать платежи >2005 из таблицы payments
SELECT paymentDate from classicmodels.payments where paymentDate >2005 ;


25. показать описание продуктовых линеек для судов и поездов  (-- show descriiption of productLines for Ships and Trains)  из таблицы  productlines

SELECT * from classicmodels.productlines where productLine in ('ships', 'trains') ;

26. показать отдельные продуктовые линейки в порядке возрастания из таблицы products  
SELECT productLine from classicmodels.products order by productLine;

27. какие продуктовые линейки существуют для BMW? Из таблицы products 
SELECT productName, productLine from classicmodels.products where productName like '%BMW%' ; 

28. показать имена всех VP из таблицы employees 
SELECT lastName,jobTitle from classicmodels.employees where jobTitle like '%VP%' ;
