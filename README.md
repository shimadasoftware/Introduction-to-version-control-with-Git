# <img src="https://github.com/shimadasoftware/Introduction-to-version-control-with-Git/assets/73977456/801ea14c-dd83-46bb-ab5b-d229a151bc5c" alt="Italian Trulli" style="width:25px;height:25px;"> Introducción al control de versiones con Git 

**©** Copyright es reservado para el curso Introducción al control de versiones con Git de la plataforma Microsoft Learn.

## Introdución

### ¿Qué es el control de versiones?

Un **sistema de control de versiones (VCS)** es un programa o conjunto de programas que realiza un **seguimiento de los cambios en una colección de archivos**. Uno de los objetivos de un VCS es recuperar fácilmente versiones anteriores de archivos individuales o de todo el proyecto. Otro objetivo es permitir que varios miembros de un equipo trabajen en un proyecto, incluso en los mismos archivos, al mismo tiempo sin que eso afecte al trabajo de los demás.

Otro nombre para un VCS es un **sistema de administración de configuración de software (SCM)**. Los dos términos suelen usarse indistintamente; de hecho, la documentación oficial de Git se encuentra en git-scm.com. Técnicamente, el control de versiones es solo uno de los procedimientos que implica el SCM. Un VCS se puede usar para otros proyectos además de los de software, incluidos libros y tutoriales en línea.

Con un VCS, puede:

- Ver todos los cambios realizados en el proyecto, cuándo se hicieron los cambios y quién los efectuó.

- Incluir un mensaje con cada cambio para explicar los motivos.

- Recuperar versiones anteriores del proyecto completo o de archivos individuales.

- Crear ramas, donde los cambios se pueden hacer experimentalmente. Esta característica permite que se trabaje en varios conjuntos de cambios diferentes (por ejemplo, características o correcciones de errores) al mismo tiempo, posiblemente personas distintas, sin que ello afecte a la rama principal. Más adelante se pueden combinar los cambios que se quieren mantener en la rama principal.

- Adjuntar una etiqueta a una versión, por ejemplo, para marcar una nueva versión.

Git es un VCS de código abierto rápido, versátil, muy escalable y gratuito. 
**Su autor principal es Linux Torvalds**, creador de Linux.

### Control de versiones distribuido

Las instancias anteriores de los VCS, como CVS, Subversion (SVN) y Perforce, usaban un servidor centralizado para almacenar el historial de un proyecto. Esta centralización significaba que un solo servidor también era un único punto de error en potencia.

**Git es un sistema distribuido**, lo que significa que el historial completo de un proyecto se almacena en el cliente y en el servidor. Se pueden editar archivos sin conexión de red, protegerlos localmente y sincronizarlos con el servidor cuando una conexión esté disponible. Si un servidor deja de funcionar, todavía tendrá una copia local del proyecto. Técnicamente, ni siquiera es necesario tener un servidor. Los cambios pueden pasarse por correo electrónico o compartirse mediante medios extraíbles, pero, en la práctica, nadie usa Git así.

### Terminología de Git
  - **Árbol de trabajo:** conjunto de directorios y archivos anidados que contienen el proyecto en el que se trabaja.
    
  - **Repositorio (repo):** directorio, situado en el nivel superior de un árbol de trabajo, donde Git mantiene todo el historial y los metadatos de un proyecto. A veces se hace referencia a los repositorios como repos. Un repositorio vacío es aquel que no forma parte de un árbol de trabajo; se usa para compartir o realizar copias de seguridad. Un repositorio vacío suele ser un directorio con un nombre que acaba en .git, por ejemplo, project.git.
    
  - **Hash:** número generado por una función hash que representa el contenido de un archivo u otro objeto como un número de dígitos fijo. Git usa hashes de 160 bits de longitud. Una ventaja de usar códigos hash es que Git puede indicar si un archivo ha cambiado aplicando un algoritmo hash a su contenido y comparando el resultado con el hash anterior. Si se cambia la marca de fecha y hora del archivo, pero el hash del archivo no, Git sabe que el contenido del archivo no se ha modificado.
    
  - **Objeto:** un repositorio de Git contiene cuatro tipos de objetos, cada uno identificado de forma única por un hash SHA-1. Un *objeto blob* contiene un archivo normal. Un *objeto árbol* representa un directorio, y contiene nombres, valores hash y permisos. Un *objeto de confirmación* representa una versión específica del árbol de trabajo. Una *etiqueta* es un nombre asociado a una confirmación.
    
  - **Confirmación:** cuando se usa como verbo, confirmar significa crear un objeto de confirmación. Esta acción toma su nombre de las confirmaciones en una base de datos. Significa que se confirman los cambios realizados para que otros usuarios también puedan verlos.

  - **Rama:** serie con nombre de confirmaciones vinculadas. La *confirmación más reciente en una rama se denomina nivel superior*. La rama predeterminada, que se crea al *inicializar un repositorio, se denomina *main*, y suele tener el nombre master en Git. El *nivel superior de la rama actual se denomina HEAD*. Las ramas son una característica increíblemente útil de Git porque permiten a los desarrolladores trabajar de forma independiente (o conjunta) en ramas y luego combinar los cambios en la rama predeterminada.

  - **Remoto:** referencia con nombre a otro repositorio de Git. *Cuando se crea un repositorio, Git crea un remoto denominado origin*, que es el remoto predeterminado para las operaciones de envío e incorporación de cambios.

  - **Comandos, subcomandos y opciones:** las *operaciones de Git se realizan mediante comandos* como git push y git pull. git es el comando, mientras que push o pull es el subcomando. El subcomando especifica la operación que quiere que Git realice. Los comandos suelen ir acompañados de opciones, que usan guiones (-) o guiones dobles (--). Por ejemplo, git reset --hard.

### Git y GitHub

Como se ha mencionado anteriormente, *Git es un sistema de control de versiones distribuido (DVCS)* que varios desarrolladores y otros colaboradores pueden usar para trabajar en un proyecto. Proporciona una manera de trabajar con una o varias ramas locales y luego insertarlas en un repositorio remoto.

*GitHub es una plataforma en la nube que usa Git como tecnología principal*. Simplifica el proceso de colaboración en proyectos y proporciona un sitio web, más herramientas de línea de comandos y un flujo integral que los desarrolladores y usuarios pueden usar para trabajar juntos. GitHub actúa como el repositorio remoto mencionado anteriormente.

Entre las características clave que ofrece GitHub se incluyen las siguientes:
- Incidencias
- Debates
- Solicitudes de incorporación de cambios
- Notificaciones
- Etiquetas
- Acciones
- Bifurcaciones
- Proyectos

## Instalación en Linux distribución Fedora
