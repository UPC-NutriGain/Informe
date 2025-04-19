# Capitulo V: Product Implementation, Validation & Deployment
## 5.1. Software Configuration Management
- ### 5.1.1. Software Development Environment Configuration
Para el desarrollo de NutriGain, se adoptó una estrategia basada en entornos especializados para cada componente de la solución: Landing Page, Aplicación Web y Backend RESTful. Esto permitió garantizar independencia en los despliegues y escalabilidad de cada módulo.

### Desarrollo del Landing Page

El equipo eligió una implementación con HTML, CSS y JavaScript puro, priorizando la carga rápida y la simplicidad en el diseño. Esta página sirve como presentación comercial de la aplicación y punto de entrada para nuevos usuarios interesados en conocer los beneficios del enfoque fitness personalizado de NutriGain.

Las herramientas empleadas son las siguientes:

### Live server:

Utilizado para agilizar el desarrollo de la Landing Page, esta herramienta permitió visualizar en tiempo real cada cambio hecho en el código, mejorando así la productividad y reduciendo errores de diseño visual.


<div style="text-align: center;">
    <img src="https://github.com/user-attachments/assets/708d1b66-1414-47d3-9368-02fb18735db8" alt="Descripción de la imagen">
</div>


### Git y GitHub:

Se decidió hacer uso de estas herramientas por la razón de que hoy en día es un estándar usar Git para el control de versiones de software y se eligió GitHub por ser la plataforma más popular y fácil de usar para crear y manejar repositorios de software, tener funciones para ver los cambios, commits, pull requests y entre otros. El enlace de descarga del instalador de GitHub Desktop es [GitHub Desktop](https://github.com/apps/desktop)


<div style="text-align: center;">
    <img src="https://github.com/user-attachments/assets/ff491b7b-1eaa-4c21-b23d-738291b25da5" alt="Descripción de la imagen">
</div>


### Desarrollo de la Aplicacion Web

La aplicación web fue construida con Vue.js en el frontend, lo cual facilitó la creación de una interfaz dinámica para personalizar rutinas, visualizar el progreso del usuario y controlar el avatar fitness. El backend fue desarrollado en .NET Core, ideal para estructurar los servicios RESTful que gestionan los planes de nutrición, estadísticas y retos semanales aleatorios.

Las herramientas claves son las siguientes:


### JetBrains WebStorm:

Se eligió esta herramienta para el desarrollo del frontend de NutriGain ya que ofrece integración nativa con Vue.js, utilizado para implementar la lógica de la interfaz de usuario personalizada. WebStorm también brinda autocompletado inteligente, detección de errores en tiempo real y compatibilidad con componentes modulares, lo que facilitó el trabajo colaborativo entre los desarrolladores.

<div style="text-align: center;">
    <img src="/images/img/webstorm.png" alt="Descripción de la imagen" width="700">
</div>

### JetBrains Rider:

Esta herramienta fue clave para implementar el backend con .NET Core, ya que proporciona un entorno de desarrollo robusto para servicios RESTful y permite integrar fácilmente bases de datos y lógica de negocio. Su compatibilidad con C# y sus herramientas de depuración permitieron mantener el control sobre la lógica de personalización de rutinas y planes alimenticios.


<div style="text-align: center;">
    <img src="/images/img/rider.jpeg" alt="Descripción de la imagen" width="700">
</div>


### Node.js y npm:

Fueron necesarios para la gestión de dependencias del proyecto frontend en Vue.js, como frameworks de diseño, librerías de gráficos de progreso y validadores de formularios. Además, el entorno Node permitió ejecutar scripts de compilación y pruebas unitarias.

<div style="text-align: center;">
    <img src="/images/img/nodeandnpm.png" alt="Descripción de la imagen" width="700">
</div>

Esta separación por entornos y herramientas permitió una mayor eficiencia en la entrega y pruebas.


- ### 5.1.2. Source Code Management

Para mantener el orden al desarrollar una solución y evitar conflictos o superposiciones de información, los proyectos se trabajaron en un organización de GitHub y dentro de esta se encuentran los diferentes repositorios para cada proyecto cuyos enlaces de los repositorios son los siguientes:

Repositorio para el [landing page]()

Repositorio para los [tests de aceptación]()

Repositorio de la aplicación web :
- [FrontEnd]()
- [Backend]()

Se aplicó el modelo de ramas GitFlow, con una estructura compuesta por:
- *main*: que almacenará las versiones estables y finales

- *develop*: donde se irán integrando los cambios implementados por cada feature y estará en constante actualización

- *feature/*: nuevas características, como edición del perfil o seguimiento gráfico de progreso

Para los commits se adoptó la convención Conventional Commits, permitiendo organizar fácilmente los cambios mediante etiquetas como *feat, fix, docs,* entre otros

<div style="text-align: center;">
    <img src="/images/img/GITFLOW.JPG" alt="Descripción de la imagen" width="500">
</div>


- ### 5.1.3. Source Code Style Guide & Conventions

Se definieron guías de estilo para cada tecnología utilizada, con el objetivo de garantizar coherencia y facilitar el mantenimiento.

- **HTML/CSS:** etiquetas en minúsculas, cierre correcto de elementos, nombres de clase descriptivos en kebab-case, uso de propiedades abreviadas y alt obligatorio en imágenes.

- **JavaScript:** uso de const y let, evitar variables globales, nombramiento en camelCase, comentarios para funciones complejas.

- **Vue.js:** uso modular por componentes, uso correcto de v-bind, v-model, v-for, computed y watch. Comunicación entre componentes vía props y eventos.

- **.NET (C#):** declaración con var donde sea evidente, buenas prácticas en métodos asíncronos con sufijo Async, uso de using para liberar recursos y comentarios XML en endpoints públicos.

- **Gherkin:** estructuración clara con Given-When-Then, uso de tablas para parámetros complejos y separación de escenarios.


- ### 5.1.4. Software Deployment Configuration

### **Despliegue del Landing Page**

La landing page fue desplegada con GitHub Pages, configurando la rama principal como fuente de publicación. Se eligió esta opción por su facilidad de integración con GitHub, cero costos de hosting y rapidez para realizar actualizaciones visuales.

Para realizar esto se realizaron los siguientes pasos:

1. Una vez que se haya lanzado el release al repositorio y las ramas estén actualizadas, se procede a ingresar a GitHub, luego acceder al repositorio del proyecto y seguidamente hacer click en la pestaña “Settings”, buscar el ítem “Pages” del menú lateral.

![Landing page]()

![Setting Landing page]()

2. Seleccionar la rama principal y confirmar los cambios, luego de esto GitHub comenzará el proceso de deploy. Cuando GitHub tenga listo el enlace público, este se podrá ver desde el mismo menú en la parte superior.


![Changes Landing Page]()


Link de la [landing page]()


### **Despliegue de la Aplicación Web**

Para el frontend de la aplicación NutriGain, se utilizó Vercel, aprovechando sus capacidades de CI/CD, soporte para frameworks modernos y facilidad de configuración para proyectos en Vue.js.

<div style="text-align: center;">
    <img src="/images/img/vercel.png" alt="Descripción de la imagen" width="400">
</div>


### **Despliegue del Backend RESTful**

El backend fue desplegado en Render, donde se configuraron entornos de desarrollo y producción con acceso a base de datos. Además, se generó documentación interactiva con Swagger, accesible públicamente en:

Link de la [BackEnd RESTful]()


## 5.2. Landing Page, Services & Applications Implementation

 - ### 5.2.1. Sprint 1
   - ### 5.2.1.1. Sprint Planning 1

   Durante esta primera planificación del sprint, el equipo definió los objetivos clave para comenzar a dar vida a la app NutriGain desde su página de presentación. 
   El foco principal fue diseñar una Landing Page atractiva y funcional que refleje de manera clara qué es NutriGain, sus caminos fitness y cómo funciona el sistema del avatar y los retos. 
   Esta planificación estableció las bases visuales y comunicativas del producto.
      
      - **Sprint Goal:** Crear una versión inicial de la Landing Page que sea visualmente atractiva, informativa y funcional para captar el interés de los usuarios potenciales y explicar los beneficios únicos de NutriGain (como el camino fitness, el avatar personalizado, el plan nutricional y los retos extremos).

      - ####  Fecha de planificación: 10 de abril de 2025

         #### Herramientas utilizadas:

        - **Trello:** Para organizar el backlog de historias de usuario y asignar tareas.

        - **GitHub Projects:** Para el seguimiento técnico de commits, ramas y avances del repositorio.

        - **Google Meet:** Para reuniones virtuales y acuerdos de planificación.

        - **Figma :** Se sugirió como herramienta para prototipado visual, especialmente útil si se desea incluir una imagen del wireframe inicial.


   - ### 5.2.1.2. Sprint Backlog 1

   sd
   - ### 5.2.1.3. Development Evidence for Sprint Review

   - ### 5.2.1.4. Testing Suite Evidence for Sprint Review

   - ### 5.2.1.4. Execution Evidence for Sprint Review

   - ### 5.2.1.5. Services Documentation Evidence for Sprint Review

   - ### 5.2.1.6. Software Deployment Evidence for Sprint Review

   - ### 5.2.1.7. Team Collaboration Insights during Sprint

     





