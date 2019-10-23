# Getting Started

### Documentación
Antes de comenzar, revisar que existan las siguientes variables de entorno:

* `CONFIG_REPO_URL` : Url del repositorio donde se encuentren los ficheros .properties o .yml.
* `REPO_USER`         : Usuario del repositorio
* `REPO_PASS`         : Contraseña del repositorio

Para comprobar el correcto funcionamiento del servidor puede ejecutar las siguientes peticiones desde un navegador:

* Health check:	`http://localhost:8888/actuator/health`
* Properties:	`http://localhost:8888/{application}/{profile|default}`

El servidor está protegido con usuario/contraseña [root / s3cr3t]

Para obtener una nueva contraseña encriptada se puede ejecutar la siguiente petición desde el navegador:

```
POST http://localhost:8888 -d {password}
```

Si hay alguna duda, en el directorio `postmanTest` se puede encontrar esta petición.
