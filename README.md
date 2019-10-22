# Getting Started

### Documentación
Antes de comenzar, revisar que existan las siguientes variables de entorno:

* `CONFIG_REPO_URL` : Url del repositorio donde se encuentren los ficheros .properties o .yml.
* `REPO_KEY` : Certificado digital de conexión al repositorio.

Para generar la llave SSH será necesario seguir estos pasos:

1. Acceder a Git bash.
2. Generar la nueva clave: `$ ssh-keygen -t rsa -b 4096 -C "mail@dominio.com"`.
3. Visualizar la clave pública: `$ cat ~/.ssh/config_repo_rsa.pub`.
4. Acceder a la cuenta de GitHub `/settings/SSH and GPG keys/New SSH Key` y pegar la clave pública junto a un título.
5. Visualizar la clave privada: `$ cat ~/.ssh/config_repo_rsa`.
6. Crear la variable de entorno `REPO_KEY` y pegar la clave privada. /settings/SSH and GPG keys/New SSH Key`.
	

Para comprobar el correcto funcionamiento del servidor puede ejecutar las siguientes peticiones desde un navegador:

* Health check:	`http://localhost:{port}/actuator/health`
* Properties:	`http://localhost:{port}/application/default`

