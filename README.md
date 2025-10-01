<center>

# Documentación y sistema de control de versiones

</center>

**_Nombre: Dario Acosta y Jose Carballeda_**
**_Curso:_** 2º de Ciclo Superior de Desarrollo de Aplicaciones Web.

### ÍNDICE

- [Introducción](#id1)
- [Objetivos](#id2)
- [Material empleado](#id3)
- [Desarrollo](#id4)
- [Conclusiones](#id5)

#### **_Introducción_**. <a name="id1"></a>

La documentación y el control de versiones son piezas fundamentales en el desarrollo de software. La documentación proporciona una guía clara sobre el propósito, uso y arquitectura de la solución, mientras que el sistema de control de versiones permite gestionar cambios a lo largo del tiempo, colaborar eficazmente en equipo y mantener un histórico reproducible de todo el proyecto. Esta práctica aborda conceptos básicos de documentación técnica, tipos de documentación (técnica, de usuario, de instalación) y las prácticas comunes de control de versiones (ramas, commits, mensajes de commit, PRs, releases). El objetivo es entender cómo construir una base sólida de documentación que acompañe al código y facilita la colaboración y la trazabilidad.

#### **_Objetivos_**. <a name="id2"></a>

- Comprender la importancia de la documentación en proyectos de software.
- Conocer los principios del control de versiones.
- Aprender a estructurar un repositorio.
- Desarrollar habilidades para crear y gestionar ramas, commits y releases.
- Fomentar buenas prácticas de colaboración.

#### **_Material empleado_**. <a name="id3"></a>

- Repositorio Git
- Herramientas de hosting de código (por ejemplo, GitHub, GitLab o Bitbucket).
- Plantillas de documentación (por ejemplo, README)
- Processos de flujo de trabajo: ramas , mensajes de commit descriptivos, issues y pull requests.

#### **_Desarrollo_**. <a name="id4"></a>

- El alumnado trabajará por parejas: user1 y user2. Indicar quién es user1 y quién es user2.

  ![](/img/1.png)

- user1 creará un repositorio público llamado git-work en su cuenta de GitHub, añadiendo un README.md y una licencia MIT.

  ![](/img/2.png)

- user1 clonará el repo y añadirá los ficheros: index.html, bootstrap.min.css y cover.css. Luego subirá los cambios al upstream.

  ![](/img/3.png)
  ![](/img/4.png)
  ![](/img/5.png)

- user2 creará un fork de git-work desde su cuenta de GitHub.
- user2 clonará su fork del repo.
- user1 creará una issue con el título "Add custom text for startup contents".

  ![](/img/9.png)
  ![](/img/10.png)

- user2 creará una nueva rama custom-text y modificará el fichero index.html personalizándolo para una supuesta startup.
- user2 enviará un PR a user1.
- user1 probará el PR de user2 en su máquina (copia local) creando previamente un remoto denominado upstream.

  ![](/img/15.png)
  ![](/img/16.png)

  - realizará ciertos cambios en su copia local que luego deberá subir al propio PR.

  ![](/img/17.png)
  ![](/img/18.png)

- user1 y user2 tendrán una pequeña conversación en la página del PR, donde cada usuario incluirá, al menos, un cambio más.

  ![](/img/23.png)

- user1 finalmente aprobará el PR.

  ![](/img/24.png)

  - cerrará la issue creada (usando una referencia a la misma) y actualizará la rama principal en su copia local.

  ![](/img/25.png)

- user2 deberá incorporar los cambios de la rama principal de upstream en su propia rama principal.
- user1 creará una issue con el título "Improve UX with cool colors".

  ![](/img/26.png)

- user1 cambiará la línea 10 de cover.css a: color: purple;

  ![](/img/27.png)

- user1 hará simplemente un commit local en main → NO HACER git push.

  ![](/img/28.png)

- user2 creará una nueva rama cool-colors y cambiará la línea 10 de cover.css a: color: darkgreen;
- user2 enviará un PR a user1.

- user1 probará el PR de user2 (en su copia local). A continuación tratará de mergear el contenido de la rama cool-colors en su rama principal y tendrá que gestionar el conflicto: Dejar el contenido que viene de user2.

  ![](/img/29.png)
  ![](/img/30.png)
  ![](/img/31.png)

- Después del commit para arreglar el conflicto, user1 modificará la línea 11 de cover.css a: text-shadow: 2px 2px 8px lightgreen;

  ![](/img/32.png)

- user1 hará un commit especificando en el mensaje de commit el cambio hecho (sombra) y que se cierra la issue creada (usar referencia a la issue). A continuación subirá los cambios a origin/main.

![](/img/33.png)
![](/img/35.png)

- user1 etiquetará esta versión (en su copia local) como 0.1.0 y después de subir los cambios creará una "release" en GitHub apuntando a esta etiqueta.

  ![](/img/34.png)

> **_IMPORTANTE:_** si estamos capturando una terminal no hace falta capturar todo el escritorio y es importante que se vea el nombre de usuario.

Si encontramos dificultades a la hora de realizar algún paso debemos explicar esas dificultades, que pasos hemos seguido para resolverla y los resultados obtenidos.

#### **_Conclusiones_**. <a name="id5"></a>

- La documentación y el control de versiones son pilares fundamentales para un desarrollo sostenible y colaborativo. Un repositorio bien documentado y con un flujo de trabajo claro facilita la colaboración, reduce conflictos y mejora la trazabilidad de los cambios.

- Un flujo de trabajo basado en ramas, commits atómicos y mensajes descriptivos favorece la revisión de código y la calidad del software. Las prácticas recomendadas, como usar branchs de feature, PRs, y releases bien definidos, permiten integrar cambios de forma gradual y controlada.
