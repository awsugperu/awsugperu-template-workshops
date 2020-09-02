
master branch: ![Build Status](https://codebuild.us-east-1.amazonaws.com/badges?uuid=eyJlbmNyeXB0ZWREYXRhIjoiUmYrQzlvK2JVYWloK3N5NFh5WUZNS1duYUtVeFN2eWJLNk9VdU9NdzdDdGtobldPcHBKYjdVQ0YxV0NQLzRZeXhWbkJVTkc2Ymd2TEpJblNYb1BraXFNPSIsIml2UGFyYW1ldGVyU3BlYyI6IjRObVVDcVUyb3JJUEFYQTciLCJtYXRlcmlhbFNldFNlcmlhbCI6MX0%3D&branch=master)

jenkinsworld branch: ![Build Status](https://codebuild.us-east-1.amazonaws.com/badges?uuid=eyJlbmNyeXB0ZWREYXRhIjoiUmYrQzlvK2JVYWloK3N5NFh5WUZNS1duYUtVeFN2eWJLNk9VdU9NdzdDdGtobldPcHBKYjdVQ0YxV0NQLzRZeXhWbkJVTkc2Ymd2TEpJblNYb1BraXFNPSIsIml2UGFyYW1ldGVyU3BlYyI6IjRObVVDcVUyb3JJUEFYQTciLCJtYXRlcmlhbFNldFNlcmlhbCI6MX0%3D&branch=jenkinsworld)

tigera branch: ![Build Status](https://codebuild.us-east-1.amazonaws.com/badges?uuid=eyJlbmNyeXB0ZWREYXRhIjoiUmYrQzlvK2JVYWloK3N5NFh5WUZNS1duYUtVeFN2eWJLNk9VdU9NdzdDdGtobldPcHBKYjdVQ0YxV0NQLzRZeXhWbkJVTkc2Ymd2TEpJblNYb1BraXFNPSIsIml2UGFyYW1ldGVyU3BlYyI6IjRObVVDcVUyb3JJUEFYQTciLCJtYXRlcmlhbFNldFNlcmlhbCI6MX0%3D&branch=tigera)

# awsugperu-workshops-templates
Hola a todos! les saluda el equipo de AWS UG Perú, para que podamos crear contenido de talleres sigan estos pasos

### Como usar los templates:

#### Necesitamos acceder a gitpod.io:

Vamos a usar un fork de este link, para mi caso seria:
`https://gitpod.io#https://github.com/awsugperu/awsugperu-template-workshops`


### Una vez dentro de gitpod:

Instalamos todas las dependencias en package.json
`npm install`

Aqui nos generara la carpeta:
"node-modules"

Luego generamos el site de hugo:
`npm run build` 

Esto nos va crear  carpetas importantes
"public/"


### Correr y previsualizar cambios en nuestro site
y Por ultimo, podemos podemos levantar el sitio con npx
`npx hugo server`

Esto nos dara un link publico o privado segun queramos en gitpod.io para previsualizar nuestros cambios

### Preparar nuestro repo e ignorar los archivos source

Ignorar los archivos fuente es importante antes de desplegar nuestro site
- revisemos el .gitignore y sino lo tenemos lo creamos
- debe contener la carpeta public, public/ node-modules entre otras que nosotros no queramos pushear a nuestro site

### Crear un bucket s3
creamos un bucket s3://us-east-1-awsugperu-template-workshops/

- habilitamos static website hosting
- Y si lo deseamos, hacemos el bucket publico, sino lo dejamos privado para hostearlo con AWS Cloudfront o AWS Amplify mas adelante.

### Desplegarlo a s3

Corremos el siguiente comando:
`npm run deploy`


#### SI desen probarlo desde local es necesario instalar  Node.js y  npm:
You can follow instructions from npm website: https://www.npmjs.com/get-npm

#### Install node packages:
`npm install`

#### Run Hugo locally:
`npm run server`
or
`npm run drafts` to see stubbed in draft pages.

`npm run build` will build your content locally and output to `./public/`

`npm run test` will test the built content for bad links

#### View Hugo locally:
Visit http://localhost:1313/ to see the site.

#### Making Edits:
As you save edits to a page, the site will live-reload to show your changes.

#### Auto Deploy:
Any commits to master will auto build and deploy in a couple of minutes. You can see the currently
deployed hash at the bottom of the menu panel.

Any commits to a branch will auto build and deploy in a couple of minutes to a custom route named with the branch name. You can see the currently
deployed hash at the bottom of the menu panel.
An example is the "jenkinsworld" branch would be deployed to https://eksworkshop.com/jenkinsworld/

note: shift-reload may be necessary in your browser to reflect the latest changes.

