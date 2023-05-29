# Installation

### Install Brew (Linux / Mac):

```
sudo apt update
sudo apt install curl
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

### Install Git:

1. Windows: https://git-scm.com/downloads

2. Linux / Mac:
```
brew install git
```

### Install VSCode: 

Install VSCode from: https://code.visualstudio.com/download

### Install NVM from:

1. Windows - https://github.com/coreybutler/nvm-windows/releases

2. Linux / Mac:
```
brew install nvm
```

### Install Latest Node Version using NVM from cmd (in windows) / terminal (in linux / mac):

```
nvm install 18 && nvm use 18
```

### Download Latest Ruby Devkit:

1. Windows: https://www.ruby-lang.org/en/downloads/

2. Linux / Mac:
```
brew install ruby@3.1
```

# Rails getting started

Use this project as a starting point to learn and improve your Rails skills.

Here are the problem description:

* This application is completely REST API based. No need for frontend with erb, or javascript.
* You can use either [Insomnia](https://insomnia.rest/) or [Postman](https://www.postman.com/) to test your rest API, including all features.

## Part1:

We are building a sports website where users will be able to participate in games.

* First there are "Game" as the top most resource. Each game could be Football, basketball, tabletennis, etc.
  * You should be able to do CRUD operations using JSON api. CRUD = Create, Retrieve, Update, Delete.
  * League has these fields: 
    * Name: (Football, Basketball, ...)
    * Governing body: National Football association, etc
* Second you have "Division"
  * Each division will belong to a Game. There can be multiple divisions per game. Eg: Football can have, "Premier league", "First division", "Second division", etc. You should be able to do CRUD operations on a division
  * Following fields
    * Name: Premier league, First division, etc
    * Game: the id of the game
* Third you have "Team". A team will belong to a division. Eg: Chelsea, Arsenal will belong to "Premier league" division. "Three start club" will belong to "First division". You should be able to do CRUD operations with JSON REST API.
  * Following fields
    * Name
    * division id
    * Manager name
    * Manager contact
 
 ## Part 2:
 
 We will add authentication to the app.
 
 1. We should be able to create accounts.
 2. Admin account can do CRUD operation on any of the three resources above: Game, Division, Team.
 3. Regular account can do CRUD operation only on their own. Eg: They can create a Game, add divisions to the game, add teams inside the divisions. But they should not be able to do CRUD operations on other people's resources.

## Part 3: Deployment

Create a free account in heroku. And deploy your application there. You should be able to finally test all of these features on heroku using Postman or Insomnia.
