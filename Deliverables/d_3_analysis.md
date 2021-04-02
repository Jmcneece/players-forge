# D.3 Analysis 

Group 08 - PlayersForge\
Group Members: Kylie Cook, Fernando Diaz, David Hermann, Jared McNeece, Conrad Murphy, Noah Olono

## 1. System Description 

### Problem Statement:
Modifications (known informally as mods) enhance games. Some improve immersion or create a different style. However, finding unique mods and installing them can be onerous. Sometimes it is difficult to find mods for specific games while at other times services such as the Steam Workshop do not support certain titles. The lack of support may be because the game is old or third party developers do not have a good relationship with Steam. Even when mods are available, the process modders have to go through can be time consuming and exhausting.

### Product Position Statement:
For individuals who want the best mod service, PlayersForge will become the central leader of mods that will deliver innovative solutions to facilitate access to the users favorite mods so they can enjoy a seamless experience across all their games, because PlayersForge takes an innovative approach to technological practices, which considers the impact that our product will have on our customers.

### Value Proposition:
PlayersForge is the easiest way to find a mod because many mods are tailored to the needs of its users, including a recommendation system.

### Model:
Users will be able to browse most web pages without having to create an account. Users will be able to search for and download mods. **Mods** will have a *title*, *description*, *image*, *date published*, ***game*** that the mod belongs to, ***mod categories*** that relate to the mod, and *files* that are part of the mod itself. Each **game** is a directory that __contains__ all *mods* that are made for the game in question. Games should also include a *name*, *image*, and ***game categories*** that relate to the game.

If a user wants to create a mod, they will have to sign up and create an account to become a registered member. **Members** can __create__ mods; a list of all their created mods is stored in their member info. They can also __mark certain mods as *favorite*__ for easy access to them.

A rating system may also be used to determine the popularity of certain mods. Each mod would store the number of *likes* and *dislikes* received over time. These numbers, factored in with the *publication date*, would make mods eligible for display in Popular/Trending pages. Members receive a better *reputation* on their profile if they create mods with high overall ratings.

Some web pages will be community pages where members can make forum-style posts or participate in a live chat similar to what Discord provides. **Forums** will __contain__ a list of *subjects* and **posts**, which will have a *title*, *date published*, *member* who __published__ the post, and the *content* of the post. **Private Messages**, on the other hand, will __contain__ a list of **chats** that will each __contain__ lists of **messages** each with their own info about the *date posted*, *member* who __posted__ it, and *content* of the message.

## 2. Model 
![UML Class Diagram](https://i.imgur.com/zTyb0nw.png)