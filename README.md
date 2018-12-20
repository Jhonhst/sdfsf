# herbalife-web-2018

> A Vue.js project

## Build Setup

``` bash
# install dependencies
npm install

# serve with hot reload at localhost:8080
npm run dev

# build for production with minification
npm run build

# build for production and view the bundle analyzer report
npm run build --report
```

For detailed explanation on how things work, checkout the [guide](http://vuejs-templates.github.io/webpack/) and [docs for vue-loader](http://vuejs.github.io/vue-loader).

El idioma por defecto es el ingles.

1:al hacer clic en una bandera se activa un metodo que guarda la abreviación del idioma al cual pertenece dicha bandera, guarda el valor en el storage para fururas peticiones.

2: se hace una petición a traves de una api a https://emeavacationreg.com/cmsweb/ por del metodo get con la abreviatura del idioma mas el numero de página para saber que contenido traer.

3: la api se encuentra en https://emeavacationreg.com/cmsweb/ y se modifica a través de Wordpress 
#https://emeavacationreg.com/cmsweb/wp-admin

#user: admin
#password: mocion.2040

4: al crear un contenido nuevo en nuestro sitio también se debe crear los textos a mostrar pero en wordpress y en ves de colocar los textos directamente en las vistas se hace de forma dinamica, guardando la respuesta de la api en una variable la cual llamara los textos traducidos dependiendo de la abrevitura de idiama y pagina seleccionada.
