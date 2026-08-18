# Village Quest - Learning Goals

## Purpose

This document defines what I should learn while building Village Quest.

The goal is not only to complete game features.

I should gradually become able to understand, explain, debug, modify, and extend the project myself.

The roadmap defines when topics are introduced.

This document defines what I should understand about them.

---

# General Programming

I should become confident with:

* variables
* data types
* conditions
* loops
* functions
* parameters
* return values
* arrays
* objects
* scope
* state
* data flow
* validation
* error handling
* debugging
* modularization
* naming
* readability
* reuse

I should be able to explain:

* where data comes from
* where it goes
* when it changes
* which part of the program is responsible for changing it

---

# PHP

I should learn to use PHP for server-side application logic.

Important topics include:

* PHP syntax
* variables
* arrays
* functions
* conditions
* loops
* forms
* GET
* POST
* request data
* validation
* safe output
* sessions
* error handling
* PDO
* database access

I should understand the difference between:

* browser-side code
* server-side code
* user input
* trusted application state

---

# Object-Oriented Programming

Object-oriented programming should be introduced through real problems in Village Quest.

I should learn:

* classes
* objects
* properties
* methods
* constructors
* visibility
* composition
* inheritance
* interfaces
* namespaces

For every important class, I should be able to explain:

* what responsibility it has
* what data it owns
* what behaviour belongs to it
* what inputs it receives
* what outputs it produces
* what other objects it depends on

I should not create classes only because something is a noun.

I should understand what problem each OOP concept solves.

---

# MVC

I should learn how a simple MVC application is structured.

I should understand the responsibilities of:

## Model

* game data
* domain rules
* data-related behaviour

## View

* presentation
* HTML output
* displaying application data

## Controller

* receiving requests
* coordinating actions
* calling Models
* selecting Views or responses

I should be able to follow a request through the application:

Browser

-> Controller

-> Model

-> Database

-> Controller

-> View

-> Browser

I should be able to decide whether a piece of code belongs in a Model, View, or Controller.

---

# HTTP and Web Applications

I should understand how the browser and server communicate.

Important topics include:

* HTTP request
* HTTP response
* GET
* POST
* URL parameters
* form data
* headers at a basic level
* status codes at a basic level

I should understand that the browser sends requests but the server decides the trusted game result.

---

# HTML

HTML should support the application.

I should learn:

* semantic document structure
* headings
* paragraphs
* links
* forms
* inputs
* buttons
* lists
* tables where appropriate

I should be able to create clear and usable game interfaces without depending on a UI framework.

---

# CSS

CSS should be introduced as needed for presentation.

I should learn:

* selectors
* classes
* box model
* spacing
* typography
* layout
* Flexbox
* basic responsive design

The goal is not advanced visual design.

The goal is to understand how presentation is separated from application logic.

---

# JavaScript

JavaScript should be introduced when browser-side interaction becomes useful.

I should learn:

* variables
* functions
* arrays
* objects
* DOM manipulation
* events
* form interaction
* modules
* asynchronous programming
* Fetch API
* JSON
* browser debugging

I should understand the difference between:

* improving the user interface in JavaScript
* enforcing important game rules on the server

The browser must not be trusted with important game state.

---

# SQL and MySQL

I should understand relational databases and how application data is stored.

Important topics include:

* databases
* tables
* rows
* columns
* data types
* primary keys
* foreign keys
* relationships
* normalization at a practical level
* constraints
* indexes at a basic level

I should learn:

* SELECT
* INSERT
* UPDATE
* DELETE
* WHERE
* ORDER BY
* GROUP BY
* JOIN

Later I should also understand:

* transactions
* database consistency

Village Quest systems should be used as examples.

Possible mappings:

Character

-> basic CRUD

Inventory

-> relationships and JOINs

Quests

-> state and relational modelling

Trading

-> transactions

Users

-> authentication and ownership

---

# Database Access with PDO

I should learn to access MySQL through PHP using PDO.

Important topics include:

* creating a connection
* executing queries
* fetching results
* prepared statements
* parameters
* handling database errors

I should understand why prepared statements help protect against SQL injection.

---

# Security

Security should be learned together with the feature that creates the risk.

Important topics include:

* validating input
* escaping output
* SQL injection
* XSS
* authentication
* authorization
* sessions
* password hashing
* ownership checks
* manipulated browser requests

I should understand that data coming from the browser cannot automatically be trusted.

Examples of values the server must control include:

* gold
* experience
* energy
* health
* quest rewards
* item ownership
* combat results

---

# State

State is an important concept throughout Village Quest.

I should understand different forms of state, including:

* values inside variables
* object state
* session state
* database state
* browser state

Game systems such as:

* character health
* energy
* inventory
* location
* quest progress

should help me understand how state changes over time.

---

# Debugging

I should learn to investigate problems systematically.

The debugging process should include:

1. read the exact error
2. identify the file and line
3. understand what the error means
4. formulate possible causes
5. test one cause at a time
6. make one change
7. test again

Tools I should learn include:

* PHP error messages
* `var_dump()`
* `print_r()`
* browser console
* JavaScript breakpoints
* Network tab
* SQL queries
* application logs

I should learn how to find the cause of a problem instead of only copying a fix.

---

# Git and GitHub

I should learn to use Git as part of normal development.

Important topics include:

* repository
* working tree
* staging
* commit
* commit history
* diff
* branch basics
* remote repositories
* push
* pull

I should develop the habit of making small and meaningful commits.

I should be able to explain what changed in a commit and why.

---

# Software Design

I should gradually learn how to structure software.

Important ideas include:

* separation of concerns
* responsibilities
* cohesion
* coupling
* duplication
* abstraction
* refactoring
* maintainability

Advanced patterns should only be introduced when the existing code creates a real need for them.

I should learn to distinguish between code that:

* works
* is understandable
* is secure
* is maintainable
* is appropriately designed

These are not always the same thing.

---

# Problem Solving

One of the main goals of the project is to improve independent problem solving.

Before coding, I should increasingly be able to ask:

* What exactly is the problem?
* What is the smallest useful step?
* What data do I need?
* Where does that data come from?
* What rules apply?
* What should happen if something goes wrong?
* Which part of the application is responsible?
* How can I test whether my solution works?

I should gradually need fewer hints from Codex.

---

# Reading Documentation

I should learn to use technical documentation instead of depending entirely on AI.

Preferred sources include:

* PHP Manual
* MDN Web Docs
* MySQL Documentation
* Bootstrap Documentation
* Material Design documentation

W3Schools may be used for simple introductions.

I should learn to:

* search for the correct term
* identify the relevant section
* understand examples
* adapt examples to Village Quest
* verify important technical details

---

# Learning Through Game Systems

Village Quest features should be connected to programming concepts where useful.

Examples:

## Character Creation

Practice:

* forms
* POST
* validation
* variables
* safe output

## Character System

Practice:

* classes
* objects
* properties
* methods
* state

## Travel

Practice:

* conditions
* state changes
* game rules
* validation

## Inventory

Practice:

* CRUD
* database relationships
* JOINs
* ownership

## Quests

Practice:

* states
* conditions
* relationships
* progress tracking

## Combat

Practice:

* methods
* object interaction
* conditions
* state transitions

## Trading

Practice:

* transactions
* validation
* database consistency

## Login

Practice:

* sessions
* authentication
* authorization
* password security

---

# Understanding Before Progress

A feature is not fully learned only because it works.

Before moving on, I should increasingly be able to answer questions such as:

* What input does this function expect?
* What does it return?
* Where does this value come from?
* Where is this value stored?
* Which code is allowed to change it?
* Why does this class exist?
* Does this belong in Model, View, or Controller?
* What could the browser manipulate?
* What happens when invalid input is sent?
* How would I debug this if it stopped working?

Codex may use these questions during quest reviews.

---

# Long-Term Goal

By the end of the project, I should not only have a working browser RPG.

I should be able to:

* understand the project structure
* explain the important code
* implement small features independently
* debug common problems
* design simple database structures
* work with PHP and MySQL securely
* use JavaScript for browser interaction
* reason about MVC and OOP
* recognize when refactoring is needed
* research technical questions independently
* use Git confidently
* justify basic architectural decisions

The project succeeds when my ability improves together with the game.
