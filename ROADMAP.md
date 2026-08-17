# Village Quest - Development Roadmap

## Purpose

This roadmap defines the major development and learning stages of Village Quest.

It is not a detailed task list.

Codex should use this roadmap together with:

* `PROGRESS.md`
* `docs/GAME_DESIGN.md`
* `docs/ARCHITECTURE.md`
* `docs/LEARNING_GOALS.md`
* the actual project files

to create small, manageable mini-quests.

Do not skip ahead simply because a later feature would be interesting.

The current implementation and my understanding determine when the next chapter is unlocked.

---

# Chapter 0 - Preparing the Adventure

## Goal

Prepare a clean development environment and understand the basic project workflow.

## Topics

* project structure
* Markdown documentation
* Git
* GitHub
* files and directories
* development workflow

## Milestone

The project repository is organized and ready for development.

---

# Chapter 1 - The First Village Page

## Goal

Create the first working browser page for Village Quest.

## Topics

* HTML structure
* basic CSS
* browser and server
* HTTP basics
* PHP entry point
* requests and responses

## Game Result

The player can open Village Quest in the browser and see the first version of the village.

## Milestone

Village Quest has a working starting page.

---

# Chapter 2 - Birth of a Character

## Goal

Allow the player to create a basic character.

## Topics

* HTML forms
* GET and POST
* PHP variables
* conditions
* functions
* validation
* user input
* safe output

## Game Result

The player can enter a character name and create a basic character.

## Milestone

Character creation works without permanent database storage.

---

# Chapter 3 - The Character Becomes an Object

## Goal

Introduce object-oriented programming through the character system.

## Topics

* classes
* objects
* properties
* methods
* constructors
* visibility
* responsibilities

## Game Result

The character is represented by a PHP object with its own state and behavior.

## Milestone

A simple `Character` class is used meaningfully in the game.

---

# Chapter 4 - The Village Archives

## Goal

Store game data permanently in MySQL.

## Topics

* relational databases
* tables
* rows and columns
* data types
* primary keys
* SQL
* PDO
* prepared statements
* INSERT
* SELECT
* UPDATE
* DELETE

## Game Result

Characters can be saved and loaded.

## Milestone

Character data survives between requests.

---

# Chapter 5 - Organizing the Village

## Goal

Introduce a simple MVC structure when the existing code makes the separation useful.

## Topics

* Model
* View
* Controller
* responsibilities
* request flow
* separation of concerns
* routing basics

## Game Result

The game begins to separate data and game logic from request handling and presentation.

## Milestone

A simple MVC request can be followed from browser to controller, model, view, and back to the browser.

---

# Chapter 6 - Roads Beyond the Village

## Goal

Introduce locations and travel.

## Topics

* state
* relationships
* validation
* database updates
* game rules
* controller actions

## Game Result

The character can move between allowed locations.

Possible early locations include:

* Village Square
* Tavern
* Blacksmith
* Forest
* Mine

## Milestone

Travel works and invalid travel attempts are rejected.

---

# Chapter 7 - Energy and Actions

## Goal

Give player actions costs and consequences.

## Topics

* conditions
* methods
* state changes
* server-side validation
* business rules

## Game Result

Actions such as travelling or gathering resources can consume energy.

## Milestone

The server controls whether an action is allowed and updates the character state correctly.

---

# Chapter 8 - The Adventurer's Backpack

## Goal

Create the first inventory system.

## Topics

* items
* CRUD
* foreign keys
* one-to-many relationships
* many-to-many relationships
* JOIN
* ownership
* database modelling

## Game Result

The character can own and view items.

Later iterations may allow:

* adding items
* removing items
* consuming items
* equipment

## Milestone

Inventory data is stored relationally and correctly belongs to a character.

---

# Chapter 9 - A Call to Adventure

## Goal

Create the quest system.

## Topics

* states
* relationships
* progress tracking
* conditions
* database modelling
* domain rules

## Game Result

The player can:

* discover a quest
* accept it
* make progress
* complete it
* receive a reward

## Milestone

At least one complete quest can be played from acceptance to reward.

---

# Chapter 10 - Creatures of the Forest

## Goal

Create a simple combat system.

## Topics

* objects interacting with objects
* methods
* conditions
* random values
* state transitions
* game rules
* separation of trusted server logic from browser input

## Game Result

The player can encounter and fight a simple enemy.

Possible actions:

* attack
* use an item
* flee

## Milestone

One complete combat encounter works reliably.

---

# Chapter 11 - Merchants of the Village

## Goal

Introduce buying and selling.

## Topics

* transactions
* validation
* ownership
* prices
* database consistency

## Game Result

The character can buy or sell selected items.

## Milestone

A trade either completes correctly or leaves the database unchanged.

---

# Chapter 12 - Remembering the Player

## Goal

Introduce users, login, and sessions.

## Topics

* users
* authentication
* sessions
* `password_hash()`
* `password_verify()`
* authorization
* ownership
* security

## Game Result

A player can log in and access their own character.

## Milestone

Characters and game data are protected from access by other users.

---

# Chapter 13 - Growing Village Quest

## Goal

Improve and expand the game after the core systems work.

Possible areas include:

* equipment
* character progression
* experience and levels
* more locations
* more quests
* more enemies
* NPC dialogue
* crafting
* professions
* larger storylines

New systems should only be added when there is a clear gameplay or learning reason.

---

# Final Milestone - A Complete Small RPG

Village Quest should eventually contain a complete playable loop:

Create Character

-> Explore Village

-> Accept Quest

-> Travel

-> Gather or Fight

-> Manage Inventory

-> Complete Quest

-> Receive Reward

-> Improve Character

-> Unlock Further Content

The goal is not to create the largest possible RPG.

The goal is to create a small, understandable, secure, and maintainable RPG whose important systems I can explain and modify myself.
