 ***Alumno:** Ismael Mulas Salinas

- **Bloque:** BLOQUE 0 · PRERREQUISITOS
    
- **Fase / ejercicio:** Fase 0.8
    
- **Fecha de inicio:** 02/11/2026
    
- **Fecha de entrega:** 02/11/2026
    

---

## 🎯 Qué se pedía

Crear desde cero una página web para gestionar el préstamo de portátiles, utilizando Git y GitHub para guardar las distintas versiones del proyecto. También había que crear varias páginas, añadir una imagen, excluir los vídeos del repositorio y comprobar que se podía recuperar la primera versión.

## ⌨️ Comandos y pasos importantes

- `git init` — crea un repositorio Git en la carpeta del proyecto.
    
- `git branch -M main` — establece el nombre de la rama principal como `main`.
    
- `git status` — muestra el estado de los archivos.
    
- `git add .` — prepara todos los archivos que no estén ignorados.
    
- `git add archivo` — prepara un archivo concreto para guardarlo.
    
- `git diff` — muestra los cambios que todavía no se han preparado.
    
- `git diff --cached` — muestra los cambios que ya están preparados.
    
- `git diff --cached --stat` — muestra un resumen de los archivos preparados y sus modificaciones.
    
- `git commit -m "mensaje"` — guarda una versión del proyecto.
    
- `git remote add origin URL` — conecta el repositorio local con GitHub.
    
- `git push` — sube los cambios a GitHub.
    
- `git log --oneline` — muestra el historial de versiones.
    
- `git switch --detach CODIGO` — permite consultar una versión anterior.
    
- `git switch main` — vuelve a la versión actual de la rama principal.
    
- `git check-ignore -v archivo` — comprueba qué regla de `.gitignore` excluye un archivo.
    

## 🛠️ Qué he hecho

- He creado una bóveda nueva en Obsidian llamada `Boveda_HTML_Casa`.
    
- He creado las carpetas necesarias para organizar el proyecto y la bitácora.
    
- He creado el archivo `.gitignore` para evitar que los vídeos se suban a GitHub.
    
- He creado la primera página `index.html` mostrando que el portátil estaba disponible.
    
- He inicializado Git dentro de `01_Proyecto` y he creado la rama `main`.
    
- He creado un repositorio vacío en GitHub y lo he conectado mediante SSH.
    
- He guardado y subido la primera versión de la página web.
    
- He cambiado el estado del portátil a reservado para mantenimiento y he guardado la segunda versión.
    
- He creado las páginas `normas.html` y `contacto.html`, he añadido una imagen y he enlazado las páginas.
    
- He añadido dos vídeos de prueba y he comprobado que Git los ignoraba.
    
- He preparado los cuatro archivos de la ampliación por separado, he revisado los cambios y he guardado la tercera versión.
    
- He consultado el historial, he abierto el primer commit y después he vuelto a `main`.
    
- He comprobado que la versión actual seguía funcionando y que los cambios estaban subidos a GitHub.
    

## 🚩 Qué me ha fallado y cómo lo he resuelto

Al cambiar el nombre del archivo `.gitignore`, me equivoqué al escribir la ruta y el nombre del archivo.

Los mensajes de error que aparecieron fueron:

```
fatal: pathspec '.gitignore' did not match any files
```

```
mv: cannot stat 'gitignore.md': No such file or directory
```

El problema era que el archivo no tenía el nombre que estaba utilizando en el comando. Para corregirlo, había que utilizar el nombre que tenía en ese momento y renombrarlo así:

```
mv gitignore .gitignore
```

Después, comprobé el nombre con:

```
ls -la
```

Y, una vez corregido, podía añadirlo a Git con:

```
git add .gitignore
```

## 🤔 Respuestas a las preguntas

### 1. ¿Por qué Git se inicializa solo en `01_Proyecto` y la grabación queda fuera?

Porque `01_Proyecto` es la carpeta que contiene los archivos del proyecto que queremos controlar con Git. Así evitamos incluir archivos de configuración de Obsidian y otros elementos que no forman parte de la entrega. La grabación queda fuera porque es un archivo de documentación y no debe formar parte del repositorio.

### 2. ¿Qué muestran `status` y `diff` antes de preparar la corrección del procedimiento? Cita la instrucción anterior y la nueva.

`git status` muestra que el archivo ha sido modificado, pero todavía no está preparado para el commit. `git diff` permite ver exactamente qué ha cambiado: el signo `-` indica la instrucción anterior y el signo `+` la nueva.

En esta práctica, el cambio de la portada fue:

- **Instrucción anterior:** `Equipo 01: disponible.`
    
- **Instrucción nueva:** `Equipo 01: reservado para mantenimiento.`
    

### 3. ¿Por qué un archivo nuevo aparece en `status` pero no en el `diff` de `README.md`?

Porque `git status` muestra tanto los archivos modificados como los archivos nuevos que Git todavía no sigue. En cambio, `git diff -- README.md` compara los cambios de ese archivo concreto y no muestra el contenido de otros archivos nuevos que aún no se han añadido al control de versiones.

### 4. ¿Qué preparas con cada `add` y qué compruebas con `diff --cached` antes del commit?

Con cada `git add` preparo un archivo concreto para incluirlo en el siguiente commit. En la ampliación preparé individualmente:

- `web/normas.html`
    
- `web/contacto.html`
    
- `web/imagenes/portatil.png`
    
- `web/index.html`
    

Con `git diff --cached --stat` compruebo un resumen de los cuatro archivos preparados y las modificaciones que se incluirán en el commit.

### 5. ¿Qué demuestra `check-ignore` y qué comprobaste además para saber que los clips existen?

El comando `git check-ignore -v` demuestra qué regla de `.gitignore` está excluyendo los vídeos y en qué línea se encuentra esa regla. Además, comprobé que los dos clips existían dentro de `web/videos/`. Así confirmé que estaban guardados localmente, pero que no se subirían a GitHub.

### 6. ¿Qué diferencias concretas observaste en el manual del primer commit y qué recuperaste al volver a `main`?

Al visitar el primer commit recuperé la versión inicial de la página, en la que el equipo aparecía como disponible y todavía no estaban las páginas adicionales ni la imagen. Al volver a `main` recuperé la versión más reciente, con el equipo reservado para mantenimiento, la imagen y los enlaces a las páginas de normas y contacto.

### 7. ¿Qué aporta un historial cuando dos técnicos necesitan conocer el procedimiento vigente?

El historial permite saber qué cambios se han realizado, cuándo se guardaron y qué versión estaba vigente en cada momento. También permite comparar versiones y recuperar una anterior si aparece algún problema. Si trabajan dos técnicos, GitHub les permite compartir el repositorio y consultar los cambios publicados.

### 8. ¿Por qué `commit` y `push` son acciones diferentes y qué miraste en GitHub?

`commit` guarda una versión de los cambios en el historial local del ordenador, mientras que `push` envía esos commits al repositorio remoto de GitHub. En GitHub comprobé que aparecían los archivos y que la página mostraba el estado actualizado del equipo, además de las páginas y la imagen añadidas.

### 9. ¿Qué pasos repetirías para corregir otra instrucción y cuáles se hicieron una sola vez?

Para corregir otra instrucción repetiría estos pasos:

1. Editar el archivo y guardar el cambio.
    
2. Ejecutar `git status` para comprobar que está modificado.
    
3. Ejecutar `git diff` para revisar el cambio.
    
4. Usar `git add` para preparar el archivo.
    
5. Revisar lo preparado con `git diff --cached`.
    
6. Crear un commit con `git commit`.
    
7. Subirlo con `git push`.
    

No repetiría `git init` ni `git remote add origin`, porque el repositorio ya está inicializado y conectado con GitHub.

## 🔗 Enlaces

- **Vídeo de esta fase:** 
    
- **Playlist:** 
    

## 💭 Dudas / a repasar

- Repasar la diferencia entre `git status`, `git diff` y `git diff --cached`.
    
- Recordar que `git add` prepara los archivos, `git commit` guarda los cambios localmente y `git push` los sube a GitHub.
    
- Tener cuidado al escribir los nombres y las rutas de los archivos, especialmente `.gitignore`.
    
- Recordar cómo consultar un commit anterior con `git switch --detach` y cómo volver a `main`.