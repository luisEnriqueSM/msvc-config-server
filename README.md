# msvc-config-server

Configuraciones de ambiente para el servicio mscv-items usando spring-actuator.


# Comandos Docker para levantar el contenedor de msvc-products

```bash
# Limpiar, generar Jar file
.\mvnw clean package
 
 # Construir imagen
docker build -t config-server:v1 .

# Crear network
docker network create springcloud

# Correr contenedor
docker run -d -p 8888:8888 --name config-server --network springcloud config-server:v1



