# Práctica con git y GitHub

Este es un repositorio muy simple para practicar GitHub, el cual es un servicio gratuito* de alojamiento de código en línea que funciona con git.
Git es una herramienta para el *control de versiones*. Cuando un conjunto de código es rastreado con git, es fácil ver cómo ha evolucionado el software con el tiempo, revertir cambios cuando sea necesario e incorporar modificaciones de múltiples colaboradores.
En esta actividad, nos enfocaremos en los principales flujos de trabajo de git.

***Nota***: si ya te sientes cómodo usando git desde la línea de comandos, puedes seguir estas instrucciones reemplazando las operaciones de GitHub Desktop con los comandos correspondientes en la terminal. ¡Ambos enfoques son válidos! Por el momento usaremos GitHub Desktop, pero muchos prefieren la línea de comandos.

## 1. Crear una cuenta y descargar Github

Ya deberías haber creado una cuenta en [GitHub](https://github.com/) y descargado [GitHub Desktop](https://desktop.github.com/).

## 2. Hacer un Fork o clonar

*Hacer un fork o bifurcar* se refiere al acto de crear una copia personal de un repositorio existente. Luego puedes modificar tu *fork* como desees. Hacer un fork es una excelente manera de aprovechar plantillas y otros recursos sobre los cuales puedes construir y contribuir, clonar es parecido pero no se conecta directamente a la cuenta y no está directo para contribuir (el dueño original acepta o rechaza dichas contribuciones).

Clona o haz un fork de este repositorio usando el botón "Fork" en la esquina superior derecha en la página o el botón de código para clonar.

Normalmente se hace un fork
Se crea una branch con un nombre descriptivo
Se hacen los cambios mediante commits
Se hace push a la branch
Se hace un pull request al dueño original

Pero si quieres hacer cambios directamente al repositorio es mejor crear un *clon local* de este.
Para hacerlo, presiona el botón verde grande y elige "Abrir en GitHub Desktop". Selecciona una ubicación donde puedas recordar fácilmente dónde está el repositorio.

En este momento, es solo una copia del [repositorio original](https://github.com/OscarMacielC/GithubPractice).

## 3. Editar un Archivo

En tu clon local del repositorio, abre (`README.md`) y modifica la siguiente línea cambiando "tu nombre completo"

> Soy \[Carlos Alejandro Rodriguez Quintero\] y edité este archivo.

## 4. Agregar y Confirmar Cambios (Commit)

Ahora en GitHub Desktop podemos observar que el archivo `README.md` ahora aparece como modificado. Si aún no hay una marca azul de verificación junto al archivo, haz clic en la casilla para marcarlo si no lo está.

Luego, agrega un *mensaje de commit* en el cuadro de abajo. El mensaje de commit debe ser una breve descripción de lo que lograste con tu modificación. Por ejemplo, un buen mensaje aquí podría ser "Agregar nombre a README.md". Una vez que hayas ingresado el mensaje de commit, haz clic en el gran botón azul "Commit".

## 5. Crear una Carpeta y un Archivo

Pero espera, hagamos más. Crea una nueva carpeta llamada `practica_git` dentro del repositorio clonado. Luego, crea un archivo index.html en esta carpeta y un archivo app.js vacío.

```HTML
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Github</title>

    <script src="app.js" defer></script>
  </head>

  <body>
    <h1>Nombre completo</h1>
    <h2>Click to get new jokes!</h2>
    <button>Click me!</button>
    <ul id="jokes"></ul>
  </body>
</html>
``` 

## 6. Agregar y Confirmar Cambios (Commit)

Ahora, agrega tu código html con un mensaje de commit informativo y confirma el archivo.

## 7. Subir (Push)

Ya tenemos hechos algunos cambios locales, lo siguiente es *subir* nuestro código de nuevo a GitHub. Esto nos permitirá compartir nuestro código con otros.

Para subir tu código, simplemente haz clic en el botón "Push" en la parte superior derecha de GitHub Desktop. Antes de hacer clic, puedes notar que el botón indica la cantidad de commits que has hecho desde tu último push. Después de hacer clic en el botón, ya no tendrás más commits pendientes de subir.

## 8. Inspeccionar en GitHub

Ahora ve a la URL de tu proyecto en GitHub e inspecciona el nuevo archivo `README.md`. También puedes echar un vistazo al html que subimos.

## 9. Obtener Cambios (Pull)

¿Qué sucede si hay un cambio hecho en GitHub que no está presente en tu repositorio local? Esta es una situación común cuando se colabora o si trabajas en distintas máquinas. Tu compañero hizo una cambio en el código que te gustaría tener. Para hacerlo, necesitas *obtener (pull)* los cambios.

Para practicar el proceso de "pull", primero necesitamos hacer un cambio en GitHub web. Edita el archivo `README.md` de nuevo, lo cual puedes hacer navegando hasta el archivo y haciendo clic en el ícono del lápiz.

> Soy \[tu nombre\] y edité este archivo desde GitHub web.

Al final de la pantalla de edición, se te pedirá que confirmes el cambio con un mensaje de commit.

Ahora vamos a obtener este cambio en nuestro repositorio local. En GitHub Desktop, el botón que antes decía "Push" ahora debería decir "Fetch" o "Pull" con un indicador del número de commits disponibles para obtener. Si dice "Fetch", haz clic una vez y espera a que diga "Pull". Una vez que diga "Pull", haz clic nuevamente y espera unos momentos para completar la actualización.

Finalmente, revisa el archivo `README.md` en tu máquina local. El cambio que hiciste en línea ahora debería estar reflejado en tu archivo local también.

## 10. Descartar y Revertir Cambios

Una gran ventaja de trabajar con un sistema de control de versiones como git es que puedes deshacer errores fácilmente volviendo a la última versión "buena" de tu proyecto. Hay múltiples maneras de hacerlo. Nos enfocaremos en dos.

### Descartar

Si por algo ya escribiste algo en app.js podemos descartar estos cambios simplemente dando clic derecho sobre el cambio y seleccionando "Discard Changes". Revisa tu archivo nuevamente. Deberías notar que el archivo queda nuevamente vacío.

### Revertir

A veces, no detectamos un error hasta después de haberlo confirmado con un commit, vamos a poner algo en app.js y darle commit, quizá incluso podemos agregar un código inservible.

Para *revertir* el commit, ve a la pestaña "Historial" en GitHub Desktop. Haz clic derecho en el commit con el mensaje que tiene el error y selecciona "Revert Changes in Commit". Esto tendrá el efecto de crear un *nuevo* commit que deshace los cambios en tu commit erróneo. Esto funcionará incluso si has hecho otros commits desde el commit incorrecto; solo los cambios de ese commit serán revertidos.

***Nota***: GitHub Desktop no tiene una opción correspondiente a `git reset`, pero si te sientes cómodo en la terminal y estás familiarizado con este comando, también puedes usar `git reset` para lograr una tarea similar, aunque con diferentes efectos en el historial de commits.

### 11. Crear una branch o rama

Cuando se quieren hacer distintas modificaciones pero no quieren arriesgar modificar su archivo general se puede hacer una branch, que solo es un commit aparte que puede ser ignorado o puede juntarse a nuestra branch principal en un futuro

Vamos a crear una branch llamada funcionalidad-api, una vez creada nos aseguramos de estar en la branch nueva, si por algo no lo estamos la seleccionamos donde dice "current branch"

Una vez en ella vamos al archivo app.js y agregamos el siguiente código.

```JS
const jokes = document.querySelector("#jokes");
const button = document.querySelector("button");

const addNewJoke = async () => {
  const jokeText = await getDadJoke();
  const newLI = document.createElement("LI");
  newLI.append(jokeText);
  jokes.append(newLI);
};

const getDadJoke = async () => {
  try {
    const res = await fetch("https://icanhazdadjoke.com/", {
      headers: { Accept: "application/json" }
    });
    const data = await res.json();
    return data.joke;
  } catch (e) {
    return "NO JOKES AVAILABLE! SORRY :(";
  }
};

button.addEventListener("click", addNewJoke);
``` 
También cambia está línea

> Soy \[tu nombre\] y cambié esto en una branch.

Hacemos commit y push a los cambios

### 12. Revisando la rama

Podrán observar que si cambiamos a nuestra rama principal el cambio hecho no existe, pero en la nueva si se encuentra.

### 13. Merge o unión de ramas

Para traer nuestros cambios hechos en la branch a nuestro código principal vamos a cambiar a la branch main y presionar el botón "choose a branch to merge into main", seleccionamos nuestra nueva branch y le presionamos en "create a merge commit"

Con eso los cambios ya se encontrarán en nuestra branch principal, revisen los cambios para asegurarse de que se realizó correctamente.

Si la branch ya no se va a utilizar se puede eliminar, hay distintos flujos de trabajo en los que se hace una branch por cada arreglo o en ocasiones hacen branches por usuario o por versiones o por tipos de trabajo como dev, fixes, qa, todo depende de la forma de trabajar del equipo.

### 14. Practicando un poco

Agrega en main en el head de su archivo html y crea un commit
``` html
<link rel="stylesheet" href="style.css" />
``` 
Haz una dos branch distintas llamada color-1 y color-2 con un archivo style.css y cambia el título de color, abre tu página web y cambia entre una branch y otra, revisando cómo cambia automáticamente la página (usando live server).
```CSS
h1{
    color: rgb(20, 255, 243);
}
```
Hacer merge del color que más les guste

Poner su nombre completo en el HTML (en el título H1)

### 15. Subir a vercel

[Ir a la página de vercel](https://vercel.com/)
Import Git Repository
Seleccionar deployment
Pasar el link de *****************.vercel.app en la tarea

### A. Resolución de conflictos

La mayoría de conflictos son generados por cambios de líneas cuando dos usuarios modifican el mismo archivo sin pasarse los cambios, y estos pueden ser resueltos en github, pero para conflictos más complicados se necesita usar la línea de comando de git, por lo que es bastante útil también entender el uso de git.

Cuando hay un conflicto se puede seleccionar si tomar los datos que se tienen, los datos nuevos o resolver el conflicto manualmente, si se selecciona la solución manual pueden entrar al documento y verán los siguientes símbolos, se usan como etiquetas de quien hizo los cambios y los igual son simples separadores.

<<<<<<<, ======= y >>>>>>>

Pueden eliminar dichos símbolos y quedarse con las líneas que quieran, pueden decidir usar solo uno de los cambios o quizá juntar ambos eliminando ciertas líneas.

### B. No dupliquen archivos

Un principio importante del control de versiones es que **nunca** dupliquemos archivos. En lugar de tener `proyecto_V1.html`, `version_final.html`, `version_final_REAL.html`, `version_final_REAL_funciona_3.html`, deberías confirmar tu código en cada etapa (o incluso con mayor frecuencia). Siempre podrás volver atrás y encontrar las versiones anteriores en el historial de commits.

### C. Temas extras explicados en clase
¿gitignore?
¿PRs?
¿git y github?
¿Cherry picking?

### D. Links de utilidad
https://git-scm.com/book/en/v2
https://training.github.com/downloads/github-git-cheat-sheet.pdf
https://docs.github.com/en/get-started/git-basics/set-up-git
https://rogerdudler.github.io/git-guide/
