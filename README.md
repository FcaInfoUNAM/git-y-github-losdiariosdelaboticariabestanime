# Laboratorio Básico de Git y GitHub

Este entrenamiento está diseñado para enseñar los comandos básicos de Git y cómo colaborar en un repositorio en GitHub. Trabajarán en equipos de 3 personas para crear un repositorio desde cero y subirlo a GitHub.

## Requisitos Previos

1. Tener instalado Git en tu computadora. Puedes descargarlo desde [aquí](https://git-scm.com/).
2. Crear una cuenta en [GitHub](https://github.com/).
3. Tener un editor de texto o IDE instalado (por ejemplo, Visual Studio Code).

---

## Instrucciones Paso a Paso

### 1. Configuración Inicial de Git

Antes de empezar, configura tu nombre y correo electrónico en Git. Abre una terminal y ejecuta los siguientes comandos:

```bash
git config --global user.name "Tu Nombre"
git config --global user.email "tuemail@example.com"
```

### 2. Crear un Repositorio Local

Crea una carpeta en tu computadora para el proyecto. Por ejemplo:
```bash
mkdir mi-proyecto
cd mi-proyecto
```
Inicializa un repositorio de Git en la carpeta:
```bash
git init
```
Esto creará una carpeta oculta llamada .git que almacenará toda la información del repositorio.
### 3. Agregar Archivos al Repositorio
> [!WARNING]
> Si estas utilizando github classroom
> * Omite los pasos #3,#4 y #5

Crea un archivo en la carpeta del proyecto. Por ejemplo, index.html:
```bash
touch index.html
```
Abre el archivo en tu editor de texto y añade algún contenido.
Agrega el archivo al área de preparación (staging area) de Git:
```bash
git add index.html
```
Si quieres agregar todos los archivos de la carpeta, puedes usar:
```bash
git add .
````

### 4. Hacer un Commit

Guarda los cambios en el historial del repositorio con un commit:

```bash
git commit -m "Mi primer commit: agregué el archivo index.html"
```
El mensaje del commit debe ser descriptivo para que los demás miembros del equipo entiendan qué cambios se hicieron.

### 5. Crear un Repositorio en GitHub
Ve a GitHub y crea un nuevo repositorio. Dale un nombre, por ejemplo, mi-proyecto.
No inicialices el repositorio con un README.md, ya que ya tienes un repositorio local.

### 6. Conectar el Repositorio Local con GitHub

Copia la URL del repositorio de GitHub (debe ser algo como https://github.com/tuusuario/mi-proyecto.git).
En tu terminal, conecta tu repositorio local con GitHub:
```bash
git remote add origin https://github.com/tuusuario/mi-proyecto.git
```
> [!IMPORTANT]
> Si estas utilizando github classroom
> * Debes jalar los cambios del repositorio haciendo ```git pull```
> * Ahora deberás relizar los pasos #3 y #4 

Sube los cambios a GitHub:
```bash
git push -u origin main
```


Esto subirá tu código a la rama main (o master en algunos casos) del repositorio remoto.
### 7. Trabajar en Equipo

Invita a tus compañeros de equipo como colaboradores en GitHub (desde la configuración del repositorio).
Cada miembro del equipo debe clonar el repositorio:
```bash
git clone https://github.com/tuusuario/mi-proyecto.git
```
Para trabajar en una nueva funcionalidad, cada miembro debecrea una rama:
```bash
git branch nombre-de-la-rama
```
Cambia a la nueva rama:
```bash
git checkout nombre-de-la-rama
```
Cada miembro debe crear un archivo con su nombre, ejemplo: Juan.txt
Editenlo agregando su número de cuenta
```bash
touch tuNombre.txt
git add tuNombre.txt
nano tuNombre.txt
git commit -m "Agregué nueva funcionalidad"
git push origin nombre-de-la-rama
```
En GitHub, crea un Pull Request para fusionar los cambios con la rama main.


> [!NOTE]
> Resumen de Comandos
> * ```git init```: Inicializa un repositorio local.
> * ```git add```: Agrega archivos al área de preparación.
> * ```git commit```: Guarda los cambios en el historial del repositorio.
> * ```git push```: Sube los cambios al repositorio remoto.
> * ```git branch```: Crea una nueva rama.
> * ```git checkout```: Cambia a una rama existente.
> * ```git clone```: Clona un repositorio remoto en tu computadora.

