# Despliegue de Aplicaciones en Servidores de Aplicaciones y Servidores FTP

## Servidores de Aplicaciones

Los servidores de aplicaciones son servidores en red que ejecutan diversos servicios y gestionan la lógica de negocio y el acceso a los datos. Algunos de los servidores de aplicaciones más utilizados son:

- WildFly
- GlassFish
- JOnAs
- Apache Tomcat

### Arquitectura de Apache Tomcat

- **Server**: Representa el contenedor completo.
- **Service**: Intermediario que se comunica con el exterior a través de conectores.
- **Engine**: Permite procesar las peticiones.
- **Host**: Nombre de la conexión.
- **Connector**: Encargado de las comunicaciones hacia el exterior, incluyendo el importante HTTP Connector.
- **Context**: Representa una aplicación web.

### Servicios de Apache Tomcat

- Catalina
- Jasper
- Coyote
Catalina se encarga del contenedor de servlets y del ciclo de vida de los servlets, Jasper se encarga de compilar archivos JSP en servlets Java, y Coyote gestiona las conexiones HTTP entrantes y salientes.
### Estructura de Directorios y Ficheros de Apache Tomcat

- **/bin**: Contiene los scripts y archivos ejecutables para iniciar y detener el servidor Tomcat.
- **/conf**: Almacena los archivos de configuración de Tomcat, incluyendo el archivo **server.xml** que define la configuración del servidor y el archivo **web.xml** que contiene la configuración de despliegue de las aplicaciones web.
- **/lib**: Directorio donde se encuentran las bibliotecas (JARs) necesarias para el funcionamiento de Tomcat.
- **/logs**: Aquí se guardan los archivos de registro (logs) generados por Tomcat durante su funcionamiento.
- **/temp**: Directorio temporal utilizado por Tomcat para almacenar archivos temporales.
- **/webapps**: Es el directorio donde se despliegan las aplicaciones web.
- **/work**: Directorio donde Tomcat almacena archivos generados dinámicamente para las aplicaciones web desplegadas.
**Fichero server.xml**:

```
<Server>
    <Service>
        <Engine>
            <Host>
                <Connector/>
            </Host>
        </Engine>
    </Service>
</Server>
```

El servidor Tomcat por defecto arranca en: [http://localhost:8080/](http://localhost:8080/)

### Utilización de Apache Tomcat

- **Independiente**: Instalación en un servidor físico.
- **Integrado**: Instalación en IDE como Eclipse.

### Despliegue de Aplicaciones Web en Servidores

1. Exportar la aplicación web en formato WAR.
2. Colocar el archivo WAR en la carpeta `webapps` de Tomcat en el servidor físico.
3. Arrancar el servidor y probar la aplicación en el navegador.

## Optimización y Documentación

### Optimización

- Funcionalidad correcta con código reutilizable y buenas prácticas.
- Eliminación de código duplicado.
- Extracción de funcionalidades relacionadas en métodos.
- Uso de herencia, polimorfismo y encapsulamiento.
- Trabajo en capas de funcionalidad.
- Uso de nombres explicativos.
- Creación de métodos y clases reducidos.
- Eliminación de código no utilizado o innecesario, así como comentarios innecesarios.

### Documentación

- Documentación oficial de cada componente del código para facilitar la comprensión de la funcionalidad.

## Pruebas

- Realización de pruebas de todos los casos de fallo posibles.
- Realización de pruebas con casos correctos.
- Automatización de pruebas siempre que sea posible.

## Servidores de Transferencia de Archivos (FTP)

Los servidores de FTP facilitan la transferencia de archivos entre un cliente y un servidor. Los tipos de usuarios en FTP son:

- Usuarios anónimos.
- Usuarios autenticados.

### Modos de Conexión

- Modo activo: el servidor crea un canal para que el cliente envíe datos.
- Modo pasivo: el cliente inicia la conexión con el servidor.

### Uso de FTP

- Conexión por navegador web.
- Conexión por comandos.
- Conexión por herramienta gráfica.

