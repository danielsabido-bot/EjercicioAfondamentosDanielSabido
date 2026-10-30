# Documentación del Ejercicio Práctico de Git y GitHub 
## Crear la identidad, la carpeta y acceder a ella:
```bash
git config --global user.name "Daniel"
git config --global user.email "danielsabidop12@gmail.com"
mkdir ejercicio\git 
cd ejercicio\git
```
## Crear el archivo .txt y el script.sh:
```bash
nano texto.txt
nano script.sh
```

## Inicializar el repositorio Git, ver el estado y cambiar el nombre a la rama (y luego restaurarlo):
```bash
git init
git status
git branch -m main
git branch -m master
```

# Añadir archivos y confirmamos
```bash
git add texto.txt
git add script.sh
git add README.md

git commit -m "Confirmación inicial"
```
# Modificar texto.txt

```bash
nano texto.txt #Y agregar nueva línea "cuatro" y "cinco"
git add texto.txt
git commit -m "Ampliada la explicación del texto"
```

# Ver el último cambio y los cambios históricos:
```bash
git show
git log
```

# Modificar texto.txt y ver diferencias de archivos:

```bash
nano texto.txt #Borrar linea "tres" y agregar linea "seis"
get diff
git commit -a -m "Probando diff"
nano texto.txt #Agregar linea "siete"
git diff
```

# Ignorar archivos:

```bash
nano .gitignore #Crear archivo para gestionar archivos a ignorar
```
Dentro del archivo agregar:
```text
# ignora los archivos terminados en .class
*.class 
# ignora los archivos terminados en ~
*~ 
# pero no importante~, aun cuando habia ignorado los archivos terminados en ~ en la linea anterior 
!importante~
```
Crear otros 2 archivos, uno llamado Hola.java con el siguiente contenido:
```java
class Hola {
 public static void main(String[] args){
 System.out.println("Welcome to the Java World");
 }
}
```
Y otro llamado temporal~ y importante~

Guardar en el repositorio:
```bash
git add .
git commit -m "Añadidos fuentes en java y archivos importantes"
```