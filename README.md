
Conexión de Contenedores PostgreSQL y pgAdmin en Docker
1. Requisitos
•	Docker debe estar instalado y en ejecución en el sistema.
2. Crear Red Docker Personalizada
Para facilitar la comunicación entre los contenedores, crearemos una red Docker personalizada llamada pg-network.
 

3. Configurar el Contenedor de PostgreSQL
Comando Docker
El siguiente comando iniciará un contenedor de PostgreSQL en la red pg-network y configurará las credenciales de la base de datos.

 



4. Configurar el Contenedor de pgAdmin
Comando Docker
El siguiente comando inicia un contenedor de pgAdmin en la red pg-network y configura los datos de acceso.
 
5. Configuración de pgAdmin para Conectar con PostgreSQL
1.	Accede a pgAdmin en http://localhost:8080.
2.	Inicia sesión con las credenciales admin@admin.com y admin.
3.	En pgAdmin, crea una nueva conexión de servidor:
o	Name: Nombre de tu preferencia.
o	Host: postgres-container (nombre del contenedor de PostgreSQL).
o	Port: 5432.
o	Username: kevin.
o	Password: kevin.





6. Verificación de la Conexión
Una vez creada la conexión en pgAdmin, el contenedor pgadmin-container debería poder acceder a la base de datos en postgres-container.
 


