# 1 Crear cuenta en GitHub 

Para crear una cuenta de GitHub hay que acceder a la web github.com y seguir los pasos para registrase rellenando los campos solicitados.
 
A continuación, en el apartado de especificación de alumno o profesor, se pulsa en la opción que aparece en la parte inferior de la pantalla “skip personalization”. Con estos sencillos pasos estará concluido el proceso de registro.

# 1.1 Crear tu primer repositorio

Tras concluir el proceso de registro, se procede a crear el primer repositorio, incluyendo un archivo README en el que, con lenguaje de marcación, se mostrara una breve explicación de la tarea, y un archivo sencillo "Hola Mundo" en el lenguaje de programación Python. 
Para crear dicho repositorio desde la página principal existe un acceso directo, donde escribiremos el nombre del nuevo repositorio y se podrá elegir la opción de ser público o privado, en mi caso seleccionare la opción de público, una vez rellenado los campos presiono el botón “Crear un nuevo repositorio”.

# 1.2 Configurar claves SSH

Necesitamos dar permisos de escritura y lectura para poder realizar cambios en nuestro repositorio para ello abrimos un terminal y desde el directorio c:/users/” nombre de usuario”/.shh, se van a generar las claves tanto publica como privada con el siguiente comando: 

```bash
	ssh-keygen -t rsa -b 4096 -C tu_correo@ejemplo.com
```

Una vez generada las claves abrimos el archivo .pub y copiamos todo su contenido (esta será la clave publica)
A continuación, desde nuestra cuenta de GitHub en el menú del icono pinchamos en SSH and GPG keys

Una vez seleccionado aparecerá un botón de NEW SSH key, se debe pinchar sobre él y es aquí donde pegaremos la clave publica copiada con anterioridad.


# 1.3 Iniciar repositorio local, preparar cambios, guardar cambios y subir cambios.

Una vez creado el repositorio en GitHub y configurado las claves SSH elegimos en nuestra maquina un directorio o creamos uno nuevo, en él se procede a crear un archivo README.md y otro holaMundo.py, desde el terminal y situado en el directorio donde se encuentran los archivos, se procede a iniciar el repositorio con los siguientes comandos: 
-	git init -> Crea una nueva carpeta oculta llamada ".git" en el directorio actual. Esta carpeta contiene todos los archivos necesarios para que Git funcione y gestione el control de versiones.

```bash

    -	git add . -> Preparara los cambios para ser incluidos en el próximo commit.

    -	git branch -M main -> Cambia el nombre de la rama actual

    -	git commit -m "primer commit" -> Guardar los cambios preparados en el área de preparación en el historial de versiones.

    -	git remote add origin https://github.com/fdlang-IA/programacion-IA-IA-BigData.git  ->  Establece una conexión entre el repositorio local y un repositorio remoto.

    -	git push -u origen main -> Envía los commits locales al repositorio remoto.

```
