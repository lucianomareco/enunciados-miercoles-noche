# Instalación y configuración del entorno Prolog

Esta página te ayudará a instalar y configurar el entorno Prolog para realizar todas las prácticas del **paradigma lógico** para los cursos del miércoles a la noche.

## Prolog Online para salir del paso

Si necesitás hacer pruebas rápidas en tu celular, o tablet, o en el trabajo donde no te dejan instalar nada, utilizalo online mediante la página [SWISH](https://swish.swi-prolog.org/). Pero para las _katas_ o bien para el _trabajo práctico_, te dejamos el entorno recomendado.

## Ejecutable Prolog

El entorno ejecutable SWI Prolog se descarga desde este link: https://www.swi-prolog.org/download/stable.

> **IMPORTANTE**: que sea la versión 7.6 ó posterior para que se integre con Visual Studio Code

Si instalaste la versión 6.20, te recomendamos que

- la desinstales
- instales la nueva versión
- incorporen a la variable PATH del entorno del sistema operativo el ejecutable que está en `C:\Program Files\swipl\bin` (chequealo por las dudas) como se muestra [en este link](https://www.computerhope.com/issues/ch000549.htm)

El ejecutable en Prolog será

- `swipl` si estás en Windows
- `prolog` si estás en Linux/Mac

## Editor de texto

Existen [muchas opciones](https://wiki.haskell.org/IDEs), nosotros elegimos [Visual Studio Code](https://code.visualstudio.com/)

### Plugins adicionales

Para mejorar nuestra experiencia de Haskell con Visual Studio Code, se deben instalar los siguientes plugins:

- **VSC-Prolog**, de Arthur Wang. Te dejamos [la página que trae tutoriales para trabajar con el plugin](https://marketplace.visualstudio.com/items?itemName=arthurwang.vsc-prolog)

Si no lo instalaste previamente, recomendamos que incorpores a la lista de plugins

- **Markdown All in One**, para leer los enunciados con el formato [Markdown](https://help.github.com/articles/basic-writing-and-formatting-syntax/)
- **GitLens**, para integrar Git con Visual Studio

## Configuración adicional para Windows

Si estás en Windows probablemente el plugin no encuentre el ejecutable donde está SWI Prolog para compilarlo y mostrarte errores en el código. Si es así, cambiá la configuración donde está el ejecutable siguiendo [estos pasos](https://github.com/arthwang/vsc-prolog/issues/4), en la configuración sobreescribí el valor por defecto incorporando esta línea:

```json
 "prolog.executablePath": "C:\\Program Files\\swipl\\bin\\swipl"
```

o donde hayas instalado SWI Prolog (en mi caso lo instalé en C:\Program Files\swipl, eso genera una carpeta bin donde está el ejecutable `swipl.exe`). Si tu default es `C:\Program Files\pl`, fijate si no instalaste la versión 6 que no funciona con el plugin de Visual Studio Code.

> IMPORTANTE: Fijate que hay que usar doble contrabarra `\\`

![](../../images/prolog/vsc-prolog.gif)