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

### Paso 6: 
## 8. Resultado esperado:
### Evidencia:
<imag

## 9. Conclusión:

## 10. Bibliografía



