<a name="readme-top"></a>


<!-- PROJECT LOGO -->
<br />
<div align="center">
  
  ![logoMovies](https://user-images.githubusercontent.com/50422794/215829613-62a22bd5-13d9-4949-8c5f-001a1c1bb7dd.png)

  
  <h3 align="center">DOCUMENTATION</h3>

  <p align="center">
    Esta documentación es parte de un proyecto educativo
    <br />
    <br />
    <a href="#">Despligue de la aplicación</a>
    <br />
    <a href="#">Brayan Duarte</a>
    ·
    <a href="https://github.com/AngelaDiaz20">Angela Diaz</a>
    ·
    <a href="#">Valentina Camacho</a>
    ·
    <a href="#">Ivan Muños</a>
    ·
    <a href="#">Jonathan Sánchez</a>
    ·
    <a href="#">Jazmin Bejarano</a>
  </p>
</div>

<!-- TABLE OF CONTENTS -->
<details>
  <summary>Table of Contents</summary>
  <ol>
    <li><a href="#Acerca-del-proyecto">Acerca del proyecto</a></li>
    <li><a href="#Construccion-de-la-aplicacion">Construcción de la aplicación</a></li>
    <li><a href="#Documentacion-tecnica">Documentación técnica</a></li>
  </ol>
</details>

<!-- ABOUT THE PROJECT -->
## Acerca del proyecto

![logoMovies](https://user-images.githubusercontent.com/50422794/215829613-62a22bd5-13d9-4949-8c5f-001a1c1bb7dd.png)

En este proyecto utilizamos algunas tecnologias basicas, utilizamos la metodologia scrum para trabajar en equipo y sacar este proyecto adelante, es un crud básico pero el verdadero reto fue trabajar en equipo para sacarlo adelante

![logoMovies](https://user-images.githubusercontent.com/50422794/215850146-7b181445-b245-4b1a-b488-820db067f12b.png)

La aplicacion nos permite tanto visualizar como agregar peliculas, con sus respectivos datos, nos permite filtrar por nombres, agregar peliculas como lo mencioné previamente, se tiene la posibilidad de editar y borrar peliculas

<p align="right">(<a href="#readme-top">back to top</a>)</p>

## Construccion de la aplicacion

Esta sección tiene una lista de los principales marcos/bibliotecas que utilicé para construir el proyecto.

* <a href="https://reactjs.org">![image](https://user-images.githubusercontent.com/50422794/211116164-7b79fadd-869a-43e3-8053-a224f080f9c2.png)</a>
* <a href="https://react-icons.github.io/react-icons/">![image](https://user-images.githubusercontent.com/50422794/211116212-ef61c9ba-9787-42f1-917d-b49a15a2d75c.png)</a>
* <a href="https://reactrouter.com/en/main">![image](https://user-images.githubusercontent.com/50422794/211116261-6cda0e56-0192-4c44-a9ec-7f7f921e1f79.png)</a>
* <a href="https://expressjs.com/es/">![image](https://user-images.githubusercontent.com/50422794/215832140-54a86230-4ede-459c-82e3-5c05ee219f10.png)</a>
* <a href="https://www.mongodb.com/">![image](https://user-images.githubusercontent.com/50422794/215832681-e822e2d6-ae97-4c63-9d0b-be6c36a2eda1.png)</a>
* <a href="https://nodejs.org/es/">![image](https://user-images.githubusercontent.com/50422794/215834151-4c767188-7bfa-406e-9967-9c07dc4f737f.png)</a>
* <a href="https://mui.com/">![image](https://user-images.githubusercontent.com/50422794/215833458-26ad6ecd-120d-4153-bd96-291f950f034c.png)</a>
* <a href="https://sweetalert2.github.io/#native_link#">![image](https://user-images.githubusercontent.com/50422794/215833564-1e1010ba-b3ce-4097-adac-6c5588a9e74a.png)</a>
* <a href="https://www.npmjs.com/package/axios">![image](https://user-images.githubusercontent.com/50422794/215833618-06eef285-0ac3-46be-ac0c-44bc311dc823.png)
</a>

<p align="right">(<a href="#readme-top">back to top</a>)</p>


## Documentacion tecnica
* <h3>Controladores</h3>

* <h3>Esquema</h3>

* <h3>Index</h3>

* <h3>Archive routes<h3/>

  <h4>Binder routes.js</h4>

  ```routes
  import { addMovie, getMovies, getMovie, editMovie, deleteMovie} from '../controller/user-controller.js';
  ```
  In this case, in the routes folder, properties called from the controller are imported to start routing each method.

  ```methods 
  router.post('/add',addMovie);
  router.get('', getMovies);
  router.get('/:id', getMovie);
  router.put('/:id', editMovie);
  router.delete('/:id', deleteMovie)
  ```

  <h3>Archive  database</h3>

  <h4>Binder db.js</h4>

  ```Connection Database
  const Connection = async (username, password) => {
  ```
  In this function it will contain 2 necessary properties that are needed to make the connection in the databases, it is the username and password.

  ```Connection Database
  const URL = `mongodb://${username}:${password}@ac-tuor9qz-shard-00-00.aha85bo.mongodb.net:27017,ac-tuor9qz-shard-00-01.aha85bo.mongodb.net:27017,ac-tuor9qz-shard-00-
  ```
    //First, the code in try is executed
    //if there were no errors,catch execution is ignored
    try {
        //The await keyword before any expression that returns a promise
        await mongoose.connect(URL, {useUnifiedTopology: true, useNewUrlParser: true});
        console.log('Database connected succesfully')
    } catch (e) {
        console.log('Error while connecting with the database', e)
    }
}

export default Connection;

  const URL = `mongodb://${Videoclub}:${movies}@movies.8wsfgdc.mongodb.net/?retryWrites=true&w=majority`;
  ```
  The constant variable URL will contain the link of the Mongo Atlas database in the cloud this link will contain two parameters of username and password.

  ```Connection Database
      try {
          await mongoose.connect(URL, {useUnifiedTopology: true, useNewUrlParser: true});
          console.log('Database connected succesfully')
  ``` 

  ```Try-catch
  The try-catch condition block is used where it allows us to detect and control what we are requesting through the connection
  ``` 

  In the try block it allows us to verify if the username and password are correct it allows us to connect to the database and show the console that it is connected

  ```Connection Database
      } catch (e) {
          console.log('Error while connecting with the database', e)
      }
  }
  ```


  ### Keywords
  There are two keywords in the connection async and await are keywords that serve to simplify the behavior of synchronous use of promises and perform some specific   behavior on a group of Promises
