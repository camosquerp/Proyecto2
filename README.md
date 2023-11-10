# Proyecto2

# Guía para Configurar Kubernetes con MySQL y WordPress:
 
### Estudiante(s): 

nombres: - Andres Guerra MOntoya, - Juan Esteban Cardona, - Carlos Andres Mosquera.

### Profesor: Edwin Nelson Montoya.

# 1. breve descripción de la actividad:
En esta actividad, se monta un cluster de kubernetes de gcp con una aplicacion de wordpress conectada a base de MySQL, donde su direccion ip externa esta conectada con un dominio 

- Se configura el cluster 
![PHOTO-2023-11-08-19-39-40](https://github.com/camosquerp/Proyecto2/assets/68928380/dbd582a0-f407-4f3e-9322-2cb38945cf49)


- Se instala el wordpress dentro del cluster 
![PHOTO-2023-11-08-19-40-24](https://github.com/camosquerp/Proyecto2/assets/68928380/011d50e8-c14b-4d41-b0bf-398e7dc8f632)

- Se crea la base de datos para el wordpress 
![PHOTO-2023-11-08-19-40-36](https://github.com/camosquerp/Proyecto2/assets/68928380/38ac85b3-2764-4d44-91ae-00b50cd62641)

-Se genera la ip externa (34.73.73.173)
![PHOTO-2023-11-08-19-40-51](https://github.com/camosquerp/Proyecto2/assets/68928380/b984a640-1c30-4ce1-b1f2-23afdf81ca41)

- Se generan las credenciales del wordpress
![PHOTO-2023-11-08-19-41-46](https://github.com/camosquerp/Proyecto2/assets/68928380/9901cdb0-801b-4dfc-a8c6-225a2da9318d)

- Se genera el wordpress 
![PHOTO-2023-11-09-13-22-45](https://github.com/camosquerp/Proyecto2/assets/68928380/18afb89e-db53-4c0d-947d-babc948e2c49)

-Se verifica la base de datos activa 
![PHOTO-2023-11-09-13-26-15](https://github.com/camosquerp/Proyecto2/assets/68928380/7d602fa5-af63-4fd5-8aff-93e812f91a3f)

- crea y se asocia el domino con la ip externa
![PHOTO-2023-11-09-13-40-26](https://github.com/camosquerp/Proyecto2/assets/68928380/42e30db0-1bdc-4f32-bc60-34f55e9d9750)

- se trata hacer la configuracion del sertificado ssl
![PHOTO-2023-11-09-17-37-33](https://github.com/camosquerp/Proyecto2/assets/68928380/01b1cff7-c1db-40b8-b856-3e6c09978ff6)

![PHOTO-2023-11-09-17-36-59](https://github.com/camosquerp/Proyecto2/assets/68928380/91dbc856-7d58-4ae3-ad0b-2ff28904e85e)

# 2. información general de diseño de alto nivel, arquitectura, patrones, mejores prácticas utilizadas.

- La arquitectura se basa en microservicios y sigue el modelo cliente-servidor:

- MySQL: Se despliega como un contenedor que ejecuta un servidor MySQL.

- WordPress: Se despliega como otro contenedor que contiene la aplicación WordPress. Este contenedor se comunica con el servidor MySQL para almacenar y recuperar datos.

- Balanceador de Carga: El servicio de WordPress se expone externamente utilizando un balanceador de carga. Para el uso de la IP Externa.

# 3. Descripción del ambiente de desarrollo y técnico: lenguaje de programación, librerias, paquetes, etc, con sus numeros de versiones.

- Kubernetes.
- vztl
- -sql google cloud 

# 4. Descripción del ambiente de EJECUCIÓN (en producción) lenguaje de programación, librerias, paquetes, etc, con sus numeros de versiones.

