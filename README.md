# CBW - TASKS
Microservicio de gestión de tareas desarrollado como parte de una prueba técnica. Permite crear tareas, consultarlas, actualizarlas, eliminarlas, filtrarlas por estado y programar acciones asíncronas mediante una cola de trabajos.

Este Repositorio contiene autenticacion en las rutas , primero toca registrarse, loguarse y enviar el token por auth como un bearer token

Se dejan las colecciones de postman e insomnia para probar la api

  > Autor: **Luis Cortes**  
## 🚀 Tecnologías utilizadas 

  | Componente    | Descripción                      |
  |---------------|----------------------------------|
  | NestJS        | Framework backend (Node.js)      |
  | MongoDB       | Base de datos                    |
  | Redis         | Sistema de colas (Bull)          |
  | Bull          | Gestión de trabajos asíncronos   |
  | Docker        | Contenedores                     |
  | Docker Compose| Orquestación de servicios        |


La url de swagger : http://localhost:3000/api/docs -  http://localhost:PORT/api/docs
Nota: Por temas de tiempo solo esta en swagger documentado el auth , pero se envian las colecciones de postman e insomnia
## Dev

1. Clonar el repositorio
2. Crear un .env basado en el .env.template (Se puede copiar y utilizar el mismo)
3. Ejecutar el comando `git submodule update --init --recursive` para reconstruir los sub-módulos
4. Ejecutar el comando `docker compose up --build`


### Pasos para crear los Git Submodules

1. Crear un nuevo repositorio en GitHub
2. Clonar el repositorio en la máquina local
3. Añadir el submodule, donde `repository_url` es la url del repositorio y `directory_name` es el nombre de la carpeta donde quieres que se guarde el sub-módulo (no debe de existir en el proyecto)
```
git submodule add <repository_url> <directory_name>
```
4. Añadir los cambios al repositorio (git add, git commit, git push)
Ej:
```
git add .
git commit -m "Add submodule"
git push
```
5. Inicializar y actualizar Sub-módulos, cuando alguien clona el repositorio por primera vez, debe de ejecutar el siguiente comando para inicializar y actualizar los sub-módulos
```
git submodule update --init --recursive
```
6. Para actualizar las referencias de los sub-módulos
```
git submodule update --remote
```


## Importante
Si se trabaja en el repositorio que tiene los sub-módulos, **primero actualizar y hacer push** en el sub-módulo y **después** en el repositorio principal. 

Si se hace al revés, se perderán las referencias de los sub-módulos en el repositorio principal y tendremos que resolver conflictos.

