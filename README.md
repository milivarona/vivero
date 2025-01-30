📌 Base de Datos: Vivero
📖 Descripción
La base de datos Vivero gestiona la información de un vivero comercial, incluyendo empleados, clientes, pedidos, productos y pagos. Está diseñada para facilitar la administración de las ventas y el control del inventario.

🏗️ Estructura de la Base de Datos
La base de datos cuenta con 7 tablas principales:

oficina: Almacena la información de las oficinas del vivero.

empleado: Registra los empleados y sus relaciones jerárquicas.

cliente: Contiene los datos de los clientes.

pago: Registra los pagos realizados por los clientes.

pedido: Gestiona los pedidos realizados por los clientes.

gama_producto: Define las distintas categorías de productos.

producto: Almacena los productos disponibles en el vivero.

detalle_pedido: Relaciona los pedidos con los productos adquiridos.

🔗 Relaciones Clave:
Un empleado puede tener un jefe dentro de la misma tabla.

Cada empleado está asignado a una oficina.

Un cliente está asociado a un empleado que lo atiende.

Un cliente puede realizar varios pedidos y pagos.

Un pedido contiene varios productos a través de detalle_pedido.

Cada producto pertenece a una gama de productos.

🚀 Instalación y Uso
🔹 1. Creación de la Base de Datos
Para crear la base de datos en MySQL, ejecuta el siguiente script que ya viene con el archivo .sql:

CREATE DATABASE IF NOT EXISTS vivero;
USE vivero;
🔹 2. Creación de las tablas
Una vez creada la base de datos, procede a ejecutar una por una la creación de las distintas tablas para evitar posibles problemas, ejemplo:

CREATE TABLE IF NOT EXISTS oficina (
    id_oficina INT PRIMARY KEY AUTO_INCREMENT,
    codigo_oficina VARCHAR(10),
    ciudad VARCHAR(30),
    país VARCHAR(50),
    region VARCHAR(50),
    codigo_postal VARCHAR(10),
    telefono VARCHAR(20)
);
🔹 3. Insertar valores en las tablas
Una vez creadas todas las tablas, al final del archivo se encuentran los INSERT INTO, para ir agregando los valores a las mismas, ejemplo:

INSERT INTO oficina VALUES (1, 'BCN-ES','Barcelona','España','Barcelona','08019','+34 93 3561182');
🔹 4. Comprobar que los valores se hayan ingresado
Luego de ejecutar todos los INSERT INTO, se puede ejecutar una consulta SELECT, para comprobar que los valores se hayan agregado correctamente:

SELECT * FROM cliente;
🔥 Consideraciones
La tabla empleado tiene una relación jerárquica con sí misma (cada empleado puede tener un jefe).

La tabla detalle_pedido funciona como una tabla intermedia para registrar los productos dentro de un pedido.

Estas instrucciones están pensadas para el entorno de MySQL Workbench, en caso de utilizar un Sistema de Gestion de Base de Datos distinto, los pasos o comandos podrían llegar a cambiar.

🛠️ Contribuciones y Soporte
Gracias por visitar este proyecto de base de datos. Si te resultó útil, acá te dejo algunas formas en las que podes mostrar tu apoyo;

⭐ Dale una estrella
Si te gustó este proyecto podes darle una ⭐ a este repositorio. Esto ayuda a que más compañeros puedan encontrar este proyecto.
