Diario

12/8/25
Git:
Hoy como es el primer día quería aprender a usar git y github
1. primeramente con el gitbash me dirigi al escritorio siguientdo esta ruta cd OneDrive/Escritorio
2. Luego cree la carpeta mkdir proyecto, cd proyecto, git init
4. Usando la interfaz de github cree mi repositorio y lo conecté a la carpeta desde gitbash con 
el enlace que había ahí, git add origin https://github.com/FabianFern4ndez/mi_primer_proyecto.git
4.1 resulta que se me equivoque al copiar el enlace y lo tuve que eliminar con el comando
git remote  remove origin, y luego volverlo a conectar
5. para subir cambios hay que hacer
git add .
git commit -m "descripcion"
git push origin rama

Quise hacer solo git commit sin el -m y me metio en vim, para salir es esc :wq enter

6. cree mi rama de desarrollo con git checkout -b dev
Bueno esto no lo he hecho pero segun deepseek, esto es lo que sigue
para cambiar de rama seria git checkout nombrerama

y para merge en main seria
git checkout main #cambiarte a la rama main
git merge dev
git push origin main

luego para eliminar la rama seria git checkout -d nombrerama

Bien, resulta que el .env no lo debo subir al repositorio ya que ahí hay informacion privada
cuando hago git add. y luego git status me sale que si hago commit se va a subir el .env
entonces hay que hacer git reset

Para que no se suban archivos que no se desean se debe hacer un archivo .gitignore
y adentro escribir el tipo de archivo que no quieres que se suba, por ejemplo yo puse .env

Python
Bien, lo primero es que voy a usar uv en vez de pip, el comando para verificar si uv esta 
instalado es uv -- version, lo que significa que lo tengo instalado, despues podria hacer 
uv install python pero ya lo tengo instalado
Use uv init . para inicializar mi proyecto en python
Para instalar todas las dependencias usamos el siguiente comando
uv add fastapi[all] langchain langchain-openai python-dotenv sqlalchemy uvicorn psycopg2-binary
Con esto se creo el .venv con las dependencias

Creamos en backend los archivos __init__.py y .env
Tambien creamos las siguientes carpetas
core: el controlador
db: para las operaciones de base de datos
models: para los modelos de las base de datos
routers: para las direcciones del router
schemas: para controlar las entradas y las salidas de la api
Ademas cree algunos archivos .py que me indico el video, y aprendi que el init es para que esa carpeta sea un modulo

