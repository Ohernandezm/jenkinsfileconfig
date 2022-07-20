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

![image](https://user-images.githubusercontent.com/12714366/179897538-82f1046f-d53c-4b4e-93bc-ac882b29355d.png)

Ejecucion de imagen creada:

``docker run -d -p 8080:8080 --name payments paymentsservice``

![image](https://user-images.githubusercontent.com/12714366/179897584-bc535965-6c95-4efa-9d14-0b0fe648e26c.png)

Prueba endpoints __Postman__

* metodo -> ``POST``
* baseUrl -> ``localhost:8084/payments/1``

![image](https://user-images.githubusercontent.com/12714366/179898158-9f30aff7-f349-40d8-8203-e4f4ff255da3.png)



## Products Service:

Compilado de aplicación:

``mvn -f pom.xml clean package`` 

![image](https://user-images.githubusercontent.com/12714366/179894481-7f0371c7-dca5-4592-85f7-b8779c0c7937.png)


Creación de imagen docker:

``docker build -t productsservice .`` 

![image](https://user-images.githubusercontent.com/12714366/179897417-cd3e20de-22f2-4815-8f1d-e0dff530aa18.png)

Ejecucion de imagen creada:

``docker run -d -p 8080:8080 --name payments productsservice``

![image](https://user-images.githubusercontent.com/12714366/179897457-e5578ac9-3878-4080-adce-cd4d74cd203b.png)

Prueba endpoints __Postman__ 

* metodo -> ``GET``
* baseUrl -> ``localhost:8083/products/123``

![image](https://user-images.githubusercontent.com/12714366/179897911-f4be06ed-e3ff-4341-8687-b8d5d41be048.png)


## Shipping Service:

Compilado de aplicación:

``mvn -f pom.xml clean package`` 

![image](https://user-images.githubusercontent.com/12714366/179894756-01cc3548-864b-4035-bd91-c8be23100008.png)


Creación de imagen docker:

``docker build -t shippingssservice .`` 

![image](https://user-images.githubusercontent.com/12714366/179896991-1c73a6eb-1810-40bd-b8e9-23e4e3597e15.png)


Ejecucion de imagen creada:

``docker run -d -p 8080:8080 --name payments shippingssservice``

![image](https://user-images.githubusercontent.com/12714366/179897253-90c64cc8-d861-4312-bf56-9f90a99736f8.png)

Prueba endpoints __Postman__ 

* metodo -> POST
* baseUrl -> 


## Orders Service:

Compilado de aplicación:

``mvn -f pom.xml clean package`` 

![image](https://user-images.githubusercontent.com/12714366/179895181-3612a1ae-e986-44a7-a757-b85102f6bf41.png)

Creación de imagen docker:

``docker build -t ordersservice .`` 

![image](https://user-images.githubusercontent.com/12714366/179897129-5df60a76-16cf-4b8a-8522-0ae1e8ca0a52.png)

Ejecucion de imagen creada:

``docker run -d -p 8080:8080 --name payments ordersservice``

![image](https://user-images.githubusercontent.com/12714366/179897320-df6d9115-6c07-465d-b7f6-d0068db4a716.png)

Prueba endpoints __Postman__ 

* metodo -> POST
* baseUrl -> 


