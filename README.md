# npm-basics

## Registros

### Github
Soporta de manera gratuito la subida de paquetes privados y públicos. La privacidad del paquete va a depender del repositorio, es decir, si el repositorio en Github está como privado, el paquete también quedará como privado.

### npmjs.com
El repositorio por defecto de NPM. De manera gratuita solo se puede subir paquetes públicos, para subir paquetes privados se deben pagar 7USD mensuales.


## NPMRC
Ejemplo de archivo .npmrc ubicado en la misma carpeta del proyecto.
Es util este archivo para poder instalar los paquetes que vienen de un repositorio distinto al por defecto (npmjs.com).
En el caso del registro de Github siempre es necesario un Token, este se puede conseguir en: https://github.com/settings/tokens .
Para un proyecto que solo instalará paquetes, basta con permisos de solo lectura.
Si se va a publicar un paquete, es necesario permisos de escritura sobre el repositorio. 

```
@hcslearning:registry=https://npm.pkg.github.com/hcslearning
//npm.pkg.github.com/:_authToken=508ff9650f537c8ee11f6619a04ab46b42cf60b7
```


## NPM LOGIN
Al hacer login se debe usar como password el token generado con anterioridad, en este caso el token debe tener permisos de escritura para poder publicar un paquete:

```
$ npm login --registry=https://npm.pkg.github.com --scope=@hcslearning
```

También existe el comando logout para salir de la sesión:
```
$ npm logout
```


## NPM PUBLISH

Antes de publicar un paquete es recomendable revisar con qué usuario hemos ingresado:

```
$ npm whoami
$ npm publish 
```
