# Architecture

Village Quest uses a simple MVC architecture.

Browser
    ↓
Controller
    ↓
Model
    ↓
Database

Controller
    ↓
View
    ↓
Browser

Models
- game rules
- domain data
- database access

Views
- HTML output
- presentation

Controllers
- process HTTP requests
- coordinate models and views

Rules
- no SQL inside Views
- no HTML inside Models
- no game rules inside Views