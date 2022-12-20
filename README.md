# Teka_Team_Pod_Team3
 E- Commerce Web Development.


Results
You should have implemented the different screens of your application, meeting the following assesment criteria:

There should be at minimum 54 pages:
Main page (Home) - Static Page with App Presentation
About Us - Static Pages
Products / Posts List - Consumes API (POST and GET)
Form Page (View / Update / Create / Delete)
Form Page (View / Create) - Optional (Update // Delete)
Example
Task 2: About Us Page
Description
Create the About Us page using Bootstrap.

The page will contain the following parts:

A short project description
Team profiles (short bio, photo and role in the project)
Tools
HTML5
Bootstrap
Walkthrough
Step 0: Create a private GitHub repository
Create a private GitHub repository that is shared among your groupmates and your instructor.

Step 1: Create the page structure
In this step, we'll create a basic HTML structure and include Bootstrap

Create a new file called about.html in your project folder.
Create a new file called styles.css and put this file inside a folder called css in your project folder.
Include your styles.css file inside the about.html page. (Hint: If you need a reminder - look up how to include css files in html files.)
Create a new Github repo and add, commit and push your files.
Step 2: Implementing your About page
Go through the different Bootstrap components and select the ones that are similar to your wireframes structure created on Task 1.

Useful Resources for this step
Bootstrap Get Started
Test Your Code!
Now is a good chance to test your page, open your about.html on your favorite browser and verify it looks and works as expected

Results
We've now set up the about.html page, created with Bootstrap! Congratulations!

Example
Stuck? Check out the provided example in the example/ folder!

Task 3: Basic Structure + Navigation - Front-End with Bootstrap
Description
Create the basic structure for the project with the navigation working:

All application views with separate HTML pages are set up.
Tools
HTML5
Bootstrap
Walkthrough

Step 1: 

Implement the home page
In this step, we'll create a basic HTML structure for the home page which includes Bootstrap

Create a new file called index.html inside your project folder.
Include your styles.css file inside the index.html page.
Add a short description, image, video or any other element you like to explain what your project does.
Add your new files to the Github repo, commit and push your changes.

Step 2: 

Implementing your Items List page
Create a new file depending on the project you are implementing:
products.html
posts.html
Include your styles.css file inside your html page.
Create a sample list with some sample data to see how your items list will look like
Useful Resources for this step
List group
Cards

Step 3:

 Implementing your Login page (Optional)
Create a new file called login.html inside your project folder.
Implement a basic login form.
Add a Login button.
Useful Resources for this step
Forms

Step 4: 

Implementing your model form page
Create a new file called item_form.html inside your project folder.
Implement a basic form with the fields needed to create a new item(post or product)
Add a Save button.
Useful Resources for this step
Forms

Step 5: 

Adding a Navigation Bar
Understand how the Navbar works.
Add a Navbar with the menu options for each page

Home
About Us
Items List
Model Form

Add a link to each menu item so it redirects to expected html page.
Useful Resources for this step
Navbar
Test Your Code!
Now is a good chance to test your page, open your index.html on your favorite browser and verify that the navigation works to all the pages.

Results
We've now create the basic html pages of your project using Bootstrap!

Example
Stuck? Check out the provided example in the example/ folder!

Task 4

Task 4: Adding Items (posts or products)
Description
For this task, we'll be

Creating a class to manage the items (products or posts)
Adding a method to the class to keep track of items in our application
Walkthrough
Step 1: The Setup
In this step, we'll re-organise our folder structure in preparation for the next few steps.

Create a js folder in your project if one does not already exist
Copy the existing js file into your js folder, and rename it to index.js
Update the <script> tag in your html file to use the new location of the js/index.js file.
Create a itemsController.js file in the js folder
Add a <script> tag pointing to the js/itemsController.js file before the <script> tag pointing to the js/index.js file.
Step 2: The ItemsController Class
In this step, we'll create a ItemsController class that will be responsible for managing the items(posts or products) in the application.

Always aim to use meaningful and long names to make your code more readable. We encourage you to replace the word Items with a more meaningful one depending on your project domain:

PostsController
ProductsController
Useful Resources for this step
ECMAScript 2015 Classes
Create a ItemsController class in js/itemsController.js
Within the constructor of the ItemsController class, initialize a this.items property on the class, Make the property equal to an empty array.
Test Your Code!
Now is a good chance to test your code, head over to js/itemsController.js and do the following

Initialize a new instance of ItemsController
console.log() the items property
Expected Result You should see an empty array logged to the browser.

Step 3: Adding A New Item Programmatically
In this step, we'll add a method to the ItemsController class that will allow us to add new items to array.

As part of this process, we're going to create a unique id for each item.

For each item to have a unique id, we will need to keep track of what id the latest task was created with, so that we can increment that id for the next item.

For example, pay attention to the two items objects below:

//E-commerce project
const product1 = {
    id: 1,
    name: ''Tayto'',
    description: 'Cheese & Onion Chips',
    img: 'https://www.irishtimes.com/polopoly_fs/1.4078148!/image/image.jpg'
    createdAt: '2020-09-20'
};

const product2 = {
    id: 2,
    name: ''Water'',
    description: 'Mineral water',
    img: 'http://www.mazalv.com/wp-content/uploads/2016/11/Bottled-Water1-979x1024-1-979x1024.png'
    createdAt: '2020-09-20'
};


//Social Media project
const post1 = {
    id: 1,
    name: 'My first post',
    text: 'This is my first post',
    img: "https://upload.wikimedia.org/wikipedia/commons/thumb/3/30/Post-greenland-uummannaq.jpg/1200px-Post-greenland-uummannaq.jpg"
    author: 'Andres Lowles',
    createdAt: '2020-09-20'
};

const post2 = {
    id: 2,
    name: 'My second post',
    text: 'This is my second post',
    img: "https://upload.wikimedia.org/wikipedia/commons/thumb/3/30/Post-greenland-uummannaq.jpg/1200px-Post-greenland-uummannaq.jpg"
    author: 'Andres Lowles',
    createdAt: '2020-09-20'
};
Notice how each item has a unique id? We will be using this id in future steps to keep track of the different items.

Useful Resources for this step
Array.prototype.push()
In the ItemsController's constructor, accept a currentId parameter, with a default value of 0.

Assign the currentId to a new property on the class, this.currentId.

Create a method on the class, addItem. This method should accept all the nessecary information from the form to create an item as parameters.

Product
name
description
img
createdAt
Post
name
text
img
author
createdAt
Within the addItem method, increment the this.currentId

push a new item into the this.items array, with the correct properties of the item, using the values passed in as parameters as well as the new this.currentId Note Make sure to include the id

Test Your Code!
Now is a good chance to test your code, head over to js/itemsController.js and do the following

Initialize a new instance of ItemsController
Use the addItem method to add a new item
console.log() the items property
Expected Result You should see an array containing the added item logged to the browser.

Results
We've now set up the ItemsController class, create an addItem and you are able to see the output on the browser console!

Test out your code by hardcoding items and checking the ItemsController instance's items array for the tasks.

Example
Stuck? Check out the provided example in the example/ folder!

Task  5

Task 5: Displaying Items List(posts or products)
Description
For this task, we'll be creating the feature to display the objects list of the selected project:

Products List
Posts List
Walkthrough
Step 1: Define the item card layout
In this step, we'll create the item representation using the card component

Read the documentation and understand how to use the card components
Define the HTML structure of the item card representation.
Add a div element with id list-items to add your list items dynamically with JavaScript.
Add 3 different sample item cards inside your div element.
Expected Result You should see the items list displayed correctly

Step 2: Adding your items cards programmatically
In this step, we'll create a function addItemCard(item) that will be responsible for adding new items to the list.

Useful Resources for this step
Document.getElementById()
Define a function called addItemCard(item) inside your in js/items.js
Write the code so your function can create the same HTML structure of your item card representation replacing the item's information.
Test Your Code!
Now is a good chance to test your code, head over to you HTML page and open it on the browser:

Open the console from the Developer Tools.
Excecute the addItemCard(item) function from the console
Expected Result You should see a new item card added to the DOM.

Step 3: Store and read Items from the LocalStorage
In this step, we'll connect the ItemsController class and items.js with the local storage to persist your items data.

Modify the items.js adding a new function to save sample items data in the local storage. Use the following JSON structure as reference(make sure you save the data as a String).
        const sampleItems = [{'name':'juice',
        'img':'https://www.gs1india.org/media/Juice_pack.jpg',
        'description':'Orange and Apple juice fresh and delicious'},
        {'name':'Tayto',
        'img':'https://www.irishtimes.com/polopoly_fs/1.4078148!/image/image.jpg',
        'description':'Cheese & Onion Chips'}];
        localStorage.setItem("items", JSON.stringify(sampleItems));
Modify the ItemsController so it loads the data from the storage implementing a new function items.js
    loadItemsFromLocalStorage() {
        const storageItems = localStorage.getItem("items")
        if (storageItems) {
            const items = JSON.parse(storageItems)
            //TODO load the items into the local items structure (this.items)           
        }
    }
Implement a new function in the items.js that loads the items from the ItemsController using the function you already implemented addItemCard(item).

Modify the items.js so it calls the loadItemsFromLocalStorage() and then iterate the ItemsController.items list to load the items into your items.html page using the function implemented from addItemCard(item)

Results
We've now implemented a basic version of your application that persist the data on the local storage.

Test out your code by calling the funciton that loads the data from the local storage and verify the items are displayed correctly. You can also use the developer tools and navigate to the Application tab to verify that the items are saved in the local storage.

Example
Stuck? Check out the provided example in the example/ folder!

# Task 6: Creating new items using the form

## Description

For this task, we'll be creating new Items using a form and validating the input data.

## Walkthrough

### Step 1: The Setup

1. Create a new file called `item-form.js` inside the `js` folder.
2. Add a `<script>` tag in your `item-form.html` file to include the `js/item-form.js` file.

### Step 2: Adding Items With The Form

In this step, we will use the `ItemsController` class to keep track of items we add with the **New Item** form.

> #### Useful Resources for this step
> - [Document.querySelector()](https://developer.mozilla.org/en-US/docs/Web/API/Document/querySelector)
> - [EventTarget.addEventListener()](https://developer.mozilla.org/en-US/docs/Web/API/EventTarget/addEventListener)
> - [Event Reference](https://developer.mozilla.org/en-US/docs/Web/Events)

1. Make sure a new `ItemsController` is initialized near the top of the `item-form.js` file.
2. In `item-form.js`, add an event listener to the **New Item** form, listening to the `submit` event. If there is already an event listener used for validation, use that one.
3. When the `submit` event fires, if validation of the form is successful, use the values of each `input` in the form to call the `itemsController`'s `addItem` method.
    - **Note**: Make sure to prevent the default action of the form!
4. Update the items list in local storage so the data is also reflected on the `items.html`.
4. Clear the values from each form input, ready for the next submission.

## Results

We've now set up the `ItemsController` class, used `addItem` and hooked it up to our **New Item** form!

Test out your code by adding some items using the **New Item** form, and checking the `ItemsController` instance's `items` array for the items.

## Example

Stuck? Check out the provided example in the [example/](example/) folder!

# Task 7: Implementing the Persistance Layer with MySQL

## Description

For this task, we'll be implementing the database of your application using MySQL.

## Walkthrough

### Step 1: Using MySQL Workbench to implement the database structure

> #### Useful Resources for this step
>
> - [MySQL Workbench Tutorial: complete guide to the RDBMS tool](https://www.educative.io/blog/mysql-workbench-tutorial)

In this step, we'll create a EER Model to represent the application data layer.

1. Create a new MySQL Workbench project
2. Create a new EER Model.
3. Create a new table that will represent your model(posts or products) and add the required columns:
   Eg Item:

   - `id`
   - `name`
   - `description`
   - `imageUrl`

   <img src="./img/mysql-workbench.png">

4. Generate your SQL code to create your database schema. Click on File / Export / Forward Engineer SQL CREATE Script..

### Step 2: Connecting and Creating the database to your local instance of MYSQL

In this step, we'll create the database Schema on your local instance of MySQL database engine.

1.  If you haven't done it download and install the [MySQL installer](https://dev.mysql.com/downloads/installer/)
2.  Copy the SQL sentences generated on step 1.
3.  Setup the database connection to connect to your local instance of MySQL.
4.  Open the local instance connection and paste the SQL sentences and run it.

    ```sql
    -- MySQL Script generated by MySQL Workbench
    -- Sun Jan 10 14:14:47 2021
    -- Model: New Model    Version: 1.0
    -- MySQL Workbench Forward Engineering

    SET @OLD_UNIQUE_CHECKS=@@UNIQUE_CHECKS, UNIQUE_CHECKS=0;
    SET @OLD_FOREIGN_KEY_CHECKS=@@FOREIGN_KEY_CHECKS, FOREIGN_KEY_CHECKS=0;
    SET @OLD_SQL_MODE=@@SQL_MODE, SQL_MODE='ONLY_FULL_GROUP_BY,STRICT_TRANS_TABLES,NO_ZERO_IN_DATE,NO_ZERO_DATE,ERROR_FOR_DIVISION_BY_ZERO,NO_ENGINE_SUBSTITUTION';

    -- -----------------------------------------------------
    -- Schema itemsdb
    -- -----------------------------------------------------

    -- -----------------------------------------------------
    -- Schema itemsdb
    -- -----------------------------------------------------
    CREATE SCHEMA IF NOT EXISTS `itemsdb` DEFAULT CHARACTER SET utf8 ;
    USE `itemsdb` ;

    -- -----------------------------------------------------
    -- Table `mydb`.`Item`
    -- -----------------------------------------------------
    CREATE TABLE IF NOT EXISTS `itemsdb`.`Item` (
    `id` INT NOT NULL,
    `name` VARCHAR(45) NULL,
    `description` VARCHAR(200) NULL,
    `imageUrl` VARCHAR(200) NULL,
    PRIMARY KEY (`id`))
    ENGINE = InnoDB;


    SET SQL_MODE=@OLD_SQL_MODE;
    SET FOREIGN_KEY_CHECKS=@OLD_FOREIGN_KEY_CHECKS;
    SET UNIQUE_CHECKS=@OLD_UNIQUE_CHECKS;

    ```

5.  Create a new database user running the following commands at the mysql prompt:

    ```bash
    mysql> create user 'admin'@'%' identified by 'passw0rd'; -- Creates the user
    mysql> grant all on itemsdb.* to 'admin'@'%'; -- Gives all privileges to the new user on the newly created database
    ```

    > #### Test Your Code!
    >
    > Now is a good chance to test your code, head over to MySQL Workbench schemas tab, click the refresh button and verify that your table is created as expected.
    >
    > 1. Right click on the table you created and select the option: `Select Rows - Limit 1000 `to interact with the table.
    > 2. Create a new entry manually using the tool to add data in result grid view.
    > 3. Insert a new record manually into the database:
    >    ```sql
    >    INSERT INTO `itemsdb`.`Item` (`id`, `name`, `description`, `imageUrl`) VALUES ('1', 'Chips', 'Sour Cream and Onion', 'https://images-na.ssl-images-amazon.com/images/I/81EUE1oZURL._SL1500_.jpg');
    >    ```

    > ```
    > **Expected Result**
    > You should see the schema created with the tables defined on the EER Diagram
    > Take a screenshot of your schema and the EER Diagram. Name the file SchemaEER.jpg and create a folder for      
    > screenshots of the project. 
    > ```
# Task 8: Database Connection with Spring Data JPA

## Description

For this task, we'll implement the backend of our web application using Spring Boot with Java.

## Walkthrough

### Step 1: Creating the base project

> #### Useful Resources for this step
>
> - [Spring Initializr](https://start.spring.io/)

In this step, we'll generate a Spring Boot project using the [spring initializr](https://start.spring.io/)

1. Go to the [spring initializr](https://start.spring.io/) and generate a new project with the following configuration:
   - Project: Gradle Project
   - Language: Java
   - Dependencies: Spring Web and Spring Data JPA (SQL)
   - Project Metadata: use meaningful names that describe your project, use Jar for packaging and select the Java version installed on your computer.
     <img src="./img/project-setup-spring-boot.png">
2. Click on Generate.
3. Create a new repo on Github for the backend and upload the generated code.

> #### Test Your Code!
>
> Now is a good chance to test your code, open your project on the Java IDE and run the main class within your Application class.
>
> **Expected Result**
> You should see the server is started correctly and no error is shown on the console.

### Step 2: Database Connection with Spring Data JPA

> #### Useful Resources for this step
>
> - [Spring Data Reference Documentation](https://docs.spring.io/spring-data/jpa/docs/current/reference/html/#jpa.introduction)
> - [Accesing data with MySQL](https://spring.io/guides/gs/accessing-data-mysql/)

In this step, we'll connect the Spring Boot project with the MySQL database created on [task 7](https://github.com/generation-org/jfsjd-final-project/tree/main/task-7).

1. Make sure you create the database user and grant access to your database:

   ```bash
       mysql> create user 'admin'@'%' identified by 'passw0rd'; -- Creates the user
       mysql> grant all on itemsdb.* to 'admin'@'%'; -- Gives all privileges to the new user on the newly created database
   ```

2. Add the following properties to the src/main/resources/application.properties:

   ```yaml
   spring.datasource.driver-class-name=com.mysql.cj.jdbc.Driver
   spring.jpa.hibernate.naming.physical-strategy=org.hibernate.boot.model.naming.PhysicalNamingStrategyStandardImpl
   spring.jpa.hibernate.ddl-auto=none
   spring.datasource.url=jdbc:mysql://${MYSQL_HOST:localhost}:3306/itemsdb
   spring.datasource.username=admin
   spring.datasource.password=passw0rd
   ```

3. Add the following dependency to your build.gradle

   ```gradle
       runtimeOnly 'mysql:mysql-connector-java'
   ```

#### Test Your Code!

> Now is a good chance to test your code, run your Application main method to start the server.
>
> **Expected Result**
> Your application should start and connect with your database, no error should be displayed on the console.

### Step 3: Interacting with the Database form your Spring Boot Project

1. Create new package called `repository.entity` and define the @Entity Model class:

   ```java
       package org.generation.ItemsAPI.repository.entity;

       import javax.persistence.Entity;
       import javax.persistence.GeneratedValue;
       import javax.persistence.GenerationType;
       import javax.persistence.Id;

       @Entity
       public class Item
       {
           @Id
           @GeneratedValue(strategy= GenerationType.AUTO)
           private Integer id;

           private String name;

           private String description;

           private String imageUrl;

           public Integer getId()
           {
               return id;
           }

           public void setId( Integer id )
           {
               this.id = id;
           }

           public String getName()
           {
               return name;
           }

           public void setName( String name )
           {
               this.name = name;
           }

           public String getDescription()
           {
               return description;
           }

           public void setDescription( String description )
           {
               this.description = description;
           }

           public String getImageUrl()
           {
               return imageUrl;
           }

           public void setImageUrl( String imageUrl )
           {
               this.imageUrl = imageUrl;
           }
       }
   ```

2. Create your repository interface to access the `Item` entity data under the repository package:

   For example:

   ```java
    package org.generation.ItemsAPI.repository;

    import org.generation.ItemsAPI.repository.entity.Item;
    import org.springframework.data.repository.CrudRepository;

    // This will be AUTO IMPLEMENTED by Spring into a Bean called itemRepository
    // CRUD refers Create, Read, Update, Delete
    public interface ItemRepository extends CrudRepository<Item, Integer>
    {
    }
   ```

3. Create a REST Controller to test your code inside a new package `controller` called ItemController:

   ```java
   @RestController
   @RequestMapping("/item")
   public class ItemController{

       final ItemRepository itemRepository;


       public ItemController(@Autowired ItemRepository itemRepository )
       {
           this.itemRepository = itemRepository;
       }

       @GetMapping
       public Iterable<Item> getItems(){
           return itemRepository.findAll();
       }
   }

   ```

> #### Test Your Code!
>
> Now is a good chance to test your code, start your application and open `http://localhost:8080/item` on your browser.
>
> **Expected Result**
> You should see the list of items stored on your MySQL database:
>
> ```json
> [
>   {
>     "id": 1,
>     "name": "Chips",
>     "description": "Sour Cream and Onion",
>     "imageUrl": "https://images-na.ssl-images-amazon.com/images/I/81EUE1oZURL._SL1500_.jpg"
>   }
> ]
> ```

## Example

Stuck? Check out the provided example in the [example/](example/) folder

# Task 9: Implementing the REST API

## Description

In this task, we'll implement our REST API so you can perform the CRUD(Create, Read, Update and Delete) operations
over your data model using the HTTP protocol.

## Walkthrough

### Step 1: Implementing the ItemService

> #### Useful Resources for this step
>
> - [Spring Beans and Dependency Injection](https://docs.spring.io/spring-boot/docs/2.0.x/reference/html/using-boot-spring-beans-and-dependency-injection.html)

In this step, we'll define our Service interface and create an implentation that handles the interaction with MySQL Database. An interface is a structure or syntax that allows software developers to define a component's behavior without worrying about the implementation.

1. Create a new package in your Spring Boot project called `service`
2. Create the `ItemService` interface with the functions needed to implement the Items CRUD:

   ```java
        public interface ItemService
        {

            Item save( Item item );

            boolean delete( int itemId );

            List<Item> all();

            Item findById( int itemId );

        }
   ```

3. Create an implementation of the `ItemService` called `ItemServiceMySQL` and inject the `ItemRepository`.

   ```java
           public class ItemServiceMySQL implements ItemService
           {
               private final ItemRepository itemRepository;

               public ItemServiceMySQL(@Autowired ItemRepository itemRepository )
               {
                   this.itemRepository = itemRepository;
               }

               @Override
               public Item save( Item item )
               {
                   //TODO implement this method
                   return null;
               }

               @Override
               public void delete( int itemId )
               {
                   //TODO implement this method
               }

               @Override
               public List<Item> all()
               {
                   //TODO implement this method
                   return null;
               }

               @Override
               public Item findById( int itemId )
               {
                   //TODO implement this method
                   return null;
               }
           }

   ```

4. Implement the methods so you persist and retrieve your data using the `ItemRepository`.
5. Annotate the `ItemServiceMySQL` with `@Service` so it can be injected into the `ItemController`

   > #### Test Your Code!
   >
   > Now is a good chance to test your code, follow the steps below:
   >
   > 1. Inject the `ItemService` inside the `ItemController`
   > 2. Add a breakpoint inside the `getItems` function on the line 24 of the `ItemController`.
   > 3. Run your project on Debug Mode and open `http://localhost:8080/item` on your browser.
   >
   > **Expected Result**
   > You should see that the `ItemService` variable is instantiated with the `ItemServiceMySQL`

### Step 2: Connecting your ItemController with the ItemService

Now that we have defined the `ItemService` behavior and created an implementation `ItemServiceMySQL` - we can use this service to implement our REST API methods to fulfill the CRUD operations.

1. Inject `ItemService` inside the `ItemController`.
2. Modify the endpoint to retrieve the list of items to be `/item/all` and change the funciton implementation so it calls the `itemService.all()`
3. Create a new package inside the `controller` called `dto` for the Data Transfer Objects, these are Java classes used to map the JSON data structure sent and received by the REST controller.
4. Add a new class called `ItemDto` inside the `dto` package.

   ```java
   public class ItemDto
   {

       private String name;

       private String description;

       private String imageUrl;

       public ItemDto( String name, String description, String imageUrl )
       {
           this.name = name;
           this.description = description;
           this.imageUrl = imageUrl;
       }

       public String getName()
       {
           return name;
       }

       public void setName( String name )
       {
           this.name = name;
       }

       public String getDescription()
       {
           return description;
       }

       public void setDescription( String description )
       {
           this.description = description;
       }

       public String getImageUrl()
       {
           return imageUrl;
       }

       public void setImageUrl( String imageUrl )
       {
           this.imageUrl = imageUrl;
       }
   }
   ```

5. Implement a new function inside the `ItemController` to create a new Item using the `@PostMapping` annotation and the `@RequestBody` annotation to receive an `ItemDto` as parameter on the POST request.

6. Call the `itemService.save` to persist the item received in the request.

```java
    @PostMapping
    public Item save( @RequestBody ItemDto itemDto )
    {
        return itemService.save( new Item( itemDto ) );
    }
```

7. Implement a new function inside the `ItemController` to retrive a specifc item using the item Id
   ```java
       @GetMapping("/{id}")
       public Item findItemById( @PathVariable Integer id ){
           return itemService.findById( id );
       }
   ```
8. Implement the remaining CRUD methods using the `@PutMapping` to update an item and `@DeleteMapping` to delete an item.

   ```java
       @PutMapping( "/{id}" )
       public Item update( @RequestBody ItemDto itemDto, @PathVariable Integer id )
       {
           Item item = itemService.findById( id );
           item.setName( itemDto.getName() );
           item.setDescription( itemDto.getDescription() );
           item.setImageUrl( itemDto.getImageUrl() );
           return itemService.save( item );
       }

       @DeleteMapping( "/{id}" )
       public void delete( @PathVariable Integer id )
       {
           itemService.delete( id );
       }
   ```

## Results

Start your server and test your Item's endpoint using any HTTP client like [Postman](https://www.postman.com/) - [Example of how to send requests in postman](https://learning.postman.com/docs/sending-requests/requests/)

## Example

Stuck? Check out the provided example in the [example/](example/) folder

# Task 10: Connecting the Frontend with the Backend

## Description

Now that we have implemented the frontend and the backend of the final project, its time to connect these two layers.

## Walkthrough

### Step 1: Using fetch to POST the new Item

> #### Useful Resources for this step
>
> - [Using Fetch](https://developer.mozilla.org/en-US/docs/Web/API/Fetch_API/Using_Fetch)

In this step, we'll use the Fetch API to consume the save item endpoint.

1. In `js/ItemsController.js`, implement a new function called `save` that will POST the new item's data using the `fetch` function:

   ```javascript
       save({name, description, imageUrl}){
               const data = { name,  description, imageUrl };

               fetch('http://localhost:8080/item', {
               method: 'POST', // or 'PUT'
               headers: {
                   'Content-Type': 'application/json',
               },
               body: JSON.stringify(data),
               })
               .then(response => response.json())
               .then(data => {
               console.log('Success:', data);
               })
               .catch((error) => {
               console.error('Error:', error);
               });
           }
   ```

2. Modify the `save` method of the `ItemsController.java` to avoid the [CORS mechanism](https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS)

   ```java
       @CrossOrigin
       @PostMapping
       public Item save( @RequestBody ItemDto itemDto )
       {
           return itemService.save( new Item( itemDto ) );
       }
   ```

3. Add a call to the `uploadItem` function inside the scope of `addItem` function (you could call it after the items are stored on the `localStorage`).

> #### Test Your Code!
>
> Now is a good chance to test your code, start your Server API and verify if the data is stored correctly on the MySQL database.
>
> 1. Open `item-form.html` in the browser and create a new item using the form.
>
> **Expected Result**
> You should see the success message on the console log.

### Step 2: Consuming REST API

> #### Useful Resources for this step
>
> - [How to use fetch api for crud operations](https://dev.to/duhbhavesh/how-to-use-fetch-api-for-crud-operations-57a0)

Now that we have made the implementation of the `save` function to consume the `POST /item` endpoint we'll implement the missing functions:

- update
- findByItemId
- delete

1. Implement the `update` function.
2. Change your code so the save button calls the `update` function.
3. Test the `update` function(make sure you send an existing item id)
4. Implement the `findItemById`
5. Change your code so the save button calls the `findItemById` function.
6. Populate the item's data into the corresponding form fields.
7. Test the `findItemById` function (make sure you send an existing item id)
8. Implement the `delete` function.
9. Change your code so the save button calls the `delete` function.
10. Test the `delete` function (make sure you send an existing item id)

## Results

Now you have all the methods to consume the REST API CRUD operations. Congratulations!

## Example

Stuck? Check out the provided example in the [example/](example/) folder

# Java Full Stack Junior Development (JFSJD) - Final Project


**General Objectives**

Implement a fully working web application with the following layers:
* Persistence: MySQL Database.
* Backend: REST API with Java and Spring Boot. 
* Frontend: JavaScript + CSS + HTML.

**Details**

* You will work in **groups of 2-3 people** as assigned by the instructor. 
* This project has **11 tasks** divided into **3 Sprints**.
* Each Sprint will have a **demo** and a **retrospective** at the end following the Scrum methodology.
* At the end of the project, you and your group will do a **final project presentation** to the entire class and potentially to a group of employers.


# eternally-charmed
