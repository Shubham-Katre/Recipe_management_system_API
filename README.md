<center>
<h1>Recipe management system</h1>
<h3>Deployment EC2 Server Link</h3>
🔗 Links http://16.16.198.148:8080/getAllRecipes <br>
<br>
<br>
</center>

<a href="Java url">
    <img alt="Java" src="https://img.shields.io/badge/Java->=8-darkblue.svg" />
</a>
<a href="Maven url" >
    <img alt="Maven" src="https://img.shields.io/badge/maven-3.0.5-brightgreen.svg" />
</a>



---



## Data Model

The Recipe and Comment Class is defined inside the model packages with validation anotation, which has the following attributes:
   
   inside Recipe Class:-
   
   recipeId : Recipe ID <br>
   recipeName : Recipe Name <br>
   recipeIngredients : Recipe Ingredients <br>
   recipeInstructions : Recipe Instructions <br>
   
   @OneToMany(cascade = CascadeType.ALL)<br>
   private List<Comment> comments<br>
   
   inside Comment Class:- <br>   
   commentId : Comment Id <br>
   comment : Comment <br>
   
   @ManyToOne <br>
   private Recipe recipe <br>

---

## Data Flow

1. The user sends a request to the application through the API endpoints.
2. The API receives the request and sends it to the appropriate controller method.
3. The controller method makes a call to the method in service class.

4. The method in service class builds logic and retrieves or modifies data from the database, which is in turn given to controller class.
5. The controller method returns a response to the API.
6. The API sends the response back to the user.

---

## Functions used :-

### API Endpoints :-
</br>

* PostMapping: /addRecipe

This endpoint makes a call to method in recipeService class which is connected to database. In database we add a new recipe given through API.

* PostMapping: /addCommentOnRecipe

This endpoint makes a call to method in commentService class which is connected to database. In database we add sum new Commants to a specific Recipe through API.

* GetMapping: /getRecipeById

This endpoint returns a specifi Recipi based on id through API.

* GetMapping: /getAllRecipes

This endpoint returns all Recipi through given API Endpoint.

* PutMapping: /updateById

This endpoint makes a call to method in RecipeService class which is connected to database. In database we update a Specific Recipe based on id.


* DeleteMapping: /deleteById

This endpoint makes a call to method in RecipeService class which is connected to database. In database we delete a Specific Recipe based on id.

## Framework Used
* Spring Boot

---

## Language Used
* Java

---

 JpaRepository extended by IRecipeRepository And ICommentRepository interface.


We have used JpaRepository to implement CRUD Operations.

---

## 📝Project Summary

The recipe management system is a RESTful API built with Spring Boot and MySQL. It allows users to store, manage, and search recipes. Users can perform CRUD operations on recipes, including adding, updating, and deleting recipes. Annotation-based validation ensures data integrity. The API also supports commenting on recipes. Users can search for recipes based on various criteria, such as recipe Id. The project follows a controller-service-repository architecture, providing a modular and maintainable codebase. It offers a user-friendly and efficient solution for recipe management and sharing.
