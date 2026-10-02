¿Qué ventaja tiene registrar las dependencias del proyecto en
requirements.txt en lugar de compartir la carpeta .venv? R= Registrar las dependencias en requirements.txt permite que otras personas puedan instalar fácilmente las mismas librerías que necesita el proyecto sin tener que compartir la carpeta .venv. Además, la carpeta .venv puede ser diferente dependiendo del equipo y ocupa más espacio. Con requirements.txt solo se guardan los nombres y versiones de las dependencias necesarias, por lo que cada integrante puede crear su propio entorno virtual y configurarlo correctamente.

## ¿Por qué el repositorio que tienes ahora en tu computadora no es el mismo concepto que el fork creado en GitHub?

El repositorio que tengo en mi computadora es una copia local con la que puedo trabajar y hacer cambios. En cambio, el fork es una copia del repositorio original que se encuentra en GitHub y pertenece a la cuenta de la persona colaboradora. El fork sirve para trabajar de manera independiente en GitHub y después poder enviar los cambios al repositorio original mediante un Pull Request.

------------------------------------------------------------------------------------------------------------------
79. ¿Cómo identificaste el comando necesario cuando la práctica no lo proporcionó?

R= Identifiqué el comando revisando el objetivo de la acción y el flujo habitual de Git. Cuando el comando no aparecía en la práctica, deduje la operación que debía hacerse (por ejemplo, preparar cambios, confirmar historial o cambiar de rama) y validé la sintaxis con la ayuda de Git o con la lógica del flujo estándar, en lugar de adivinarlo.

80. ¿Qué diferencia existe entre preparar un archivo para un commit y crear el commit?

R= Preparar un archivo consiste en usar git add para dejarlo listo en el área de preparación, es decir, seleccionar los cambios que se incluirán. Crear el commit es ejecutar git commit, que guarda esos cambios en la historia del repositorio con un mensaje descriptivo. En otras palabras, add elige qué se va a guardar y commit registra definitivamente ese estado.

81. ¿Cómo puedes comprobar en qué rama estás trabajando?

R= Puedes usar el comando git branch --show-current para ver la rama activa o bien git status, que también muestra la rama actual en la parte superior junto con el estado del repositorio. Esto permite saber en qué rama se está trabajando antes de hacer cambios o commits.

82. ¿Cómo puedes determinar qué archivos fueron modificados antes de registrarlos?

R= Puedes usar git status para ver los archivos que tienen cambios pendientes y su estado, o git diff --name-only para listar únicamente los nombres de los archivos modificados. Así puedes revisar qué archivos están afectados antes de preparar o confirmar los cambios.

83. ¿Cómo puedes observar exactamente qué cambió dentro de un archivo?

R= Puedes usar git diff, que muestra las líneas agregadas y eliminadas en un archivo en comparación con la última versión guardada. Si quieres ver el contenido exacto de los cambios en un archivo específico, puedes ejecutar git diff -- archivo o revisar también la diferencia de una línea a otra con la salida de Git.

84. ¿Por qué debe reconstruirse .venv después de obtener un repositorio?

R= Porque .venv es un entorno local y no se comparte ni se incluye en el repositorio. Al obtener un repositorio nuevo, el entorno virtual puede no existir o puede estar incompleto, y es necesario crearlo otra vez para instalar las dependencias registradas en requirements.txt. De esta forma, todos los paquetes del proyecto quedan disponibles en el mismo entorno del equipo o de la computadora.

85. ¿Qué relación existe entre requirements.txt y .gitignore?

R= La relación es complementaria: requirements.txt registra las dependencias del proyecto para que cualquiera pueda reproducir el entorno, mientras que .gitignore evita que archivos locales o temporales, como .venv, __pycache__ o archivos de configuración de cada máquina, se suban al repositorio. Por eso requirements.txt se versiona, pero .venv no se comparte entre equipos.

86. ¿Por qué la colaboración se realiza desde una rama y no directamente desde main?

R= Porque main debe mantenerse estable y representar una versión segura del proyecto. Al trabajar desde una rama, cada persona puede hacer cambios, probarlos y revisarlos sin afectar el código principal. Después, esos cambios se integran mediante merge o Pull Request, lo que facilita la colaboración y reduce el riesgo de romper el proyecto.

87. ¿Por qué una solicitud de cambios no requiere crear un Pull Request nuevo?

R= Porque la solicitud de cambios ya existe y su propósito es seguir el mismo conjunto de modificaciones. Si ya se abrió un Pull Request para la rama de trabajo, no hace falta crear otro; se continúa sobre esa misma discusión, revisión y aprobación. Crear uno nuevo duplicaría la misma tarea y complicaría el flujo de colaboración.

88. Después de realizar el merge en GitHub, ¿por qué todavía es necesario actualizar el repositorio local?

R= Porque GitHub y el repositorio local son dos copias distintas que pueden quedar desalineadas. Al hacer merge en GitHub, la rama remota cambia, pero la copia local no refleja ese cambio hasta que se sincroniza con git pull o git fetch y git merge. Actualizar el repositorio local garantiza que el entorno de trabajo esté al día con los últimos cambios del proyecto.