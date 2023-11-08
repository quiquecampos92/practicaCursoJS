# Desarrollo de la práctica

## Introducción a Git

Git es una herramienta fundamental en el mundo del desarrollo de software, revolucionando la forma en que gestionamos el control de versiones de nuestros proyectos. Permite a equipos de desarrollo colaborar de manera eficiente, mantener un historial preciso de cambios y revertir a versiones anteriores con facilidad.

## Metodología GitFlow: Organizando Nuestro Flujo de Trabajo

En nuestro enfoque de desarrollo, adoptamos la metodología GitFlow. Esta metodología proporciona una estructura organizada y clara para gestionar el ciclo de vida del código fuente. Se basa en la creación de diversas ramas para distintos propósitos, lo que nos permite llevar a cabo desarrollos de manera más segura y controlada.

## Ramas Clave en GitFlow: Developer y Main

En GitFlow, al menos dos ramas principales coexisten en nuestro repositorio: `developer` y `main`. La rama de `developer` es donde se fusionan las características nuevas y las correcciones de errores antes de ser desplegadas. Esto garantiza que las nuevas funcionalidades sean probadas y se integren de manera adecuada. La rama `main` es la encargada de llevar a producción el proyecto.

## Ramas Especializadas: Feature, Test y Hotfix

Además de las ramas principales, GitFlow nos anima a utilizar otras ramas especializadas. Las ramas de `feature/` nos permiten trabajar en nuevas funcionalidades de manera aislada, lo que facilita el seguimiento y prueba de estas características. Estas ramas no tienen porque salir de una principal llamada feature, simplemente pueden salir de developer, pero en el nombre indicar `feature/ejemplo`. Las ramas de `test` sirven para realizar pruebas rigurosas antes de la fusión con `main`. Estas serán hijas de developer y solo aparecerán cuando las ramas de features estén fusionadas con developer. Después de probar los test se fusiona con main y se deben eliminar. Por último, las ramas de `hotfix` se centran en la corrección de errores críticos en producción de forma rápida y efectiva.

## Rama para la documentación: gh_pages

Por último, se creará una rama para subir la documentación del proceso del proyecto denominada `gh_pages` la cual será la que se suba a github pages.

## Beneficios de GitFlow en Nuestro Desarrollo

La adopción de GitFlow en nuestro proceso de desarrollo nos proporciona una serie de ventajas significativas. Nos brinda un mayor control sobre el flujo de trabajo, facilita la colaboración entre equipos y garantiza una mayor estabilidad en el ciclo de vida del código fuente.

## Pasos a seguir por los usuarios

### USUARIO 1

1. Crea repositorio en blanco
   ![Imagen](src/imágenes/Imagen%201.jpg)

2. Clonamos el repositorio indicado en la práctica `boilerplate` en local y modificamos para crear la web como se indica en la práctica. Así cuando subamos a remoto ya tiene el contenido principal.
   ![Imagen](src/imágenes/Imagen%202.jpg)

3. Asociamos el remoto a local con git remote, después hacemos los commits del proyecto para poder subirlo y realizamos el push para subirlo a remoto. También se podría hacer el git remote después de los commits y antes del push.
   ![Imagen](src/imágenes/Imagen%203.jpg)

4. Se crea la rama developer ya que la main está creada por defecto.
      ![Imagen](src/imágenes/Imagen%204.jpg)

5. Creamos la estructura de la web en la rama developer para que al crear las otras ramas tengan la base.
      ![Imagen](src/imágenes/Imagen%205.jpg)


### USUARIO 2

6. El usuario 2 se posiciona en la rama developer
      ![Imagen](src/imágenes/Imagen%206.jpg)

7. Crea las dos ramas pertinentes
      ![Imagen](src/imágenes/Imagen%207.jpg)


### USUARIO 3

8. El usuario 3 se posiciona en la rama developer
      ![Imagen](src/imágenes/Imagen%208.jpg)

9.  Crea la rama pertinente
       ![Imagen](src/imágenes/Imagen%209.jpg)

10. Al final las ramas creadas quedan así:
    a. Main
    b. Developer
       i. Feature/contenidoHTML
       ii. Feature/atributosHTML
       iii. Feature/estilosCSS

### USUARIO 1

11. Una vez creadas las ramas se suben a remoto para que se guarden y los demás usuarios puedan disponer de ellas.
       ![Imagen](src/imágenes/Imagen%2011.jpg)


### USUARIO 3

12. Una vez creadas las ramas se suben a remoto para que se guarden y los demás usuarios puedan disponer de ellas.
       ![Imagen](src/imágenes/Imagen%2012.jpg)


### USUARIO 2

13. Una vez creadas las ramas se suben a remoto para que se guarden y los demás usuarios puedan disponer de ellas.
       ![Imagen](src/imágenes/Imagen%2013.jpg)

14. Cada usuario ha subido las respectivas ramas a remoto para que todos puedan disponer de ellas.
15. Ahora deben implementar el código en su rama y subirlo.

### USUARIO 2

16. Modifica el contenido y añade un commit en la rama feature/contenidoHTML
       ![Imagen](src/imágenes/Imagen%2016.jpg)

17. Modifica los atributos y añade un commit en la rama feature/atributosHTML
       ![Imagen](src/imágenes/Imagen%2017.jpg)


### USUARIO 3

18. Modifica los estilos CSS y añade un commit en la rama feature/estilosCSS
       ![Imagen](src/imágenes/Imagen%2018.jpg)


### USUARIO 2

19. Cada usuario sube las modificaciones a remoto con push
        ![Imagen](src/imágenes/Imagen%2019a.jpg)
        ![Imagen](src/imágenes/Imagen%2019b.jpg)



### USUARIO 3

20. Crea rama test sobre developer
       ![Imagen](src/imágenes/Imagen%2020.jpg)

21. Fusionamos la rama feature/atributosHTML
       ![Imagen](src/imágenes/Imagen%2021.jpg)

22. Fusionamos la rama feature/contenidoHTML
       ![Imagen](src/imágenes/Imagen%2022.jpg)

23. Fusionamos la rama feature/estiloCSS. Nos sale un conflicto y lo solucionamos guardando ambos cambios (Aceptar ambos cambios).
       ![Imagen](src/imágenes/Imagen%2023.jpg)

24. Commit en la rama developer para guardar el cambio del archivo
       ![Imagen](src/imágenes/Imagen%2024.jpg)


### USUARIO 1

25. Ahora fusionamos la rama developer con la main
       ![Imagen](src/imágenes/Imagen%2025.jpg)

26. Etiqueta la rama main con la etiqueta “v1.0”
       ![Imagen](src/imágenes/Imagen%2026.jpg)

27. Aquí se puede ver como existe la etiqueta
       ![Imagen](src/imágenes/Imagen%2027.jpg)

28. Procedemos a crear los Hooks
29. El ususario 1, como es el encargado empieza a crear hooks
    a. Automatización de la instalación del proyecto. Cuando se realice un clonado/checkout del proyecto, se deberá recrear la carpeta de node_modules del proyecto.
       ![Imagen](src/imágenes/Imagen%2029a.jpg)

    b. Otorgamos permisos para poder acceder
       ![Imagen](src/imágenes/Imagen%2029b.jpg)

30. Verificación del formato de mensaje de commit.
       ![Imagen](src/imágenes/Imagen%2030a.jpg)

    Otorga permisos
       ![Imagen](src/imágenes/Imagen%2030b.jpg)

    Formato:
        MOTIVO DEL COMMIT: <título>
        IMPLEMENTACIÓN: <explicación>
31. Previo a realizar el commit, se verificará el correcto formato en los ficheros html. Para ello, se ejecutará el linter eslint (suponiendo que el plugin ya esta instalado).
       ![Imagen](src/imágenes/Imagen%2031.jpg)

32. Permisos
       ![Imagen](src/imágenes/Imagen%2032.jpg)

33. Se crea una carpeta para poder subir a github y que todos puedan disponer de ellos
       ![Imagen](src/imágenes/Imagen%2033.jpg)


