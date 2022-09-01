# Servidor de configuración
Sección 6: Spring Cloud Config Server: centralizando la configuración

# Directorio donde se almacenarán archivos manejados por git
Por el momento, en la siguiente ruta almacenaremos nuestros archivos que estarán siendo manejados con git

```
C:\config-repo
```
Creamos el primer archivo para el servicio item

```
servicio-item.properties
```
Contenido del archivo

```
server.port=8005
```
**NOTA:** las configuraciones del **servidor de configuraciones** sobreescribirán
las configuraciones definidas en los microservicios. Por ejemplo, en el microservicio item
se definió el puerto=8002, pero ahora en el servidor de configuraciones se definirá
con el puerto=8005.

Si hay configuraciones que no están definidas en el servidor de configuraciones pero sí
en el microservicio, se fusionarán; del mismo modo, si hay configuraciones en el servidor
de configuraciones y no en el microservicios, también se fusionarán.