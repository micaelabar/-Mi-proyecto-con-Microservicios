# Mi proyecto con Microservicios
## 1. Tiempo de duración:
El tiempo estimado para el desarrollo del proyecto fue de 2 horas, desde la configuración del entorno hasta la ejecución inicial de los microservicios.
## 2. Fundamentos:
Este proyecto se basa en la arquitectura de microservicios, que permite el desarrollo de aplicaciones distribuidas compuestas por servicios independientes. Cada microservicio es desplegado de forma autónoma y se comunica con los demás mediante protocolos ligeros como HTTP (REST).
Los componentes clave aplicados en este proyecto son:
- Separación de responsabilidades: Cada servicio maneja una lógica de --negocio específica (clientes, créditos, notificaciones).
- Despliegue independiente: Los servicios se pueden ejecutar y escalar por separado.
- Eureka Server (Servicio descubridor): Permite registrar y localizar microservicios dinámicamente.
- API Gateway: Punto de entrada único para el enrutamiento, seguridad y balanceo de carga.
- Config Server: Centraliza la configuración de todos los servicios.
## 3. Conocimientos previos
Para el desarrollo del proyecto fue necesario contar con conocimientos en:
- Java y Spring Boot.
- Arquitectura de microservicios.
- Uso de herramientas como Maven, Gradle y Visual Studio Code.
- Manejo de dependencias y configuración de servicios con Spring Cloud.
## 4. Objetivo a alcanzar
Implementar una arquitectura de microservicios funcional que permita:
- La creación de servicios desacoplados y escalables.
- El consumo de servicios REST mediante llamadas HTTP.
- La gestión centralizada de configuraciones.
- La administración dinámica de rutas y servicios con ayuda de Eureka y el API Gateway.
## 5. Equipo necesario
- Computadora con Windows 10 o superior.
- Conexión a internet.
- Entorno de desarrollo (Visual Studio Code, JDK 17).
- Administrador de dependencias (Maven o Gradle).
- Terminal de comandos o PowerShell.
- Chocolatey para la instalación de Maven.
## 6. Material de apoyo:
- Documentación oficial de Spring Boot y Spring Cloud.
- Tutoriales de arquitectura de microservicios.
- Artículos sobre Eureka, Config Server y API Gateway.
- Herramienta Spring Initializr para generar el esqueleto del proyecto.
## 7. Procedimiento:
### Paso 1: Generar el proyecto base
Usando Spring Initializr, se generó el proyecto con las siguientes dependencias:
- Spring Boot DevTools
- Eureka Discovery Client
- Config Client
Configuración:
- Lenguaje: Java
- Versión: 3.5.3
- Empaquetado: JAR
- Versión de Java: 17
### Evidencia:
<imag!![1+](https://github.com/user-attachments/assets/4de50b08-abec-4dbd-9030-e38df67d1249)

### Paso 2: Crear los módulos del proyecto
```
mkdir config-server
mkdir eureka-server
mkdir api-gateway
mkdir servicio-clientes
mkdir servicio-creditos
mkdir servicio-notificaciones
````
### Evidencia:
<imag!![2](https://github.com/user-attachments/assets/b9b170e1-64dc-4725-a1d3-6a8471dc9c1e)

### Paso 3: Abrir y configurar el proyecto
Se intentó navegar a la carpeta del proyecto con cd demo, pero se presentó un error de ruta.
Luego, se abrió el proyecto con code . y se intentó ejecutar con Maven, mostrando error ya que Maven no estaba instalado.
### Evidencia:
<imag!![2 1](https://github.com/user-attachments/assets/7d8e3510-1ca0-47b4-af18-09eef55daf44)

### Paso 4: Instalar Maven
Se usó Chocolatey en PowerShell para instalar Maven con el comando:
```
choco install maven -y
````
### Evidencia:
<imag![3](https://github.com/user-attachments/assets/8c658a24-3840-4a2d-b7af-408b0760f8c8)

### Paso 5: Ejecución del proyecto Spring Boot con Maven
Una vez instalado Maven, se procede a ejecutar el proyecto Spring Boot ubicado en el directorio:
```
Tercer ciclo/cooperativa-san-juan-microservicios/demo
````
Esto se hace con el comando:
```
mvn spring-boot:run
````
### Evidencia:
<imag![4](https://github.com/user-attachments/assets/dc9d0420-d299-4e84-8bbb-bce764de2942)
<imag!![5](https://github.com/user-attachments/assets/78b6c5f4-1a65-460d-9329-8bd9369cdfcb)

### Paso 6: Verificación del panel de Eureka en el navegador
Una vez iniciado correctamente el servidor Eureka, se accede a la interfaz gráfica de Eureka mediante un navegador web, ingresando la siguiente URL:
```
http://localhost:8761
````
### Evidencia:
<imag![6](https://github.com/user-attachments/assets/c8482ed8-bca4-4ce7-9c36-2d6814c9e014)

### Paso 7: Implementación del servidor Eureka en el código fuente
Para habilitar un servidor Eureka con Spring Boot, se creó una clase principal llamada EurekaServerApplication.java, la cual se encuentra dentro del paquete:
```
com.cooperativa.sanjuan
````
### Evidencia:
<imag![7](https://github.com/user-attachments/assets/a3e11f8f-97ce-4a78-b8a9-2b078e465da3)

### Paso 8: Creación del microservicio cliente (clientes-service)
Para crear el microservicio clientes-service, se utilizó Spring Initializr con los siguientes parámetros:
```
Configuración del proyecto:
Project: Gradle - Groovy
Language: Java
Spring Boot: 3.5.3
Group: com.cooperativa
Artifact: clientes-service
Name: clientes-service
Package name: com.cooperativa.clientes-service
Java version: 17
Packaging: Jar
````
### Evidencia:
<imag!![8](https://github.com/user-attachments/assets/40683cde-1b0b-40b9-9243-2a77937f361b)
### Paso 9: Configuración del cliente Eureka (clientes-service)
El microservicio clientes-service fue creado con Spring Boot y configurado como un cliente Eureka, lo que le permite registrarse automáticamente en el servidor Eureka.

Clase principal: ClientesServiceApplication.java
### Evidencia:
<imag!![9](https://github.com/user-attachments/assets/5066d59f-7625-4627-a1d0-76f21f8dd4e3)

### Paso 10: Registro exitoso en Eureka
Significa que el cliente Eureka ya está comunicándose correctamente con el servidor Eureka ubicado en:
### Evidencia:
<imag![10](https://github.com/user-attachments/assets/51ff9d25-0794-42f1-8235-d44d4b584b7f)

## 8. Resultado esperado:
- Que los microservicios puedan registrarse en Eureka.
- Que desde el API Gateway se pueda consumir REST de forma centralizada.
- Que cada servicio pueda ejecutarse de manera independiente.
- Que el Config Server permita la gestión centralizada de propiedades de cada servicio.
## 9. Conclusión:
Este ejercicio práctico permitió aplicar los conceptos fundamentales de la arquitectura de microservicios en un entorno real. Se observaron las ventajas del desarrollo modular, el despliegue independiente y el uso de herramientas clave como Eureka, Config Server y API Gateway.
También se evidenció la importancia de contar con el entorno correctamente configurado (Maven, Java, Visual Studio Code) para evitar errores en la ejecución del proyecto.
## 10. Bibliografía
- Spring Boot Documentation: https://docs.spring.io/spring-boot/docs/current/reference/html/
- Spring Cloud Netflix Eureka: https://cloud.spring.io/spring-cloud-netflix/multi/multi_spring-cloud-eureka-server.html
- Baeldung: "Introduction to Spring Cloud Gateway"
- Chocolatey Documentation: https://docs.chocolatey.org/
- YouTube – Curso Spring Boot Microservicios (varios autores)




