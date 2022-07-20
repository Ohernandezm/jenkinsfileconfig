# Informe de pruebas ejecutadas:

En el siguiente informe se muestran las pruebas ejecutadas en cada uno de los microservicios proporcionados, desde el empaquetado a la pruebas de endpoints. 

En las pruebas de microservicio se utilizaron las siguientes herramientas:
* __Docker__ utilizado para la ejecución del microservicio conterizado.
* __Postman__ para realizar la prueba de funcionamiento de los endpoint.
* __Maven__ para el compilado de la imagen.

Para cada microservicio se realizó los siguientes pasos:

1. Prueba de compilar la aplicación con __Maven__.

&nbsp; `` mvn -f pom.xml clean package ``
 
2. Construimos la imagen del contenedor con __Docker__

&nbsp; `` docker build -t nombreservice . ``
 
3. Levantar contenedor

&nbsp; `` docker run -d -p 8080:8080 --name orders nombreservice  ``

4. Probar endpoints en __Postman__

 
## Payments Service:

Compilado de aplicación:
mvn -f pom.xml clean package
![image](https://user-images.githubusercontent.com/12714366/179889261-6cb80eb9-a964-4047-91ef-8a9fb7dfef13.png)


Creación de imagen docker:
docker build -t paymentsservice .
![image](https://user-images.githubusercontent.com/12714366/179889306-4498d210-0c31-4d87-bb02-dc2ce5cba4b6.png)


Ejecucion de imagen creada:
docker run -d -p 8080:8080 --name payments paymentsservice

Prueba endpoints


