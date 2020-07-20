Ray Tracing en un fin de semana
====================================================================================================

| ![RT in One Weekend][cover1] | ![RT The Next Week][cover2] | ![RT The Rest of Your Life][cover3] |
|:----------------------------:|:---------------------------:|:-----------------------------------:|
|   [In One Weekend][book1]    |   [The Next Week][book2]    |   [The Rest of Your Life][book3]    |


Conseguir los libros
------------------
La serie de libros _Ray Tracing in One Weekend_ ahora está disponible para el público de forma gratuita directamente
de la web:

  - [Ray Tracing in One Weekend][web1]
  - [Ray Tracing: The Next Week][web2]
  - [Ray Tracing: The Rest of Your Life][web3]

Estos libros han sido formateados tanto para pantalla como para impresión. Para copias impresas o para crear PDF versiones, utilice la función de impresión en su navegador.

Noticias
-----
2020-May-5 - ¡Lanzada la v3.1.0! Un parche de nivel menor más pequeño para planchar algunas de las cosas más grandes que quería cambiar después de un año de organización. El mayor cambio en el texto es la separación de capítulos en subcapítulos. No hay un cambio importante en la fuente, pero hay un gran cambio. cantidad de cambios pequeños y significativos.


Estructura de directorios
-------------------
La organización de este repositorio debe ser simple y evidente a simple vista:

### books/
Esta carpeta contiene los tres libros de trazado de rayos (en HTML) y algunos materiales de apoyo.

### images/
Contiene todas las imágenes y figuras de los libros. También se puede usar para comparar sus resultados.

### style/
Contiene el CSS para los libros y el sitio.

### src/
Contiene los codigos fuente.

### src/common/
Contiene los encabezados que son comunes a dos o más libros. Aquí también es donde los encabezados externos se almacenan.

### src/<book>/
Contiene la fuente específica de cualquier libro. No se comparte la fuente fuera de lo común directorio.


Código fuente
-----------
### Intención
Este repositorio no está destinado a actuar como su propio tutorial. La fuente presentada aquí se proporciona así puedes comparar tu trabajo al avanzar en el libro. Recomendamos encarecidamente leer y
siguiendo junto con el libro para entender la fuente.


### Descargar el código fuente
El [GitHub home][] para este proyecto contiene toda la fuente y documentación asociada con el _Ray
Tracing en un fin de semana_ serie de libros. Para clonar o descargar el código fuente, vea el verde "Clonar o descargar "en la esquina superior derecha de la página de inicio del proyecto.

### Lenguaje de programación
Este libro está escrito en C ++ y utiliza algunas características modernas de C ++ 11. El lenguaje y las características fueron elegido para ser ampliamente entendido por la mayor colección de programadores. No es para representa el código ideal de C ++.

### Implementaciones en otros lenguajes
La serie _Ray Tracing in One Weekend_ tiene una larga historia de implementaciones en otros lenguages de 
programación (consulte [_Implementations in Other Languages_][implementations]), y en los tres
sistemas operativos primarios ¡No dude en agregar su propia implementación a la lista!

### Ramas
La rama `master` contiene el código de la última versión. Todo el desarrollo continuo, con todos los
Los últimos cambios se pueden encontrar en las ramas `dev-patch`,` dev-minor` y `dev-major`.


Construyendo y corriendo
---------------------
Se proporcionan copias de la fuente para que pueda verificar su trabajo y compararlo. Si deseas construir
la fuente provista, el proyecto usa CMake. En la raíz del directorio del proyecto, ejecute lo siguiente
comandos para construir la versión de depuración de cada ejecutable:

    $ cmake -B build
    $ cmake --build build

Puede especificar el objetivo con la opción `--target <program>`, donde el programa puede ser `inOneWeekend`,` theNextWeek`, `theRestOfYourLife`, o cualquiera de los programas de demostración. Por defecto (sin la opción `--target`), CMake construirá todos los objetivos.

En Windows, puede compilar `debug` (el valor predeterminado) o` release` (la versión optimizada). Para
especificar esto, use la opción `--config <debug|release>`.

### CMake GUI en Windows
Puede optar por utilizar la GUI de CMake al construir en Windows.

1. Abra CMake GUI en Windows
2. Para "Dónde está el código fuente:", establezca la ubicación del directorio copiado. Por ejemplo,
    `C:\Usuarios\Peter\raytracing.github.io`.
3. Agregue la carpeta "build" dentro de la ubicación del directorio copiado. Por ejemplo,
    `C: \ Usuarios \ Peter \ raytracing.github.io \ build`.
4. Para "Dónde compilar los binarios", configúrelo en el directorio de compilación recién creado.
5. Haga clic en "Configurar".
6. Para "Especificar el generador para este proyecto", configúrelo en su versión de Visual Studio.
7. Haga clic en "Listo".
8. Haga clic en "Configurar" nuevamente.
9. Haga clic en "Generar".
10. En el Explorador de archivos, navegue al directorio de compilación y haga doble clic en el proyecto `.sln` recién creado.
11. Construir en Visual Studio.

Si el proyecto se clona y construye con éxito, puede usar el terminal nativo de su
sistema operativo para simplemente imprimir la imagen al archivo.

### Ejecutando los programas

En Linux u OSX, desde la terminal, ejecute así:

    $ build/inOneWeekend > image.ppm

En Windows, ejecute así:

    build\debug\inOneWeekend > image.ppm

o ejecute la versión optimizada (si ha compilado con `--config release`):

    build\release\inOneWeekend > image.ppm

El archivo PPM generado se puede ver directamente como una imagen de computadora normal, si su sistema operativo admite este tipo de imagen. Si su sistema no maneja archivos PPM, entonces debería poder encontrar Visores de archivos PPM en línea. Nos gusta [ImageMagick][].


Correcciones y Contribuciones
----------------------------
Si detecta errores, ha sugerido correcciones o desea ayudar con el proyecto, por favor
revise el documento [CONTRIBUTING][] para conocer la forma más efectiva de proceder.



[book1]:                    books/RayTracingInOneWeekend.html
[book2]:                    books/RayTracingTheNextWeek.html
[book3]:                    books/RayTracingTheRestOfYourLife.html
[CONTRIBUTING]:             ./CONTRIBUTING.md
[cover1]:                   images/RTOneWeekend-small.jpg
[cover2]:                   images/RTNextWeek-small.jpg
[cover3]:                   images/RTRestOfYourLife-small.jpg
[GitHub home]:              https://github.com/kurganpsp/raytracing_raw.github.io
[ImageMagick]:              https://imagemagick.org/
[web1]:                     https://raytracing.github.io/books/RayTracingInOneWeekend.html
[web2]:                     https://raytracing.github.io/books/RayTracingTheNextWeek.html
[web3]:                     https://raytracing.github.io/books/RayTracingTheRestOfYourLife.html
[implementations]:          https://github.com/RayTracing/raytracing.github.io/wiki/Implementations-in-Other-Languages
