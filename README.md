# SQL

 1. Вывести все поля и все строки.
 SELECT * from classicmodels.employees;
 ![a66064b015](https://user-images.githubusercontent.com/117518577/214374689-f0c19992-41ec-4f88-a43a-7c4aae04609e.jpg)

 2. Вывести все имена в таблице
SELECT firstName from classicmodels.employees;
![e8f401dbea](https://user-images.githubusercontent.com/117518577/214495306-576696eb-bdd9-4bdc-8d40-dd73259db904.jpg)

 3. Вывести только employeeNumber пользователей
SELECT employeeNumber from classicmodels.employees;
![808498b9e9](https://user-images.githubusercontent.com/117518577/214493536-0803724d-8db8-4a7d-861e-dfcbbf347f06.jpg)

 4. Вывести только фамилии пользователей
SELECT lastName from classicmodels.employees;
![17827ff584](https://user-images.githubusercontent.com/117518577/214493170-2e98fc67-8882-4e25-9c59-3ad3a1d47451.jpg)

 5. Вывести только email пользователей
SELECT email from classicmodels.employees;
![a71a353392](https://user-images.githubusercontent.com/117518577/214494302-c7b3be45-f719-4733-9be8-5122c2485b15.jpg)

 6. Вывести имя и email пользователей
SELECT firstName, email from classicmodels.employees;
![f856e74e98](https://user-images.githubusercontent.com/117518577/214495396-bd87c970-0655-4df4-96e9-29cbac628184.jpg)

 7. Вывести employeeNumber, имя, email и extension пользователей
SELECT employeeNumber, lastName, email, extension from classicmodels.employees;
![5d1fc6092a](https://user-images.githubusercontent.com/117518577/214492530-2a0ed267-7b33-4e4f-b6e5-49b8530f66df.jpg)

 8. Вывести пользователей где extension -   'x101'
SELECT firstName, extension from classicmodels.employees where extension = 'x101';
 9. Вывести пользователей у которых reportsTo равен 1102
SELECT firstName, reportsTo from classicmodels.employees where reportsTo = '1102';
![a15bce9b25](https://user-images.githubusercontent.com/117518577/214494138-207e9446-9b5d-4c72-b56e-65969e1636ba.jpg)

 10. Вывести пользователей где в имени есть слово  Leslie
 SELECT firstName, lastName from classicmodels.employees where firstName = 'Leslie'
 ![4a9a9a3ed6](https://user-images.githubusercontent.com/117518577/214492454-322e9964-94e1-4949-b4f7-2d0529986905.jpg)

11. Вывести пользователей где в имени в конце есть Yue  в таблице employees
SELECT firstName from classicmodels.employees where firstName like '%Yue';
![7c488272f8](https://user-images.githubusercontent.com/117518577/214492860-bd2c40b9-c110-4305-bf7b-ab6e69afcc8c.jpg)

 12. Вывести пользоватеей где в имени в есть буква а
SELECT firstName from classicmodels.employees where firstName like '%a%';
![2912466e4a](https://user-images.githubusercontent.com/117518577/214493985-5e6d3f70-685f-4c76-837a-bff99f2a2ed4.jpg)

 13. Вывести пользователей у которых officeCode равен 6
SELECT firstName, officeCode from classicmodels.employees where officeCode = '6';
![ad0723b743](https://user-images.githubusercontent.com/117518577/214494409-3fa41ae4-418a-4a46-aa12-a6df0ce4c874.jpg)

 14. Вывести customerNumber у которых paymentDate создан '2004-03-01' и имеет checkNumber - 'NM916675'
SELECT customerNumber, paymentDate from classicmodels.payments where paymentDate = '2004-03-01' or checkNumber = 'NM916675';
![153a6100f9](https://user-images.githubusercontent.com/117518577/214493016-3aaf19b5-738d-40a9-9aed-abba89bb844a.jpg)

15. Вывести всё по отдельности из каждой таблицы

SELECT * from classicmodels.customers; 
SELECT * from classicmodels.employees;
SELECT * from classicmodels.offices;
SELECT * from classicmodels.orderdetails;
SELECT * from classicmodels.orders;
SELECT * from classicmodels.payments;
SELECT * from classicmodels.productlines;
SELECT * from classicmodels.products;
![b61cc4898b](https://user-images.githubusercontent.com/117518577/214495164-450edf49-81ca-4955-bfe9-a0ac61c5884d.jpg)

16. показать всех клиентов в Норвегии
SELECT customerName,country from classicmodels.customers where country = 'Norway'
![iu](https://user-images.githubusercontent.com/117518577/214497311-ec25763d-c96c-4cd2-ba0c-85050fb8b8e9.jpg)

17. показать всех клиентов в Неваде из таблицы  customers
 SELECT customerName, state from classicmodels.customers where state = 'NV'; 
![505e982af1](https://user-images.githubusercontent.com/117518577/214493076-5a7e8dd3-1030-4339-a560-1b4b1ef4bbee.jpg)

18. показать всех клиентов с кредитным лимитом от 50 тыс. до 60 Тыс из таблицы  customers
SELECT customerName,creditLimit from classicmodels.customers where creditLimit between 50000 and 60000;
![6b348ea3ba](https://user-images.githubusercontent.com/117518577/214492649-df7daf7e-3de4-4b33-a642-143eeda987c6.jpg)

19. показать номера телефонов офисов в Сан-Франциско и Бостоне из таблицы  offices
SELECT phone, city from classicmodels.offices where city = 'San Francisco' or city = 'Boston'
![b0c2c097e2](https://user-images.githubusercontent.com/117518577/214495118-0892cbf9-7bf4-4972-ba99-857205e21a29.jpg)

20. показать город с нулевым штатом из таблицы offices
 SELECT * from classicmodels.offices where state is null;
![ff](https://user-images.githubusercontent.com/117518577/214497270-e0c0df6b-3201-4a8b-93ef-e14fd8f70584.jpg)

21. показать номера заказов в порядке наибольшего количества заказанных 
SELECT orderNumber,quantityOrdered from classicmodels.orderdetails order by orderNumber,quantityOrdered DESC;
![4141062228](https://user-images.githubusercontent.com/117518577/214493920-e1d7d77d-c3e1-4d45-b7cc-6950edc5ddb5.jpg)

22. показать заказы > 200 долларов из таблицы orderdetails
SELECT priceEach from classicmodels.orderdetails where priceEach >200;
![cty](https://user-images.githubusercontent.com/117518577/214496738-c451b12a-f83d-451c-941d-e71bb2272d4d.jpg)

23. какие статусы существуют в заказах из таблицы orders
SELECT status from classicmodels.orders status;
![MySQL Workbench](https://user-images.githubusercontent.com/117518577/214495584-28fd498f-15ff-4b09-b228-70e8117e5db0.jpg)

24. показать платежи >2005 из таблицы payments
SELECT paymentDate from classicmodels.payments where paymentDate >2005 ;
![MySQL Workbenchhhg](https://user-images.githubusercontent.com/117518577/214496018-5b5a8812-59d4-4746-bef6-a167a6e8856e.jpg)

25. показать описание продуктовых линеек для судов и поездов   из таблицы  productlines
SELECT * from classicmodels.productlines where productLine in ('ships', 'trains') ;
![MySQL Workbench ка](https://user-images.githubusercontent.com/117518577/214495917-0fe12308-ee4c-4b8f-972f-f97dad0a89d4.jpg)

26. показать отдельные продуктовые линейки в порядке возрастания из таблицы products  
SELECT productLine from classicmodels.products order by productLine;
![MySQL Workbenchh](https://user-images.githubusercontent.com/117518577/214495988-b0556966-6541-4561-adc9-3efe5664269a.jpg)

27. какие продуктовые линейки существуют для BMW? Из таблицы products 
SELECT productName, productLine from classicmodels.products where productName like '%BMW%' ; 
![Приложению meet google com предоставлен доступ к вашему экрану](https://user-images.githubusercontent.com/117518577/214496066-a5f72371-7a72-40d6-b5a9-2be909d3f2ce.jpg)

28. показать имена всех VP из таблицы employees 
SELECT lastName,jobTitle from classicmodels.employees where jobTitle like '%VP%' ;
![dhjgsd](https://user-images.githubusercontent.com/117518577/214495228-7f0adcd3-ae2a-48ad-8ece-593849c10b62.jpg)
