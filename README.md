# Project_Unisangil
Sistema de gestion para una comercializadora de productos frutales con bases de datos: MolinoFruit
1. ¿Por qué lo vamos a realizar?
El proyecto MolinoFruit se crea para optimizar la gestión de un negocio de frutas mediante un sistema digital integrado. Actualmente, el negocio enfrenta desafíos como la falta de integración entre las áreas operativas, dificultades en el control del inventario, gestión ineficaz de ventas y clientes, y la necesidad de generar reportes precisos. El objetivo es solucionar estos problemas con una plataforma que automatice los procesos, reduzca errores y mejore la toma de decisiones, ademas al producir y vender productos perecederos resulta en la perdida de dinero.

2. ¿Para qué lo vamos a realizar?
Automatizar el Control de Inventario: Seguimiento preciso del stock de productos, incluyendo entradas y salidas.
Gestión de Ventas: Registro y procesamiento eficiente de ventas, generación de reportes y gestión de pagos.
Administración de Clientes: Registro detallado de clientes y sus compras para mejorar la atención.
Generación de Reportes: Creación de reportes en formato PDF sobre ventas, productos y clientes.
Optimización de Procesos: Reducción de la intervención manual en la gestión de ventas, inventarios y clientes.

3. ¿Cómo se va a realizar?
Definición de requisitos, diseño de arquitectura y módulos, y planificación de la implementación.
Programación de funcionalidades utilizando las tecnologías seleccionadas. Esto incluye la interfaz de usuario, lógica de negocio e integración con la base de datos.
Mantenimiento y Soporte: Soporte técnico y mantenimiento continuo para resolver problemas y realizar mejoras.

5. Lenguaje y Tecnologías Utilizadas
Lenguaje de Programación: Java. Elegido por su robustez, portabilidad y soporte en la comunidad de desarrollo.
Frameworks y Librerías:
JPA (Java Persistence API): Para la gestión de la persistencia de datos.
Hibernate: Implementación de JPA para facilitar la interacción con la base de datos.
Java Swing: Para la creación de la interfaz gráfica de usuario.
iText: Para la generación de reportes en formato PDF.
Base de Datos: MySQL. Utilizado para el almacenamiento y gestión de la información del negocio.
Herramientas de Desarrollo: Netbeans o Visual Estudio Code para el desarrollo, y Maven para la gestión de dependencias y construcción del proyecto.


Módulo de Clientes

Registro de nuevos clientes.
Actualización de datos de clientes existentes.
Consulta y eliminación de clientes.
Entidades:
Cliente con atributos como ID, nombre, celular, edad y dirección.

Módulo de Productos

Registro de nuevos productos.
Actualización de información de productos existentes.
Consulta y eliminación de productos.
Entidades:
Producto con atributos como ID, nombre, categoría, descripción, precio unitario y cantidad disponible.
Relación: Cada producto está asociado a un cliente (uncliente).

Módulo de Ventas

Registro de nuevas ventas.
Consulta de ventas realizadas.
Generación de reportes de ventas.
Entidades:
Venta con atributos como ID de venta, cliente, total de la venta y fecha de venta.
Relaciones:
Cada venta está asociada a un cliente (cliente).
Cada venta puede incluir múltiples productos.

Módulo de Reportes

Creación de reportes sobre ventas realizadas.
Reportes detallados de productos y clientes.
Herramientas:
Utiliza la biblioteca iText para la generación de PDFs.

Módulo de Trabajadores

Registro de nuevos trabajadores.
Actualización de datos de trabajadores existentes.
Consulta y eliminación de trabajadores.
Entidades:
Trabajador con atributos como ID, nombre, cargo, y salario.

2. Diseño de Conexión entre Módulos
Clientes y Productos

Los productos están asociados a un cliente (uncliente). Esto puede ser útil para llevar un registro de qué cliente tiene qué producto o para ventas personalizadas.
Conexión: Cuando se registra una venta, se debe seleccionar el cliente y los productos involucrados en esa venta.
Clientes y Ventas

Las ventas están asociadas a un cliente (cliente). Esto permite saber qué cliente realizó cada venta.
Conexión: Para generar un reporte de ventas, se necesita consultar la información de los clientes y los detalles de sus compras.
Productos y Ventas

Las ventas incluyen productos específicos. Cada venta puede contener múltiples productos.
Conexión: Al generar reportes de ventas, se deben incluir detalles sobre los productos vendidos en cada transacción.
Generación de Reportes

