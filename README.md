# MY-CLI-TASK
Desarrollo de una aplicacion en node, que consiste en un programa de consola que a traves de comandos como `save`, `delete` entre otros, permite hestionar una pequeña lista de tareas gusrdada en mongodb. Desarrollo tomado de [este video de Fazt][video de fazt]
***

## Tecnologías usadas
- comander: Modulo encargado de crear los comandos
- inquirer: Moudulo que permite recibir información del usuario desde consola (como un propmt)
- donenv: Para las variables de entorno y poder asi configurar una conexión a base de datos
- mongoose (adaptador para la bd mogoose)


***
## Como ejecutar en modo desarrollo
Solo corre en local. pues no se hizo despliegue, en caso de hacerlo ver en el video
Se debe correr mongod en local y luego ejecutar node
```
$ mongod
$ node src/index.js
```
***
## Cómo ejecutar con un nombre de comando
En este caso (ver mas abajo la manera) el programa se llama taskcli, así que su uso es
```
$ taskcli <comando>
```

***
## Descripción detallada del proyecto y caracteristicas
Este es un interesante proyecto el cual consiste en un programa que se ejecuta netamemte desde consola y el cual permite gestionar uan sencilla lista de tareas que estan almacenadas en mongodb. Lo bacano de este proyecto es que se muestra como con node es posible hacer aplicaciones de escritorio (en este caso es una aplicacion que funciona solo en consola)

La ejecución en etapa de desarrollo es con el comando
```
$ node src/index <Comando>
```
La ejecucion con el binario generado es con 
```
$ taskcli <Comando>
```
Los comandos que se usan son: `save`, `list`, `delete <id>`, `update <id>`, `find <text>` 

Por ejemplo 
`taskcli list` Muestra todas las listas guatrdadas

***
## Descripción de la estructra del proyecto
- index.js es el que permite inciar la ejecución del desarrollo
- db.js: Encargado de toda la conexión a la base de datos
- config: Se encarga de traer el valor de la variable de entorno para el caso que se haga un despliegue en la nube
- commands.js: Es el archivo principal donde se definen los comandos de la app
- Models: carpeta con el modemlo de tareas
- Controllers, alli están las funciones encargadas de los procesos

*** 
## Por menores del proyecto
1. Es interesante el uso de console.table() para mostrar la información en forma de tabla


## Mejoras futuras
-   Hacer la implementacion en mongo Atlas
***
### Maolink software
Version. 1.0.0

Enero 2021



[video de fazt]:<https://www.youtube.com/watch?v=tjqrtXU3V6M&t=2499s>










## Tasks CLI

Tasks CLI is a program to manage your tasks in a database using terminal or console. This is a sample project for beginners

### Requirements

- Nodejs
- Mongodb Local Installation or Cloud

### Installation

```sh
npm install
```

```sh
npm link
```

### Commands

```
tasks-cli --version
```

```
tasks-cli --help
```

```
tasks-cli list
tasks-cli l
```

```
tasks-cli find title
```

```sh
tasks-cli save
tasks-cli s
```

```sh
tasks-cli update <id>
```

```sh
tasks-cli delete <id>
tasks-cli d <id>
```
