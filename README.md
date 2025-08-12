Diario

12/8/25
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
