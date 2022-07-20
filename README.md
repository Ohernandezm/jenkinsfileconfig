# Informe de pruebas ejecutadas:

En el siguiente informe se muestran las pruebas ejecutadas en cada uno de los microservicios proporcionados, desde el empaquetado a la pruebas de endpoints. 

En las pruebas de microservicio se utilizaron las siguientes herramientas:
* __Docker__ utilizado para la ejecución del microservicio conterizado.
* __Postman__ para realizar la prueba de funcionamiento de los endpoint.
* __Maven__ para el compilado de la imagen.

Para cada microservicio se realizó los siguientes pasos:

1. Prueba de compilar la aplicación con __Maven__.

- `` mvn -f pom.xml clean package ``
 
2. Construimos la imagen del contenedor con __Docker__

- `` docker build -t nombreservice . ``
 
3. Levantar contenedor

- `` docker run -d -p 8080:8080 --name orders nombreservice  ``

4. Probar endpoints en __Postman__

 
## Payments Service:

Compilado de aplicación:

``mvn -f pom.xml clean package``

![image](https://user-images.githubusercontent.com/12714366/179893328-6d7b1fe9-7ef5-4cfd-a7cf-fb17a5a4bcb9.png)


Creación de imagen docker:

``docker build -t paymentsservice .``




Ejecucion de imagen creada:

``docker run -d -p 8080:8080 --name payments paymentsservice``

Prueba endpoints __Postman__



## Products Service:

Compilado de aplicación:

``mvn -f pom.xml clean package`` 

![image](https://user-images.githubusercontent.com/12714366/179894481-7f0371c7-dca5-4592-85f7-b8779c0c7937.png)


Creación de imagen docker:

``docker build -t productsservice .`` 


Ejecucion de imagen creada:

``docker run -d -p 8080:8080 --name payments productsservice``

Prueba endpoints __Postman__ 


## Shipping Service:

Compilado de aplicación:

``mvn -f pom.xml clean package`` 

![image](https://user-images.githubusercontent.com/12714366/179894756-01cc3548-864b-4035-bd91-c8be23100008.png)


Creación de imagen docker:

``docker build -t shippingssservice .`` 


Ejecucion de imagen creada:

``docker run -d -p 8080:8080 --name payments shippingssservice``

Prueba endpoints __Postman__ 



## Orders Service:

Compilado de aplicación:

``mvn -f pom.xml clean package`` 

![image](https://user-images.githubusercontent.com/12714366/179895181-3612a1ae-e986-44a7-a757-b85102f6bf41.png)

Creación de imagen docker:

``docker build -t ordersservice .`` 



Ejecucion de imagen creada:

``docker run -d -p 8080:8080 --name payments ordersservice``



Prueba endpoints __Postman__ 
