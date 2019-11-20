# Getting Started

### Documentación
Antes de comenzar, comprobar las siguientes dependencias:

* `CONFIG_REPO_URL` : Variable de entorno con la Url del repositorio donde se encuentren los ficheros .properties o .yml.
* `REPO_USER`         : Variable de entorno con el Usuario del repositorio
* `REPO_PASS`         : Variable de entorno con la Contraseña del repositorio
* La estructura del repositorio deberá estar formada por:

```
    .
    ├── {label}
        ├── {application}.properties
        	ó
        ├── {application}-{profile}.properties
        	ó
        ├── {application}-{profile}.yml
    ├── {label}
        ├── ...

```



Para comprobar el correcto funcionamiento del servidor puede ejecutar las siguientes peticiones desde un navegador:

* Health check:	`http://localhost:8888/actuator/health`
* Properties:	`http://localhost:8888/{application}/{profile|default}`

El servidor está protegido con usuario/contraseña [root / s3cr3t]

Para obtener una nueva contraseña encriptada se puede ejecutar la siguiente petición desde el navegador:

```
POST http://localhost:8888/encrypt -d {password}
```

Si hay alguna duda, en el directorio `postmanTest` se puede encontrar esta petición.
