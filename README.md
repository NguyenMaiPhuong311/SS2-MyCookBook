# [My CookBook](https://mycookbook-project.herokuapp.com/)   

<img src="https://i.ibb.co/3kJTfZG/home.jpg" alt="mockup-homepage" target="_blank" rel="noopener" width="800">

"My CookBook" - Practical Python and Data-Centric Development Milestone Project.

The main purpose of this full-stack MongoDB-based Flask project is to create a database of recipes that allows users to create, read, update and delete (CRUD) recipes.
"My CookBook" gives an access to all the recipes in the database for non-registered users. At the same time, it gives the opportunity to create an account and benifit from having convenient access to all features of the website.
Registered users can add new recipes, edit and delete their own ones, as well as edit their username and password or delete account.  
[My CookBook](https://mycookbook-project.herokuapp.com/) is a simple way to view, create and store your recipes!   
Sign in, get inspired, contribute, cook and enjoy!

---

## Table of Contents
1. [UX](#ux)
    - [User Stories](#user-stories)
    - [Design](#design)
    - [Wireframes](#wireframes)

2. [Features](#features)
    - [Existing Features](#existing-features)

3. [Technologies Used](#technologies-used)

---

## UX
My main goal in UX was to built a website minimalistic in design, simple to use; where users can create their own recipes, view all the recipes created by others,
edit and delete their recipes. The target audience for this app is anyone who has passion for cooking, wants to discover new recipes or needs to store their own recipes online.  
Creating modern, sleek and user-friendly interface with easy access to all information is the key to giving users feel of reliability, security and positiveness. 
With this in mind, I developed this app in a way that everyone can view all the recipes on the website, while only authors can make changes to their recipes.   
As well as that, structuring the website in well-organised readable way with easy navigation was another goal for this project.
### User Stories
**As a user, I want/expect:**
- to view all the recipes without having to register
- to view all recipe details (including cuisine, meal and diet types, cooking time, servings, list of ingredients and directions)
- to see how many recipes are on the website
- to create my own account
- to add new recipes 
- to edit my recipes 
- to view a list of my recipes on a separate page and see how many recipes I've created
- to delete my recipes
- to log out any time and have the session terminated
- to change my current username
- to change my current password
- to delete my account and all recipes I've created
- to use the website from any device (laptop, tablet, mobile)
### Design
The goal in design was to create a website that is overall user friendly, has a modern feel with emphasis on providing information about recipes in a readable and eye-catching way. Therefore, following design choices were made:
#### Framework
[Materialize](https://materializecss.com/), front-end framework based on Material Design was chosen for this project for its modern interface and ease of use. It was used for creating features such as navbar, cards, forms, modal, as well as for its grid.  
[JQuery](https://jquery.com/) was used for initializing some Materialize elements listed above, as well as for custom functions, simple DOM manipulation.
#### Colour Scheme
One of the main goals was to focus user's attention on the recipe cards and recipes' images. Therefore, I decided to have a lot of whitespaces and mostly white background accross the website, giving preferences to calm white and grey colours (e.g. for navbar, footer, forms). Bright colours are only used for buttons, icons and some headings to catch user's atention.    
The idea of using different shades of the same colour is implemented accross the website. The primary colour used for main buttons and headings is coral as it seems to create a nice contrast with grey and white backgrounds. The secondary colour used for icons, dividers and some other buttons is yellow.   
##### Main colour palette
 - ![#ff4242](https://placehold.it/15/ff4242/ff4242) `#ff4242` - **coral**
 - ![#fab700](https://placehold.it/15/fab700/fab700) `#fab700` - **yellow**
 - ![#c89200](https://placehold.it/15/c89200/c89200) `#c89200` - **darkyellow**
 - ![#2e2e2e](https://placehold.it/15/2e2e2e/2e2e2e) `#2e2e2e` - **lightblack**
 - ![#f5f5f5f3](https://placehold.it/15/f5f5f5f3/f5f5f5f3) `#f5f5f5f3` - **darkwhite**
 - ![#ffffff](https://placehold.it/15/ffffff/ffffff) `#ffffff` - **white** 
#### Typography
There are two fonts used across the project: [Open Sans](https://fonts.google.com/specimen/Open+Sans)-the main primary font and [Ubuntu](https://fonts.google.com/specimen/Ubuntu) - the secondary font, used for some headings and buttons.

#### Icons
Icons are used widely, as they are good attention grabbers. They help users to find and scan content. Another advantage of using them is to help to break language barriers. They create more user-friendly experience for people with non-native English.  
I used [FontAwesome](https://fontawesome.com/) as the main icon library across the project (e.g. for navbar, footer, forms, recipe details page). However,  [Materialize icons](https://materializecss.com/icons.html) were used as well in some cases.
#### Further styling decisions
- The recipe cards were styled with rounded corners (`border-radius: 25px`), which was considered sleek and modern-looking. This styling concept is repeated across the website in images, buttons, forms.
- Different shadows were used accross the website to create balance between volume and readability(e.g. for headings).

### Wireframes
[Balsamiq Wireframes](https://balsamiq.com/) was used to create all wireframes for the project.

Initial wireframes with some comments for both desktop and mobile devices can be found [here](https://github.com/irinatu17/MyCookBook/tree/master/mycookbook/wireframes).

---

## Features
### Existing Features
#### Navbar   
- <img src="https://i.imgur.com/V4XgEvj.gif" alt="navbar-logged-in" target="_blank" rel="noopener">
The navbar is fixed at the top of the page, this allows a user to easily navigate throughout the website. The logo is located in the top right corner on a desktop and in the center on smaller devices. It redirects the user to the home page when clicked.
On the smaller resolutions (tablet, mobile) the navbar is collapsed into a burger icon. A slide out menu opens when the burger icon is clicked.     

For **non-logged in** users or **guests** navbar contains the following links:
<img src="https://i.ibb.co/kXy0gH1/navbar-not-logged-in.jpg" alt="navbar-not-logged-in" target="_blank" rel="noopener">
- Home
- Browse Recipes
- Login
- Register    
   
For **logged-in** users navbar contains the following links:
<img src="https://i.ibb.co/7KYHxg4/navbar-logged-in.jpg" alt="navbar-logged-in" target="_blank" rel="noopener">
- Home
- Browse Recipes
- Account (it is a dropdown on a desktop)
    - My Recipes
    - Add Recipe
    - Settings
- Logout
#### Home page and Featured Recipes   
The home page contains a button that redirects a user to the "All Recipes" page. It also displays 4 random images from 
the database using the `$sample` function of MongoDB. 
#### Browse All Recipes   
 - <img src="https://i.ibb.co/fvR791x/all-recipes.jpg" alt="all-recipes" target="_blank" rel="noopener">
The all recipes page displays recipe cards sorted from the oldest to the most recently added. As well as that, there is a total number of recipes displayed in parentheses after the heading.
All recipe cards are clickable and redirect a user to the individual recipe page with detailed information.
The pagination at the bottom of the page allows to display 8 recipes per page.
#### Single Recipe details   
- <img src="https://i.ibb.co/tBvfdTM/recipe-card.jpg" alt="recipe-card" target="_blank" rel="noopener">

The single recipe details page renders when user clicks on the recipe card. It displays information about the selected recipe:
recipe name, description, cuisine type, meal type, diet type, number of servings, cooking time, author, ingredients, directions and recipe image (or recipe placeholder if no image was added by user).
If the user is an author of the recipe, there are buttons "Edit" and "Delete", that redirect to the edit and delete recipe pages, respectively.
#### Register   
- <img src="https://i.imgur.com/teX28yi.gif" alt="register" target="_blank" rel="noopener">
The register page allows a user to create a new account. The user is asked to fill the fields "username", "password" and "confirm password".
When adding a username, the code compares it against existing usernames to ensure that it is unique. A username must be 3-15 characters long. The same requirement applies to the password field.
The "confirm password" field must match the original password. All passwords are hashed for security purposes. If user's input does not meet requirements, flash messages will inform a user about the error.
When the form is submitted successfully, a user is redirected to the home page and informed that account was created.
There is also a link to the login page for existing users at the bottom of the form.
#### Login   
- <img src="https://i.ibb.co/8mxdPPk/login.jpg" alt="login" target="_blank" rel="noopener">
The login page features the form with "username" and "password" fields, allowing registered users to log into their account.
If the entered username and hashed password match the ones in the database, a user is redirected to the home page and informed that the  log in was successful. Otherwise, flash messages will be displayed about incorrect user's input.
There is also a link to the register page for new users at the bottom of the form.
#### Logout 
Hitting "logout" button by the logged in users ends their session and redirects to the homepage.
#### My recipes   
- <img src="https://i.ibb.co/kyQMbCR/my-recipes.jpg" alt="my-recipes" target="_blank" rel="noopener">
My recipes page allows registered users to view all their recipes. It also displays the total number of all the user's recipes. Below that there is a button "Add new recipe" taht redirects a user to the "Add recipe" page.
Pagination is in place displaying 8 recipes per page. If user has not created any recipes yet, there's a message that asks a user to create one.
#### Add Recipe   
- <img src="https://i.ibb.co/8PDVxSV/add-recipe.jpg" alt="add-recipe" target="_blank" rel="noopener">
The registered and logged in users can add new recipes through the form. There are some validations in place - all the fields except "Cuisine type", "Diet type" and "Recipe Image" are required. For the "recipe name" and "recipe description" fields, limit of characters is set.
If user does not provide a URL to the recipe image, the recipe placeholder will be assigned for that recipe. There is also a Tooltip-instruction saying that a user can upload the image to a free image hosting website(e.g. ImgBB).   
After the succsessful addition, a user is redirected to the newly created recipe details page. There is also a button "Cancel" that simply redirects a user to the home page (in order to avoid to hit "back" button in a browser).
#### Edit Recipe
The edit recipe page allows the logged in user to update information about the recipe. The "Edit" button will appear only for the author of the recipe.   
As well as that, the defensive design (against brute-forcing) in place allows only author of the recipe to make changes. 
The form is pre-populated with the original recipe's details. After clicking "Edit recipe" button, the recipe is updated in the database and a user is redirected to the details page of the updated recipe.   
There is also a button "Cancel" that simply redirects a user to the home page (in order to avoid to hit "back" button in a browser)
#### Delete Recipe
The delete recipe function allows only author of the recipe to delete it. After a user clicks the "delete" button in a Single Recipe Details page, the modal will be opened. It asks a user to confirm if the recipe is to be deleted. 
If so, upon clicking "delete" button the recipe will be removed from the database as well as from the "user_recipes" field of the recipe's author in "users" collection. There is also a button "cancel" that closes the modal when it's clicked.
#### Account Settings page   
- <img src="https://i.ibb.co/H2G09hg/settings.jpg" alt="settings" target="_blank" rel="noopener">
The Account Settings page contains username, randomly generated user avatar with a greeting and 3 buttons: "Change username", "Change password" and "Delete account". These buttons redirect a user to the corresponding page.
#### Change username
The Change Username form displayed allows the registered user to change their username. It checks if the new entered username is present in the database. The current username is displayed above the new username field. There is also a question mark that displays requirements for the field when hovered over. After succsessfull submission, it redirects a user to the login page asking to log in with a new username. There is also a button "Cancel" that simply redirects a user to the account settings page.
#### Change password
A user can change their current password by filling the form that contains following fields: "Current password", "New password", "Confirm New password".
Both new password have to match and be 3-15 characters long. There is a question mark that displays requirements for the field when hovered over. If the form is successfully submitted, a user is redirected to the account settings page with a flash message about successfully changed password. There is also a button "Cancel" that simply redirects a user to the account settings page.
#### Delete account   
- <img src="https://i.imgur.com/U72EQ0Y.gif" alt="delete-account" target="_blank" rel="noopener">
Once the "delete account" button on the account settings page is clicked, the modal shows up asking to confirm if the user certainly wants to delete their account. To verify this, user has to provide the password. After clicking the "delete account" button, the account is removed from the "users" collection. All the recipes created by this user are removed from the "recipes" collection as well. There is also a button "Cancel" that closes the modal.
#### Footer
The footer features links to the social media which open in a new tab (by using `'target="_blank"`). 
#### 404 and 500 error pages   
- <img src="https://i.ibb.co/16LRVcp/error-404.jpg" alt="error-404" target="_blank" rel="noopener">
Customized 404 and 500 pages contain short information about the error and a button "Back Home". As well as that, they display navbar that allows users to come back easily to any page if they got lost.

---

## Technologies Used

- [GitPod](https://www.gitpod.io/) - an online IDE for developing this project.
- [Git](https://git-scm.com/) - for version control.
- [GitHub](https://git-scm.com/) - for remotely storing project's code.
- [PIP](https://pip.pypa.io/en/stable/installing/) - for installation of necessary tools.
- [GIMP2](https://www.gimp.org/) - for editing, compressing and resizing images.
- [Am I Responsive](http://ami.responsivedesign.is/) - for creation of the images in the readme file and checking responsiveness.
- [Ezgit](https://ezgif.com/) - to create gifs for README
- [Imgur](https://imgur.com/) - to host gifs
- [ImgBB](https://imgbb.com/) - to host images used in README
### Front-End
- [HTML](https://developer.mozilla.org/en-US/docs/Web/Guide/HTML/HTML5) - to build the foundation of the project.
- [CSS](https://developer.mozilla.org/en-US/docs/Archive/CSS3) - to create custom styles.
### Back-End
- [Python 3.8.2](https://www.python.org/) -  back-end programming language used in this project.
- [Flask 1.1.2](https://flask.palletsprojects.com/en/1.1.x/) - microframework for building and rendering pages.
- [MongoDB Atlas](https://www.mongodb.com/) - NoSQL database for storing back-end data.
- [PyMongo](https://api.mongodb.com/python/current/) - for Python to get access the MongoDB database.
- [WTForms 2.2.1](https://pypi.org/project/WTForms/) - for creating forms with validation.
- [Werkzeug 0.16.1](https://werkzeug.palletsprojects.com/en/0.16.x/) - to generate and verify password hashing.
- [Jinja 2.10.1](https://jinja.palletsprojects.com/en/2.10.x/) - templating language for Python, to display back-end data in HTML.
- [Heroku](https://heroku.com/) - to host the project.
### Libraries
- [Materialize 1.0.0](https://materializecss.com/) - main responsive modern front-end framework used for grid and responsivesness.
- [Google Fonts](https://fonts.google.com/) - to import fonts.
- [FontAwesome](https://fontawesome.com/) - to provide icons used across the project. 
- [Adorable Avatars](http://avatars.adorable.io/) -  to create user avatars.
- [JQuery 3.5.0](https://jquery.com/) - to simplify DOM manipulation and to initialize Materialize functions.
---

**This project is for educational use only.**
