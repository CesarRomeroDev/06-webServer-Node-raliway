# 06-webServer-Node.

## Configuración Inicial NPM.

1- Para iniciar, crearemos el archivo package.json. El archivo json es de gran utilidad en el futuro, ya que cuenta con las versiones instaladas en el proyecto.

```
npm init -y
```

2- Instalamos express js con el siguiente comando

```
 npm i express
```

3- Una vez intalado express, creamos el archivo con el nombre app.js e ingresamos el siguiente codigo.

```
const express = require('express')
const app = express()

app.get('/', (req, res) => {
  res.send('Hello World')
})

app.listen(3000)
```

4- Ingresamos a la consola donde se encuentra el archivo del proyecto y corremos el servidor con el siguiente comando:

```
nodemon app
```


## Desplegar apicacación.

1- instalamos env con el siguiente comando:

```
npm i dotenv --save
```

2- Creamos en archivo .env en la raíz del proyecto, e ingresamos lo siguiente:

```
PORT=8081
```

3- Ingresamos al archivo app.js y colocamos la variable de entorno como el siguente codigo:

```
require('dotenv').config();   //variable de entorno
```

4- En la variable port la inicializamos con lo siguente:

```
const port = process.env.PORT;
```

5- El siguiente paso es ingresar al archivo package.js y en el apartado de "scripts" esyto se hace para que el servidor busque la direccion correcta y renderize. ingresar lo siguiente:

```
"start": "node app.js"
```

## Probar aplicación antes de desplegarla. usando [http-server](https://www.npmjs.com/package/http-server)

1- instalar http-server:

```
npm install --global http-server
```

2- Ingresamos mediante consola al proyecto y en consola ingresamos el siguiente comando:

```
http-server -o
```

3- Podemos observar que la aplicación esta corriendo.

## probar aplicación de Reac en nuestro proyecto 06-webserver.

1- Ingresamos a las carpetas del proyecto de la raiz.

2- Copiamos todas las carpetas y la pegamos en el proyecto 06-webserver en la carpeta public eliminando los archivos anteriores.

3- Probamos que funciones con el siguiente comando desde el proyecto 06-webserver.

```
nodemon app
```

## Desplegar nuevos cambios en Rallway

1- Para desplegar nuevos cambios en Rallway te nemos que ingresar al proyecto en rallway.

2- Ingresar al proyecto y en el apartado de settings observar en el deploy tengamos la opción de main.

3- Una vez observado ese detalle, solo es cuestion de hacer un push en nuestro proyecto principal y se hacen los cambios al recargar la página.
