# Apuntes del Curso de Git

## Clase 1

### Instalación de Git
La instalación de Git es el primer paso para comenzar a trabajar con este sistema de control de versiones. Puedes descargar Git desde su página oficial de [Git](https://git-scm.com/) y seguir las instrucciones según tu sistema operativo. Una vez instalado, puedes verificar la versión con el comando `git --version`.

### ¿Qué es git?

### Antecedentes
A continuación un poco de historia sobre los sistemas de control de versiones.
* **1986**: CVS (Concurrent Versions System) es creado como uno de los primeros sistemas de control de versiones.
* **2000**: BitKeeper, un sistema de control de versiones distribuido, se convierte en una herramienta popular en el desarrollo de software.
* **2002**: Linus Torvalds y el equipo de desarrollo del kernel de Linux adoptan BitKeeper para gestionar el código del kernel.
* **2005**: Después de disputas sobre la licencia de BitKeeper, Torvalds desarrolla Git como un sistema de control de versiones distribuido para el kernel de Linux.
* **2007**: Git se vuelve ampliamente utilizado en la comunidad de desarrollo de software de código abierto, ofreciendo una alternativa descentralizada y eficiente a CVS y SVN.
* **2008**: GitHub, una plataforma de alojamiento de repositorios Git, se lanza al público, facilitando aún más la colaboración y el desarrollo de proyectos basados en Git.
* **2016**: Microsoft adquiere GitHub, fortaleciendo aún más la posición de Git como un estándar en el desarrollo de software.

### Iniciando un repositorio
Para iniciar un repositorio Git en un directorio existente, utilizamos el comando `git init`. Esto crea un repositorio local en ese directorio, que luego podemos utilizar para realizar seguimiento de cambios.

### Áreas de un repositorio
Git tiene tres áreas principales en las que se manejan los archivos:

1. **Directorio de trabajo (Working Directory)**: Es donde trabajamos con nuestros archivos de manera activa.
2. **Área de preparación (Staging Area)**: Aquí colocamos los archivos que queremos incluir en el próximo commit utilizando el comando `git add`.
3. **Repositorio local (Local Repository)**: Una vez que hacemos commit de los cambios en el área de preparación, se guardan de manera permanente en el repositorio local con el comando `git commit`.

### Comandos Git
* **git add**: Este comando se utiliza para agregar cambios al área de preparación. Puedes agregar archivos específicos con `git add nombre_archivo` o agregar todos los cambios con `git add .`.
* **git commit**: Después de agregar cambios al área de preparación, utilizamos `git commit -m "mensaje"` para confirmar esos cambios en el repositorio local con un mensaje descriptivo.
* **git log**: Con este comando podemos ver el historial de commits realizados en el repositorio, incluyendo información como el autor, la fecha y el mensaje del commit.
  * `git log --oneline`
  * `git log --graph`
* **git checkout**: Permite cambiar entre ramas o versiones de archivos. Por ejemplo, `git checkout nombre_rama` cambia a una rama específica, mientras que `git checkout -- nombre_archivo` descarta cambios locales en un archivo.
* **git --amend**: Este comando se utiliza para modificar el commit más reciente. Puedes cambiar el mensaje del commit o incluso agregar archivos que olvidaste incluir en el commit anterior utilizando `git add` y luego `git commit --amend`.