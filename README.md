CREATE DATABASE my_company_database;

CREATE TABLE employees (
id INT AUTO_INCREMENT, 
birth_date DATETIME,
first_name VARCHAR (25),
last_name VARCHAR (25),
gender VARCHAR (10),
PRIMARY KEY(id)
);

ALTER TABLE employees ADD salary VARCHAR (50000);
ALTER TABLE employees ADD title VARCHAR (25);
ALTER TABLE employees ADD title_date DATE;
ALTER TABLE employees MODIFY COLUMN title_date DATETIME;

INSERT INTO employees (first_name, last_name, salary, gender, title, title_date) values
('Miguel', 'Herrera', '5000', 'male', 'Barista', '2020-03-17'),
('Miguel', 'Herrera','6000', 'male', 'Translator', '2020-05-18'), 
('Miguel', 'Herrera','7000', 'male', 'Lawyer', '2020-09-12'),
('Daniel', 'Miguelez','8000', 'male', 'Plumber', '2020-05-16'),
('Peppa', 'Pig','9000', 'non-binary', 'Teacher', '2020-06-06'),
('Laura', 'Argente','10000', 'female', 'Doctor', '2014-09-17'),
('Claudia', 'Mobilia','20000', 'female', 'Nurse', '2018-02-18'),
('Hadi', 'Samadi','30000', 'male', 'Professor', '2015-12-12'),
('Pascual', 'Bellros','40000', 'male', 'Baker', '2019-06-17'),
('Patricia', 'Mengual','50000', 'female', 'Lawyer', '1985-04-17'),
('Marta', 'Enguidanos','30000', 'female', 'Nurse', '1980-09-16'),
('Arturo', 'Valls','8000', 'male', 'Journalist', '1990-10-26'),
('Carla', 'Otelo','6000', 'female', 'Fullstack', '2010-03-25'),
('Sami', 'Hassanzada','16000', 'male', 'Dentist', '2015-06-12'),
('Charo', 'Villanueva','18000', 'female', 'Doctor', '1980-03-17');

UPDATE employees SET first_name='Pepito' WHERE id=15;

SELECT * FROM employees WHERE salary >=20000;
SELECT * FROM employees WHERE salary <=10000;
SELECT * FROM employees WHERE salary BETWEEN 14000 AND 50000;
SELECT * FROM employees WHERE salary >=20000;
SELECT COUNT(*) FROM employees;
SELECT * FROM employees WHERE title_date BETWEEN 2019-01-01 AND 2019-12-31;
SELECT UCASE(first_name) FROM employees;
SELECT DISTINCT first_name FROM employees;

DELETE FROM employees WHERE id=5;
DELETE FROM employees WHERE salary >20000;