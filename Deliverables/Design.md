# D5. - Design

Group 08 - PlayersForge\
Group Members: Kylie Cook, Fernando Diaz, David Hermann, Jared McNeece, Conrad Murphy, Noah Olono

## 1. Description

PlayersForge is a website with a dedicated, free to join community for uploading and downloading mods. 
Users can access the PlayersForge website on their web browser and sign up to become a part of the 
modding community. Modders also can gain access to mods such as skins and maps without signing up.
Each of the mods are categorized  and sorted by the game they are for and the type of mod.

The PlayersForge website is currently still in early development, with multiple features to be 
implemented in the near future (community forum, dedicated mod pages, user profiles). The website 
provides a sleek and simple design, allowing for users to easily navigate and locate their desired 
mods. The homepage currently features the most popular or most downloaded mods.

Project Repository: [https://github.com/KylieNCook/players-forge](https://github.com/KylieNCook/players-forge)

Trello: [https://trello.com/cs3864](https://trello.com/cs3864)

## 2. Architecture

We designed out system architecture to have four layers: PSQL & Flask, models & forms, app, and 
serve. PSQL & Flask consists of packages downloaded for the website to work, the configuration, a 
Flask environment file for easy refresh changes, and SQLAlchemy to connect with out database 
models. Models & forms consists of all of our database models and forms including the
user database model and RegisterUsers form. The app layer consists of routes for the 
website, templates (HTML) and static files (CSS, images, etc.). Lastly, there is the serve file, 
which is the system of connecting our GitHub website folder to Amazon Web Services in order to 
serve the website.

![image](https://user-images.githubusercontent.com/78190024/112666147-186c2800-8e19-11eb-8d55-531e24bb5cd7.png)

## 3. Class Diagram
![Imgur](https://imgur.com/cf9KfoZ.png)

## 4. Sequence Diagram

### Use Case Description
**Use Case**: User Login
**Actor**: User
**Description**: The user logs into their account.
**Preconditions**: The user is not logged in.
**Postconditions**: The user is successfully logged in.

**Main Flow**:

1. LogInFormReader prompts the user to input their email or username and password.
2. LogInFormReader passes the information to LogInForm.
3. LogInForm verifies the information is correct with the database.
4. LogInFormReader reads LogInForm and tells the user.
5. The user is notified they are successfully logged in.

**Alternative Flow**:
1. The user inputs incorrect information into LogInFormReader.
2. LogInFormReader passes the information to LogInForm.
3. LogInForm verifies the information is incorrect with the database.
4. LogInForm notifies the user the information is incorrect.
5. LogInFormReader prompts the user to reenter their information.

### Sequence Diagram
![Sequence Diagram](https://i.imgur.com/bfbh4vJ.png)

## 5. Design Patterns
First Design Pattern was Singleton, specially used in the navigation class that was crunched into one class

![Untitled Diagram](https://github.com/KylieNCook/players-forge/blob/main/Deliverables/Untitled%20Diagram.png)

Second design patter is a Command Pattern given that all the info will be needed to perform an action.
![Sequence Diagram](https://i.imgur.com/bfbh4vJ.png)

## 6. Design Principles
We used the following SOLID design principles for our project.
Single responsibility principle: An example we used for this is the logout function. For logout() 
the purpose of it is calling another function which does the rest of the work. Thus it only has a 
single responsibility. Other examples include the index() and mods() functions which their only 
purpose is to return from a select form. 

Open/Closed principle: An open/closed principle example is our SignUpForm and LoginForm. These 
forms are part of the entire login and sign up process. They are loaded in and closed upon user 
completion. 

Dependency Inversion Principle(DIP): DIP is used in our project. In the Users class, the class 
depends on abstractions instead of lower level modules. The model carries a user's information 
automatically to the database. 
