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
### Intent
Este repositorio no está destinado a actuar como su propio tutorial. La fuente presentada aquí se proporciona así puedes comparar tu trabajo al avanzar en el libro. Recomendamos encarecidamente leer y
siguiendo junto con el libro para entender la fuente.


### Downloading The Source Code
The [GitHub home][] for this project contains all source and documentation associated with the _Ray
Tracing in One Weekend_ series of books. To clone or download the source code, see the green "Clone
or download" button in the upper right of the project home page.

### Programming Language
This book is written in C++, and uses some modern features of C++11. The language and features were
chosen to be broadly understood by the largest collection of programmers. It is not meant to
represent ideal C++ code.

### Implementations in Other Languages
The _Ray Tracing in One Weekend_ series has a long history of implementations in other programming
languages (see [_Implementations in Other Languages_][implementations]), and across all three
primary operating systems. Feel free to add your own implementation to the list!

### Branches
The `master` branch contains the code at latest release. All ongoing development, with all of the
latest changes, can be found in the `dev-patch`, `dev-minor`, and `dev-major` branches.


Building and Running
---------------------
Copies of source are provided for you to check your work and compare against. If you wish to build
the provided source, the project uses CMake. At the root of the project directory, run the following
commands to build the debug version of every executable:

    $ cmake -B build
    $ cmake --build build

You can specify the target with the `--target <program>` option, where the program may be
`inOneWeekend`, `theNextWeek`, `theRestOfYourLife`, or any of the demonstration programs. By default
(with no `--target` option), CMake will build all targets.

On Windows, you can build either `debug` (the default) or `release` (the optimized version). To
specify this, use the `--config <debug|release>` option.

### CMake GUI on Windows
You may choose to use the CMake GUI when building on windows.

1. Open CMake GUI on Windows
2. For "Where is the source code:", set to location of the copied directory. For example,
   `C:\Users\Peter\raytracing.github.io`.
3. Add the folder "build" within the location of the copied directory. For example,
   `C:\Users\Peter\raytracing.github.io\build`.
4. For "Where to build the binaries", set this to the newly-created build directory.
5. Click "Configure".
6. For "Specify the generator for this project", set this to your version of Visual Studio.
7. Click "Done".
8. Click "Configure" again.
9. Click "Generate".
10. In File Explorer, navigate to build directory and double click the newly-created `.sln` project.
11. Build in Visual Studio.

If the project is succesfully cloned and built, you can then use the native terminal of your
operating system to simply print the image to file.

### Running The Programs

On Linux or OSX, from the terminal, run like this:

    $ build/inOneWeekend > image.ppm

On Windows, run like this:

    build\debug\inOneWeekend > image.ppm

or, run the optimized version (if you've built with `--config release`):

    build\release\inOneWeekend > image.ppm

The generated PPM file can be viewed directly as a regular computer image, if your operating system
supports this image type. If your system doesn't handle PPM files, then you should be able to find
PPM file viewers online. We like [ImageMagick][].


Corrections & Contributions
----------------------------
If you spot errors, have suggested corrections, or would like to help out with the project, please
review the [CONTRIBUTING][] document for the most effective way to proceed.



[book1]:                    books/RayTracingInOneWeekend.html
[book2]:                    books/RayTracingTheNextWeek.html
[book3]:                    books/RayTracingTheRestOfYourLife.html
[CONTRIBUTING]:             ./CONTRIBUTING.md
[cover1]:                   images/RTOneWeekend-small.jpg
[cover2]:                   images/RTNextWeek-small.jpg
[cover3]:                   images/RTRestOfYourLife-small.jpg
[GitHub home]:              https://github.com/RayTracing/raytracing.github.io/
[ImageMagick]:              https://imagemagick.org/
[web1]:                     https://raytracing.github.io/books/RayTracingInOneWeekend.html
[web2]:                     https://raytracing.github.io/books/RayTracingTheNextWeek.html
[web3]:                     https://raytracing.github.io/books/RayTracingTheRestOfYourLife.html
[implementations]:          https://github.com/RayTracing/raytracing.github.io/wiki/Implementations-in-Other-Languages
