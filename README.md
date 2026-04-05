# Git ignore

_Es un archivo de texto que le indica a git que archivos o carpetas debe ignorar y no incluirse en el control de versiones_

### a) ¿Por qué es conveniente incluir un archivo .gitignore?

_Acostumbrarnos a incluirlo nos sirve de buena practica para mantener el repositorio limpio eficiente y profesional_

1.Evita subir archivos innecesarios: Impide que archivos temporales, cachés, logs o dependencias (node_modules/) se suban al repositorio, lo que lo mantiene ligero.

2.Protege información sensible: Ayuda a prevenir que archivos con contraseñas, claves API o configuraciones locales (como .env) sean expuestos públicamente.

3.Previene conflictos: Excluye archivos de configuración específicos de tu máquina o de tu IDE (como .idea/ o .vscode/), evitando conflictos con la configuración de otros miembros del equipo.

4.Claridad en los cambios: Al ignorar archivos que no son parte del código fuente, los resultados de git status muestran únicamente los archivos relevantes del proyecto, lo que facilita ver qué ha cambiado realmente. 

### b) ¿Cuándo se debe hacer?

_ Se recomienda configurar el .gitignore al inicio del proyecto, antes de realizar el primer commit. Hacerlo al principio evita tener que "limpiar" el repositorio después. _


### c) ¿Cómo configurar el archivo .gitignore?

_ Sepuede crear el archivo .gitignore desde la terminal o con cualquier editor de texto._

_ Desde la terminal (Linux/macOS/Git Bash): _

```
# Te ubicas en la raíz de tu proyecto
cd mi-proyecto

# Creas el archivo .gitignore
touch .gitignore```


```
_Estructura y sintaxis básica: _
_El archivo es un simple texto donde escribes un patrón por línea._

- # : Para añadir comentarios.

- * : Comodín que coincide con cualquier carácter (ej. *.log ignora todos los archivos con extensión .log).

- nombre/ : La barra al final ignora todo el directorio (ej. node_modules/).

- ! : El signo de exclamación al inicio niega un patrón (ej. !info.log dentro de un patrón *.log hará que Git sí rastree info.log)._
- 
 _ejemplo practico de un archivo git ignore_
```
# Dependencias (ignorar la carpeta completa)
node_modules/

# Archivos del sistema operativo
.DS_Store
Thumbs.db

# Archivos de entorno con claves secretas
.env
.env.local

# Archivos de log
*.log

# Directorios de salida de compilación
dist/
build/

# Configuraciones de IDE (ej. Visual Studio Code)
.vscode/
.idea/

plo
```

_Otra formas de hacer git ignore mas facil: _

_GitHub: Mantiene una colección oficial de plantillas para casi cualquier lenguaje y entorno en github/gitignore._

_gitignore.io: Un sitio web donde seleccionas tu sistema operativo, IDE y lenguaje, y te genera el archivo .gitignore personalizado al instante. También puedes usarlo desde la terminal con curl: curl -sL https://www.toptal.com/developers/gitignore/api/node,macos > .gitignore._
