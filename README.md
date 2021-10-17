# cloud_computing MicroTarea 2

Antes de generar la base de datos se creó un nuevo KEYSPACE con el siguiente comando:
```
CREATE KEYSPACE cloud_computing
WITH REPLICATION = {'class':'SimpleStrategy', 'replication_factor' : 3};
```
y para entrar a esta KEYSPACE se utilizó el comando:
```
use cloud_computing
```
1. Para crear una tabla en Cassandra se utiliza el siguiente comando:
```
CREATE TABLE users_by_city ( 
	city text, 
	last_name text, 
	first_name text, 
	address text, 
	email text, 
	PRIMARY KEY ((city), last_name, first_name, email));
```
2. Para insertar datos en la tabla creada se utiliza el siguiente comando:
```
INSERT INTO users_by_city 
  (city,last_name,first_name,email,address)
  VALUES('City','LastName','FirstName','Email','Adress');
```
3. Las queries utilizadas en el documento son las siguientes:
```
SELECT * FROM users_by_city WHERE city='Phoenix';
SELECT * FROM users_by_city WHERE city='Seattle';
```
