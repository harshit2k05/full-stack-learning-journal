# Full Stack Learning Journal

## About This Repository

This repository contains my notes, projects, and concepts that I learned during my full stack internship. I have documented everything in a simple and organized way so that I can quickly revise the concepts whenever needed.

The goal of this repository is to strengthen my fundamentals and track my learning throughout the internship.

---

## Table of Contents

- [How a Website Loads](#how-a-website-loads)
- [Browser Developer Tools](#browser-developer-tools)
- [HTML](#html-hypertext-markup-language)
- [CSS](#css-cascading-style-sheets)
- [Git & GitHub](#git--github)
- [GitHub Pages](#github-pages)
- [Markdown](#markdown)
- [Tools I Used](#tools-i-used)
- [Key Learnings](#key-learnings)
- [JavaScript Functions](#javascript-functions)
- [JavaScript Objects & Arrays](#javascript-objects--arrays)
- [Working with APIs & Fetch](#working-with-apis--fetch)
- [HTTP & REST APIs](#http--rest-apis)


# How a Website Loads

Whenever we open a website, the browser performs several steps before displaying the page.

```text
Enter URL
    │
    ▼
DNS Lookup
    │
    ▼
HTTP Request
    │
    ▼
Server Processing
    │
    ▼
HTTP Response
    │
    ▼
Browser Downloads Files
    │
    ▼
Page Rendered
```

## DNS (Domain Name System)

Computers communicate using IP addresses, while humans use domain names like `google.com`.

DNS converts a domain name into an IP address so the browser can locate the correct server.

---

## HTTP Request

The browser sends a request to the server for a resource.

### Example

```http
GET /index.html HTTP/1.1
```

| Method | Purpose |
|---------|---------|
| GET | Retrieve data |
| POST | Send new data |
| PUT | Update existing data |
| DELETE | Delete data |

---

## HTTP Response

The server processes the request and returns the requested resource along with a status code.

### Example

```http
HTTP/1.1 200 OK
Content-Type: text/html
```

### Common Status Codes

| Code | Meaning |
|------|---------|
| 200 | Success |
| 301 | Redirect |
| 400 | Bad Request |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Not Found |
| 500 | Internal Server Error |

> **Note**
>
> Opening a webpage doesn't send just one request. The browser makes separate requests for HTML, CSS, JavaScript, images, fonts, and other resources.

---

## Browser Developer Tools

Developer Tools helped me inspect webpages and debug issues while building projects.

| Tab | Purpose |
|-----|---------|
| Elements | Inspect HTML and CSS |
| Network | View requests and status codes |
| Console | Check errors and warnings |
| Sources | View project files |

Instead of guessing why something wasn't working, I learned to use DevTools to inspect elements, verify file paths, and identify errors more efficiently.

---

## Quick Revision

- DNS → Converts domain name to IP address.
- HTTP → Communication between browser and server.
- GET → Retrieve data.
- POST → Send data.
- 404 → Resource not found.
- 500 → Internal server error.
- One webpage = Multiple HTTP requests.

# HTML (HyperText Markup Language)

HTML is the standard markup language used to create the structure of a webpage. It defines what each element represents, while CSS is responsible for its appearance.

---

## Basic HTML Structure

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>My Website</title>
</head>

<body>

</body>
</html>
```

### Common HTML Tags

| Tag | Purpose |
|------|---------|
| `<!DOCTYPE html>` | Declares an HTML5 document |
| `<html>` | Root element of the webpage |
| `<head>` | Stores metadata |
| `<title>` | Browser tab title |
| `<body>` | Visible webpage content |

---

## Common HTML Elements

| Tag | Purpose |
|------|---------|
| `<h1>` - `<h6>` | Headings |
| `<p>` | Paragraph |
| `<a>` | Hyperlink |
| `<img>` | Image |
| `<ul>`, `<ol>`, `<li>` | Lists |
| `<table>` | Display tabular data |
| `<form>` | Collect user input |

---

# Semantic HTML

Semantic elements describe the purpose of the content instead of using generic `<div>` elements everywhere.

## Common Semantic Elements

| Tag | Purpose |
|------|---------|
| `<header>` | Top section of the webpage |
| `<nav>` | Navigation links |
| `<main>` | Main content |
| `<section>` | Related content |
| `<article>` | Independent content |
| `<aside>` | Sidebar or extra content |
| `<footer>` | Bottom section |

### Why Semantic HTML?

- Improves readability.
- Makes webpages more accessible.
- Helps search engines understand page structure.
- Makes code easier to maintain.

---

## `<div>` vs `<span>`

| `<div>` | `<span>` |
|----------|----------|
| Block-level element | Inline element |
| Used for larger sections | Used for small pieces of text |

---

# HTML Forms

Forms are used to collect information from users.

## Common Input Types

| Type | Purpose |
|------|---------|
| `text` | Text input |
| `email` | Email address |
| `password` | Password |
| `number` | Numeric input |
| `date` | Date selection |
| `checkbox` | Multiple selections |
| `radio` | Single selection |

---

## Quick Revision

- HTML → Webpage structure
- Semantic HTML → Meaningful elements
- `<div>` → Block element
- `<span>` → Inline element
- `alt` → Image description for accessibility
- Forms → Collect user input
- Tables → Only for tabular data

---

# CSS (Cascading Style Sheets)

CSS is used to style HTML elements. It controls the colors, fonts, spacing, layout, and responsiveness of a webpage.

---

## CSS Selectors

| Selector | Example | Purpose |
|----------|---------|---------|
| Element | `p` | Selects all `<p>` elements |
| Class | `.card` | Reusable styles |
| ID | `#header` | Styles one unique element |
| Universal | `*` | Selects every element |
| Descendant | `nav a` | Selects child elements |

> **Tip:** Use classes for reusable styles and IDs only for unique elements.

---

## Box Model

Every HTML element is treated as a box.

| Part | Purpose |
|------|---------|
| Content | Text or image |
| Padding | Space inside the border |
| Border | Boundary around the element |
| Margin | Space outside the border |

---

## Display Property

| Value | Purpose |
|-------|---------|
| `block` | Takes full width |
| `inline` | Takes only required width |
| `inline-block` | Inline with width & height |
| `flex` | Flexible layout |
| `grid` | Grid layout |
| `none` | Hides the element |

---

## Flexbox vs Grid

| Flexbox | Grid |
|----------|------|
| One-dimensional layout | Two-dimensional layout |
| Best for rows or columns | Best for complete page layouts |

---

## Position Property

| Value | Purpose |
|-------|---------|
| `static` | Default position |
| `relative` | Relative to its original position |
| `absolute` | Relative to nearest positioned parent |
| `fixed` | Stays fixed while scrolling |
| `sticky` | Sticks after reaching a position |

---

## Quick Revision

- CSS → Styling
- Class → Reusable selector
- ID → Unique selector
- Margin → Outside spacing
- Padding → Inside spacing
- Flexbox → One-dimensional layout
- Grid → Two-dimensional layout
- Media Query → Responsive design

  # Git & GitHub

Although Git and GitHub are often used together, they serve different purposes.

## Git vs GitHub

| Git | GitHub |
|------|---------|
| Version Control System | Cloud platform for Git repositories |
| Tracks changes locally | Hosts repositories online |
| Works without internet | Makes collaboration and sharing easier |

---

## Git Workflow

Whenever I worked on a project, my changes followed this workflow:

```text
Working Directory
        │
     git add
        │
        ▼
  Staging Area
        │
   git commit
        │
        ▼
 Local Repository
        │
    git push
        │
        ▼
     GitHub
```

---

## Common Git Commands

| Command | Purpose |
|----------|---------|
| `git init` | Initialize a repository |
| `git status` | Check repository status |
| `git add .` | Stage all changes |
| `git commit -m "message"` | Save a snapshot |
| `git push` | Upload commits to GitHub |
| `git pull` | Download latest changes |
| `git clone <url>` | Copy a repository |
| `git branch` | List or create branches |
| `git checkout <branch>` | Switch branches |
| `git merge` | Merge branches |

> **Tip:** Writing meaningful commit messages makes it easier to understand the project's history later.

---

# GitHub Pages

GitHub Pages allows static websites to be hosted directly from a GitHub repository.

## Steps

1. Push the project to GitHub.
2. Open **Repository Settings**.
3. Go to **Pages**.
4. Select the branch.
5. Save the settings.
6. GitHub generates a live website link.

---

# Markdown

Markdown is a lightweight language used for writing documentation.

I used Markdown to create README files because it is simple, readable, and supported by GitHub.

## Common Syntax

| Syntax | Output |
|---------|--------|
| `# Heading` | Heading |
| `**Text**` | **Bold** |
| `*Text*` | *Italic* |
| `` `code` `` | `code` |
| `- Item` | Bullet List |
| `1. Item` | Numbered List |

---

# Tools I Used

| Tool | Purpose |
|------|---------|
| VS Code | Writing and managing code |
| Chrome DevTools | Inspecting HTML, CSS, and Network requests |
| Git | Version control |
| GitHub | Hosting repositories |
| GitHub Pages | Hosting static websites |
| Dillinger | Writing and previewing Markdown |

---

# Key Learnings

- Understanding concepts is more important than memorizing syntax.
- Writing clean HTML makes CSS easier to manage.
- Git provides confidence to experiment because changes can always be tracked.
- Browser Developer Tools are essential for debugging.
- Building projects is the best way to strengthen fundamentals.
- Clean code, meaningful file names, and proper folder structure make projects easier to maintain.

---
## Quick Revision

- Git → Version control
- GitHub → Online repository hosting
- Commit → Snapshot of changes
- Push → Upload changes
- Pull → Download latest changes
- GitHub Pages → Host static websites
- Markdown → Documentation
---
## JavaScript Functions

JavaScript functions are reusable blocks of code used to perform a specific task. They help make code modular, reusable, and easier to maintain.

### Function Declaration

```javascript
function greet(name) {
    return `Hello, ${name}!`;
}

console.log(greet("Bhanu"));
```

### Function Expression

```javascript
const add = function(a, b) {
    return a + b;
};

console.log(add(5, 3));
```

### Arrow Function

```javascript
const square = (num) => num * num;

console.log(square(5));
```

### Parameters & Arguments

- **Parameters** are variables defined in a function.
- **Arguments** are the values passed while calling the function.

```javascript
function multiply(a, b) {
    return a * b;
}

console.log(multiply(4, 6));
```

### Return Statement

```javascript
function cube(num) {
    return num ** 3;
}

console.log(cube(3));
```

### Callback Function

A callback is a function passed as an argument to another function.

```javascript
function process(callback) {
    callback();
}

process(() => {
    console.log("Task Completed");
});
```

### Scope

- Global Scope
- Local Scope
- Block Scope

```javascript
let language = "JavaScript";

function showLanguage() {
    console.log(language);
}
```

---

# JavaScript Events

An **event** is an action that occurs in the browser, such as clicking a button, typing in an input box, or moving the mouse. JavaScript can respond to these events using event listeners.

## Common Events

| Event | Description |
|--------|-------------|
| click | Triggered when an element is clicked |
| dblclick | Triggered on double click |
| mouseover | Mouse enters an element |
| mouseout | Mouse leaves an element |
| keydown | A key is pressed |
| keyup | A key is released |
| input | Input value changes |
| submit | Form is submitted |
| change | Input value changes after losing focus |
| load | Page finishes loading |

---

## Event Listener

The `addEventListener()` method is the preferred way to handle events.

```javascript
const button = document.querySelector("button");

button.addEventListener("click", () => {
    alert("Button Clicked!");
});
```

---

## Event Object

JavaScript automatically passes an event object containing information about the event.

```javascript
document.addEventListener("click", function(event) {
    console.log(event.target);
});
```

---

## Prevent Default Action

```javascript
const form = document.querySelector("form");

form.addEventListener("submit", function(event) {
    event.preventDefault();
    console.log("Form submission prevented.");
});
```

---

## Practice Example

```javascript
const btn = document.getElementById("btn");

btn.addEventListener("click", () => {
    btn.textContent = "Clicked!";
});
```

---

## Key Learnings

- Learned different types of JavaScript functions.
- Understood parameters, arguments, and return values.
- Practiced callback functions and variable scope.
- Learned how JavaScript responds to browser events.
- Used `addEventListener()` to handle user interactions.
- Understood the event object and `preventDefault()`.

---
# JavaScript Objects & Arrays

## Objects

- Stores related data as **key-value pairs**.
- Used for users, products, employees, etc.

```javascript
const student = {
  name: "Rahul",
  age: 18
};
```

### Access Properties

```javascript
student.name
student["age"]
```

### Add / Update / Delete

```javascript
student.city = "Delhi";
student.age = 19;
delete student.city;
```

### Object Methods

- Method = Function inside an object.
- `this` refers to the current object.

### Useful Methods

- `Object.keys()` → Keys
- `Object.values()` → Values
- `Object.entries()` → Key-value pairs

---

## Arrays

- Stores multiple values in order.
- Real-world data usually comes as **arrays of objects**.

```javascript
const products = [
  { id: 1, name: "Laptop", price: 65000 },
  { id: 2, name: "Mouse", price: 500 }
];
```

---

## Array Methods

| Method | Purpose |
|---------|---------|
| `forEach()` | Run code for every item |
| `map()` | Create a new array |
| `filter()` | Keep matching items |
| `find()` | First matching item |
| `some()` | Returns true if any match |
| `every()` | Returns true if all match |
| `sort()` | Sort items |
| `reduce()` | Convert to one value |

---

## Quick Revision

- Object → Key-value pairs
- Array → Ordered list
- `this` → Current object
- `map()` → New array
- `filter()` → Matching items
- `find()` → One item
- `reduce()` → One value
- `some()` → Any?
- `every()` → All?

---

# Working with APIs & Fetch

## API

- API connects the client and server.
- Client sends a request, server sends a response.
- One request = One response.

---

## Request & Response

### Request

- Method
- URL
- Headers
- Body

### Response

- Status Code
- Headers
- Body

> Always check the **status code first**.

---

## JSON

- `response.json()` → Convert JSON to JavaScript object.
- `JSON.stringify()` → Convert JavaScript object to JSON.

---

## HTTP Methods

| Method | Purpose |
|---------|---------|
| GET | Read data |
| POST | Create data |
| PUT | Replace data |
| PATCH | Update data |
| DELETE | Remove data |

---

## Common Status Codes

| Code | Meaning |
|------|---------|
| 200 | OK |
| 201 | Created |
| 204 | No Content |
| 400 | Bad Request |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Not Found |
| 429 | Too Many Requests |
| 500 | Server Error |

---

## fetch()

```javascript
fetch(url)
```

### Using async/await

```javascript
const res = await fetch(url);
const data = await res.json();
```

---

## Sending Data

```javascript
fetch(url, {
  method: "POST",
  headers: {
    "Content-Type": "application/json"
  },
  body: JSON.stringify(data)
});
```

---

## Error Handling

- `fetch()` throws only for network errors.
- Check `res.ok` for HTTP errors.

---

## Authentication

- API Key → Identifies the application.
- Bearer Token → Identifies the user.
- Store secrets in `.env`.
- Never push API keys to GitHub.

---



---
## HTTP & REST APIs

HTTP (HyperText Transfer Protocol) is a communication protocol that allows a client (browser or mobile app) to communicate with a server. Whenever we visit a website, submit a form, or request data, HTTP is used.

REST (Representational State Transfer) is an architectural style used to build web APIs. REST APIs use HTTP methods to perform different operations on resources.

---

## How HTTP Works

```
Client (Browser)
       │
       │ HTTP Request
       ▼
     Server
       │
       │ HTTP Response
       ▼
Client (Browser)
```

### Example

When you open **https://github.com**:

1. Your browser sends an HTTP request.
2. GitHub's server receives the request.
3. The server processes it.
4. The webpage is sent back as an HTTP response.

---

# HTTP Request

An HTTP request is sent by the client to the server.

It contains:

- URL
- HTTP Method
- Headers
- Body (optional)

---

# HTTP Response

An HTTP response is sent by the server back to the client.

It contains:

- Status Code
- Headers
- Response Body

---

# HTTP Methods

### GET
Used to retrieve data from the server.

### POST
Used to create new data on the server.

### PUT
Used to replace an existing resource completely.

### PATCH
Used to update only specific fields of an existing resource.

### DELETE
Used to remove data from the server.

---

# Common HTTP Status Codes

| Status Code | Meaning |
|-------------|---------|
| 200 | Request Successful |
| 201 | Resource Created Successfully |
| 400 | Bad Request |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Resource Not Found |
| 500 | Internal Server Error |

---

# What is REST?

REST (Representational State Transfer) is a way of designing APIs. It uses HTTP methods to perform operations on resources.

A resource can be anything like:

- Users
- Products
- Orders
- Students

REST APIs use meaningful URLs to access these resources.

---

# REST API Example

| HTTP Method | Endpoint | Description |
|-------------|----------|-------------|
| GET | `/users` | Get all users |
| GET | `/users/1` | Get a specific user |
| POST | `/users` | Create a new user |
| PUT | `/users/1` | Replace user information |
| PATCH | `/users/1` | Update specific user details |
| DELETE | `/users/1` | Delete a user |

---

# JSON

JSON (JavaScript Object Notation) is the most common format used to exchange data between a client and a server.

Example:

```json
{
  "id": 1,
  "name": "Bhanu Joshi",
  "course": "Full Stack Development"
}
```

# Key Learnings

- Learned how clients and servers communicate using HTTP.
- Understood the difference between an HTTP request and an HTTP response.
- Learned the purpose of GET, POST, PUT, PATCH, and DELETE methods.
- Learned common HTTP status codes and their meanings.
- Understood how REST APIs organize resources using endpoints.
- Learned that JSON is the standard format for exchanging data in REST APIs.
---
## Quick Revision

- API → Client ↔ Server
- JSON → Data format
- GET → Read
- POST → Create
- PUT → Replace
- PATCH → Update
- DELETE → Remove
- `fetch()` → Send request
- `await res.json()` → Read response
- `res.ok` → Check success
- `.env` → Store secret keys
---
# Final Note

This repository documents my learning during the initial phase of my web development internship.

I will continue updating it as I learn new concepts, build more projects, and improve my development skills.
