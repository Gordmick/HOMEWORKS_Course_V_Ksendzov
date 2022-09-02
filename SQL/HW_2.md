![](https://timeweb.com/ru/community/article/6a/6aec84e99f708bc438b913c3089e18ae.png)

# _HOMEWORK 2 SQL DDL_
# in Postgre

 ## 1.  Создать таблицу employees
- id. serial,  primary key,
- employee_name. Varchar(50), not null
Наполнить таблицу employee 70 строками.
```sql
create table employees(
id serial primary key,
employee_name varchar(50) not null
);
insert into employees (employee_name)
values ('Ivan'),
       ('Piter'),
       ('Aala'),
       ('Aaleahya'),
       ('Aaleyah'),
       ('Aalijah'),
       ('Aaliyah'),
       ('Aaliyah'),
       ('Aamori'),
       ('Aanjay'),
       ('Aaralyn'),
       ('Aaric'),
       ('Aarika'),
       ('Aaron'),
       ('Aaron'),
       ('Aarshiya'),
       ('Aart'),
       ('Aart'),
       ('Aarthi'),
       ('Aarush'),
       ('Aarushi'),
       ('Aase'),
       ('Aashish'),
       ('Aashka'),
       ('Aasiya'),
       ('Aaylah'),
       ('Abagail'),
       ('Abaigael'),
       ('Abaigeal'),
       ('Aballach'),
       ('Aballach'),
       ('Byme'),
       ('Byme'),
       ('Byram'),
       ('Byrd'),
       ('Byrdene'),
       ('Byreleah'),
       ('Byrne'),
       ('Byrnes'),
       ('Byron'),
       ('Byron'),
       ('Byrtel'),
       ('Byrtwold'),
       ('Bysen'),
       ('Bysen'),
       ('Cabal'),
       ('Cabal'),
       ('Cabe'),
       ('Cable'),
       ('Cacamwri'),
       ('Cacamwri'),
       ('Cacanisius'),
       ('Cace'),
       ('Cacey'),
       ('Cacey'),
       ('Cachamwri'),
       ('Cachamwri'),
       ('Cacia'),
       ('Cadabyr'),
       ('Cadan'),
       ('Cadassi'),
       ('Cadby'),
       ('Cadda'),
       ('Cadenza'),
       ('Cadeo'),
       ('Cadha'),
       ('Cadhla'),
       ('Cadhla'),
       ('Cadi'),
       ('Cadie');

select * from employees;
```

## 2. Создать таблицу salary
- id. Serial  primary key,
- monthly_salary. Int, not null
## Наполнить таблицу salary 15 строками:
- 1000
- 1100
- 1200
- 1300
- 1400
- 1500
- 1600
- 1700
- 1800
- 1900
- 2000
- 2100
- 2200
- 2300
- 2400
- 2500
```sql
create table salary(
id serial primary key,
monthly_salary int not null
);
insert into salary (monthly_salary)
values (1000),
       (1100),
       (1200),
       (1300),
       (1400),
       (1500),
       (1600),
       (1700),
       (1800),
       (1900),
       (2000),
       (2100),
       (2200),
       (2300),
       (2400),
       (2500);
      
select * from salary;
```

## 3. Создать таблицу employee_salary
- id. Serial  primary key,
- employee_id. Int, not null, unique
- salary_id. Int, not null
## Наполнить таблицу employee_salary 40 строками:
- в 10 строк из 40 вставить несуществующие employee_id
```sql
create table employee_salary(
id serial primary key,
employee_id int unique not null,
salary_id int not null
);
insert into employee_salary(employee_id, salary_id)
values 	(1, 10),
		(5, 12),
		(7, 1),
		(10, 5),
		(11, 8),
		(13, 8),
		(20, 3),
		(21, 4),
		(25, 10),
		(30, 11),
		(35, 12),
		(37, 13),
		(40, 9),
		(41, 16),
		(45, 6),
		(47, 8),
		(51, 2),
		(53, 8),
		(55, 9),
		(58, 14),
		(60, 14),
		(61, 8),
		(62, 10),
		(63, 11),
		(64, 12),
		(65, 13),
		(66, 16),
		(67, 1),
		(68, 2),
		(69, 5),
		(71, 1),
		(72, 1),
		(73, 1),
		(74, 1),
		(75, 1),
		(76, 1),
		(77, 1),
		(78, 1),
		(79, 1),
		(80, 1);
	
select * from employee_salary;
```

## 4. Создать таблицу roles
- id. Serial  primary key,
- role_name. int, not null, unique
## Поменять тип столба role_name с int на varchar(30)
## Наполнить таблицу roles 20 строками:

```sql
create table roles(
id  serial primary key,
role_name int unique not null
);	

alter table roles
alter column role_name type varchar(30) using role_name::varchar(30);

insert into roles(role_name)
values 	('Junior Python developer'),
		('Middle Python developer'),
		('Senior Python developer'),
		('Junior Java developer'),
		('Middle Java developer'),
		('Senior Java developer'),
		('Junior JavaScript developer'),
		('Middle JavaScript developer'),
		('Senior JavaScript developer'),
		('Junior Manual QA engineer'),
		('Middle Manual QA engineer'),
		('Senior Manual QA engineer'),
		('Project Manager'),
		('Designer'),
		('HR'),
		('CEO'),
		('Sales manager'),
		('Junior Automation QA engineer'),
		('Middle Automation QA engineer'),
		('Senior Automation QA engineer');
	
select * from roles;	
```

5. Создать таблицу roles_employee
- id. Serial  primary key,
- employee_id. Int, not null, unique (внешний ключ для таблицы employees, поле id)
- role_id. Int, not null (внешний ключ для таблицы roles, поле id)
Наполнить таблицу roles_employee 40 строками:
```sql
create table roles_employee(
id serial primary key,
employee_id int unique not null,
role_id int not null,
foreign key (employee_id)
	references employees(id),
foreign key (role_id)
	references roles(id)
);		

insert into roles_employee (employee_id, role_id)
values 	(1, 10),
		(2, 1),
		(3, 1),
		(4, 1),
		(5, 12),
		(7, 1),
		(10, 5),
		(11, 8),
		(13, 8),
		(20, 3),
		(21, 4),
		(25, 10),
		(26, 1),
		(27, 1),
		(28, 1),
		(29, 1),
		(30, 11),
		(31, 1),
		(32, 1),
		(33, 1),
		(35, 12),
		(37, 13),
		(40, 9),
		(41, 16),
		(45, 6),
		(47, 8),
		(51, 2),
		(53, 8),
		(55, 9),
		(58, 14),
		(60, 14),
		(61, 8),
		(62, 10),
		(63, 11),
		(64, 12),
		(65, 13),
		(66, 16),
		(67, 1),
		(68, 2),
		(69, 5);
	
select * from roles_employee;	
```
