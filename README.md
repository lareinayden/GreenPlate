# GreenPlate: A Sustainable Food Management System

## Introduction

Welcome to GreenPlate, an innovative project designed to revolutionize the way we think about and manage our food. At the heart of GreenPlate is our commitment to promoting sustainable food management. This initiative plays a pivotal role in enhancing sustainable eating and shopping habits, empowering users to make eco-friendly choices that benefit both the planet and their health. Through GreenPlate, we aim to reduce food waste and improve food resource management by integrating smart technology and user-friendly interfaces into everyday activities.

## Design & Architecture

The architecture of GreenPlate is built on robust design principles and patterns that ensure scalability, maintainability, and efficiency. Below are the UML diagrams that provide a clear visual representation of the application's design:

- ***Use Case Scenarios***:

-  ***Sequence Diagram***:

![Sequence Diagram](GreenPlate_SD.jpg)
   
  
- ***Design class Diagram***: This design diagram details the structure of our classes, their interrelationships, and how they interact within the system.
  
![Design Class Diagram for Ingredient and Recipe screens](GreenPlate_Ingredient_Recipe_DCD.jpg)

We utilize a combination of Singleton, Strategy Pattern and Observer patterns to manage object creation and ensure that the system uses resources optimally.


- **Singleton Design Pattern**:
  We implemented Singleton Pattern in the UserInfoViewModel and the InputMealViewModel as we only need 1 ViewModel for each of the UserInfoActivity and InputMeal activity. These activities used the getInstance() method to get the functions in the  viewmodels to work as desired. Each class has a static private instance variable, which holds an individual instance of the class. This variable is initially set to null. Also, each class has a private constructor that is responsible for initializing the instance. The constructor initializes the databaseReference with the Firebase in the case of both UserInfoViewModel and InputMealViewModel. The use of getInstance()  method creates access from other classes to get the instance of the ViewModel. It ensures that only one instance of each ViewModel class is created and used throughout our application, and it provides a controlled actress to the Firebase reference.
  
- **Strategy Design Pattern**:
  Our implementation of sortings align with the principles of the Strategy Pattern. We created a common interface RecipeSortingStrategy and individual classes for each sorting algorithm that implements RecipeSortingStrategy. We created the method setupSortingButtons， and called it within onCreate to initiate all buttons for sorting purposes. The  RecipeViewModel acts as the context, holding a reference to the functional interface that represents the chosen sorting behavior. This is exemplified in the methods in  RecipeViewModel. Sorting methods SortByDefault, SortByNameStrategy, SortByIngredientCount, each configuring the ViewModel to use a different sorting algorithm. This setup allows the sorting behavior to be changed dynamically, and it also ensures loose coupling in the implementation. The RecipeActivity interacts with the ViewModel by invoking these methods based on user input, extending the sorting methods of our application would not require changes to the RecipeViewModel or RecipeActivity.

- **Observer Design Pattern**:



    

## User Interface (UI)

GreenPlate features a user-friendly interface that simplifies complex processes and enhances user engagement. Here's a visual tour of the app through various screenshots, showcasing the main functionalities and the interaction flow within the app:

1. **Home Screen**:
   ![Home Screen](HomeScreen.png)
   *The home screen allows users to input their own information and logout or exit the application.*

2. **Ingredient Screen**:
   ![Inventory Management](IngredientScreen.png)
   *Users can easily add, remove, and monitor food items in their pantry.*

3. **Meal Screen**:
   ![Meal Management](MealScreen.png)
   *The meal screen allows users to input their meals and see visualization and stats of meals.*
   

5. **Recipe Screen**:
   ![Recipe Sharing](RecipeScreen.png)
   *The recipe screen allows users to share their recipes and view others' recipes, and recipe can easily convert to meals and ingredients in shopping list.*

6. **Shoppinglist Screen**:
   ![Shopping Assistant](ShoppingScreen.png)
   *The shopping list screen allows users to create a shopping list and buy items.*

## Functionality

For a deeper insight into how GreenPlate works, check out our video demonstration below. This video covers various features and showcases the real-time capabilities of the app:

[![Video Demonstration](path/to/thumbnail.jpg)](link_to_video)

## Conclusions and Reflections/Learning

Prior to this project, we had no experience using Android Studio or Firebase. It took four sprints to complete, in conjunction with integrating standard principles like Strategy patterns, SOLID/GRASP, creating UMLs, and MVVM architecture. Learning and applying these industry-standard design principles and architectural patterns not only enhanced our technical skills but also provided a deeper understanding of effective software development processes. Everyone got an oppurtunity to work on both the front-end and back-end of this system, giving us each a hollistic glimpse into the world of software development. 
## Contributors

Special thanks to all team members who contributed to the development of GreenPlate. Each individual’s effort was vital in bringing this project to fruition:

- **Yixiao Zhang**
- **Qingzhou Shen**
- **Yurun Zhu**
- **Sirui Lin**
- **Zihan Chen**
- **Trevor Goo**

Special mention to **Yixiao Zhang**, **Zihan Chen**, **Sirui Lin**, and **Trevor Goo** who were instrumental in the website's deployment.


