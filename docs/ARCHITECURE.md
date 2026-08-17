# Village Quest - Architecture

## Purpose

This document describes the current technical architecture of Village Quest.

It should stay simple and grow only when the project creates a real need for more structure.

Do not add architectural patterns only because they are common in professional projects.

Every new abstraction should solve a concrete problem in Village Quest.

---

# Technology Stack

Village Quest uses:

* PHP for server-side logic
* MySQL as the relational database
* SQL for database queries
* HTML for page structure
* CSS for presentation
* JavaScript for browser-side interaction when needed

Large application frameworks are not used during the early development stages.

---

# Architecture Goal

The project should gradually evolve toward a simple object-oriented MVC architecture.

MVC means:

* Model
* View
* Controller

The architecture should help separate responsibilities.

The project should not be forced into a complex MVC structure before that separation solves an actual problem.

---

# Basic Request Flow

A typical request should eventually follow this flow:

Browser

-> HTTP Request

-> Controller

-> Model / Game Logic

-> Database

-> Controller

-> View

-> HTTP Response

-> Browser

Not every early development step needs the complete flow.

---

# Controllers

Controllers are responsible for handling requests and coordinating the application.

Typical responsibilities include:

* reading request data
* calling Models or domain objects
* coordinating game actions
* handling validation results
* selecting the appropriate View or response

Controllers should not contain large amounts of game logic.

---

# Models

Models represent important game data and rules.

Possible future examples include:

* Character
* Location
* Item
* Quest

Models may contain:

* state
* game rules
* domain behaviour
* data-related logic according to the current stage of the project

Models should not generate HTML.

---

# Views

Views are responsible for presentation.

They may contain:

* HTML
* displayed values
* simple presentation logic

Views should not contain:

* SQL queries
* important game rules
* database access logic

The View displays the result of the application logic.

It should not decide whether a game action is valid.

---

# Object-Oriented Design

PHP code should gradually use object-oriented programming where it provides a clear benefit.

Classes should have clear responsibilities.

A class should not be created only because something is a noun.

Before creating a new class, ask:

* What responsibility does this class have?
* What data does it need?
* What behaviour belongs to it?
* Does this class solve a real problem in the current code?

Prefer small and understandable classes.

---

# Game State

Important game state must be controlled by the server.

Examples include:

* character health
* energy
* gold
* experience
* current location
* inventory ownership
* quest progress
* rewards

The browser may request an action.

The browser must not be trusted to decide the result of that action.

Example:

The browser may send:

"Gather wood"

The server decides:

* whether gathering is allowed
* whether enough energy exists
* how much energy is consumed
* how much wood is received
* how the inventory changes

---

# Database

MySQL is used for persistent game data.

Database access should use PHP PDO.

Prepared statements should be used when user-controlled values are included in SQL queries.

Database design should be introduced gradually as game systems require it.

Possible future data areas include:

* characters
* locations
* items
* inventory
* quests
* quest progress
* users

Do not create all tables before they are needed.

---

# Frontend

HTML and CSS are responsible for the basic user interface.

JavaScript should be introduced when browser-side interaction provides a real benefit.

JavaScript may later be used for:

* DOM updates
* user interactions
* Fetch requests
* JSON communication with the PHP backend

Important game rules must still be validated on the server.

---

# Security Principles

The server must treat browser input as untrusted.

Important security areas include:

* input validation
* output escaping
* SQL injection prevention
* session security
* authentication
* authorization
* ownership checks

Security should be introduced together with the feature that creates the risk.

Do not postpone obvious security problems simply because the project is a learning project.

---

# Project Structure

The exact directory structure should evolve with the project.

Do not create directories before they have a clear responsibility.

Current high-level structure:

```text
Village-Quest/
├── AGENTS.md
├── README.md
├── ROADMAP.md
├── PROGRESS.md
├── docs/
│   ├── GAME_DESIGN.md
│   ├── ARCHITECTURE.md
│   └── LEARNING_GOALS.md
└── src/
```

Future MVC directories may include structures such as:

```text
src/
├── Controllers/
├── Models/
└── Views/
```

These directories should be introduced when the project actually begins using these responsibilities.

---

# Architectural Principles

## Keep It Simple

Use the simplest structure that solves the current problem clearly.

## Separate Responsibilities

Keep presentation, application coordination, game rules, and database logic separated where practical.

## Introduce Complexity Gradually

Do not introduce advanced patterns before the project creates a need for them.

## Server Is Authoritative

Important game state and game rules are decided and validated by the server.

## Learn the Fundamentals

Prefer direct and understandable PHP, SQL, HTML, CSS, and JavaScript over abstractions that hide how the system works.

## Refactor When Needed

The architecture may change as the project grows.

Refactoring is expected when existing code becomes difficult to understand, duplicate, or maintain.

---

# Not Planned for Early Development

Do not introduce these without a concrete reason:

* large PHP frameworks
* frontend frameworks
* microservices
* dependency injection containers
* event buses
* complex routing systems
* Repository Pattern
* service layers
* ORM systems
* advanced design patterns

These may be discussed later if a real project problem makes them useful.

---

# Architecture Decision Rule

Before introducing a new architectural concept, ask:

"What problem in the current Village Quest code does this solve?"

If there is no clear answer, the concept should probably not be introduced yet.
