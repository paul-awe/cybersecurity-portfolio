# TryHackMe: How Websites Work

## Room Overview

The **How Websites Work** room introduced the fundamental technologies and concepts that power modern websites. I learned how browsers communicate with web servers, the difference between front-end and back-end components, how HTML and JavaScript work, and some common web security issues such as Sensitive Data Exposure and HTML Injection.

Understanding how websites function is an essential skill for cybersecurity professionals because most attacks today target web applications and their underlying technologies.

---

## Tasks Completed

- Understanding Website Architecture
- Learning Front-End and Back-End Components
- Understanding HTML Fundamentals
- Learning JavaScript Basics
- Understanding Sensitive Data Exposure
- Learning HTML Injection Vulnerabilities

---

## Key Concepts Learned

### How Websites Work

Whenever a user visits a website, their browser sends a request to a web server.

The web server processes the request and sends back data that the browser uses to display the website.

Examples of browsers include:

- Google Chrome
- Mozilla Firefox
- Microsoft Edge
- Safari

A web server is simply a computer dedicated to processing requests and delivering website content to users.

---

## Website Components

A website consists of two major parts:

### Front End (Client-Side)

The front end is everything users see and interact with in their browser.

Examples include:

- Text
- Images
- Buttons
- Forms
- Navigation menus

The browser renders these elements for the user.

---

### Back End (Server-Side)

The back end processes requests and performs operations behind the scenes.

Examples include:

- User authentication
- Database operations
- Account management
- Data processing
- File storage

The server responds with information that is displayed on the front end.

---

## Technologies Used to Build Websites

Most websites are built using three core technologies:

### HTML

Used to create the structure of a website.

### CSS

Used to style and improve the appearance of a website.

### JavaScript

Used to add functionality and interactivity.

Together, these technologies create modern web applications.

---

# HTML Fundamentals

## What is HTML?

HTML (HyperText Markup Language) is the standard language used to create web pages.

HTML uses elements, also known as tags, to define content and structure.

Example:

```html
<!DOCTYPE html>
<html>
<head>
    <title>Page Title</title>
</head>
<body>
    <h1>Example Heading</h1>
    <p>Example paragraph.</p>
</body>
</html>
```

---

## Important HTML Elements

### <!DOCTYPE html>

Defines the document as an HTML5 page.

This helps browsers correctly interpret the page.

---

### <html>

The root element of an HTML document.

All other elements exist inside it.

---

### <head>

Contains information about the webpage.

Examples:

- Page title
- Metadata
- CSS links
- JavaScript references

---

### <body>

Contains content visible to users.

Everything displayed on the webpage appears inside the body element.

---

### <h1>

Defines a large heading.

Example:

```html
<h1>Cybersecurity Portfolio</h1>
```

---

### <p>

Defines a paragraph.

Example:

```html
<p>This is my first webpage.</p>
```

---

### Other Common Elements

Examples include:

```html
<button>Click Me</button>

<img src="image.jpg">

<ul>
    <li>Item 1</li>
</ul>
```

These allow developers to build interactive and structured web pages.

---

## HTML Attributes

Attributes provide additional information about HTML elements.

Example:

```html
<p class="bold-text">Example Text</p>
```

The class attribute can be used for styling.

---

### Image Source Attribute

Example:

```html
<img src="img/cat.jpg">
```

The src attribute tells the browser where to find the image.

---

### ID Attribute

Example:

```html
<p id="example">
```

IDs uniquely identify elements.

Unlike classes, IDs should only be used once per page.

Common uses include:

- Styling
- JavaScript interaction
- Navigation

---

## Viewing Page Source

A useful skill for cybersecurity professionals is viewing page source.

This allows analysts to inspect:

- HTML code
- Hidden comments
- Embedded scripts
- Exposed information

Most browsers allow this through:

```text
Right Click → View Page Source
```

---

# JavaScript Fundamentals

## What is JavaScript?

JavaScript is one of the most popular programming languages used on the web.

While HTML provides structure, JavaScript provides functionality and interactivity.

Without JavaScript:

- Websites would be static
- Buttons would not respond
- Dynamic content would not update

---

## What JavaScript Can Do

JavaScript can:

- Update page content
- Change page styles
- Display animations
- Validate forms
- Respond to user actions

This allows websites to become interactive.

---

## JavaScript Example

The following code changes the content of an HTML element:

```javascript
document.getElementById("demo").innerHTML = "Hack the Planet";
```

This finds an element with the ID:

```text
demo
```

and replaces its contents.

---

## JavaScript Events

HTML elements can trigger JavaScript through events.

Examples include:

- onclick
- onmouseover
- onhover
- onkeydown

Example:

```html
<button onclick='document.getElementById("demo").innerHTML = "Button Clicked";'>
Click Me!
</button>
```

When the button is clicked, the text changes automatically.

---

# Sensitive Data Exposure

## What is Sensitive Data Exposure?

Sensitive Data Exposure occurs when confidential information is accidentally exposed to users.

This information is often found in:

- HTML source code
- JavaScript files
- Comments
- Hidden pages

---

## Examples of Exposed Information

A developer might accidentally leave:

- Login credentials
- API keys
- Internal URLs
- Test accounts
- Hidden functionality

inside the website source code.

Example:

```html
<!-- TODO: remove test credentials admin:password123 -->
```

Although invisible on the page itself, anyone viewing the page source could discover it.

---

## Why This Matters

Attackers frequently inspect page source looking for:

- Credentials
- Hidden links
- Developer comments
- Internal resources

These findings can provide valuable information during security assessments.

---

## Security Best Practice

One of the first steps when assessing a web application is:

```text
View Page Source
```

This can reveal exposed information that may lead to additional vulnerabilities.

---

# HTML Injection

## What is HTML Injection?

HTML Injection occurs when a website displays user input without properly sanitizing it.

If user input is trusted, attackers can inject their own HTML into the page.

---

## Why Input Sanitization Matters

User input should never be trusted.

Examples of user-controlled input include:

- Search boxes
- Contact forms
- Registration forms
- Comment sections

If input is not sanitized, attackers can manipulate how content appears on the page.

---

## How HTML Injection Works

A website may take user input and display it directly:

```text
Welcome USERNAME
```

If no filtering exists, an attacker may submit:

```html
<h1>Hacked</h1>
```

The browser interprets this as HTML and displays it as a heading.

---

## Risks of HTML Injection

HTML Injection can allow attackers to:

- Alter page appearance
- Mislead users
- Inject malicious content
- Prepare for more advanced attacks

Although primarily a client-side issue, it demonstrates the importance of proper input validation.

---

## Security Best Practice

The golden rule of web security is:

```text
Never Trust User Input
```

All user-supplied data should be sanitized and validated before being processed or displayed.

---

## Why This Matters in Cybersecurity

Understanding how websites work provides a foundation for web application security.

Cybersecurity professionals use this knowledge to:

- Identify exposed information
- Analyze page source code
- Discover hidden functionality
- Detect input validation flaws
- Investigate web application vulnerabilities
- Perform penetration testing

Most modern cybersecurity roles require a strong understanding of web technologies.

---

## Practical Skills Gained

- Understanding website architecture
- Differentiating front-end and back-end systems
- Learning HTML fundamentals
- Understanding HTML elements and attributes
- Learning JavaScript basics
- Identifying Sensitive Data Exposure
- Understanding HTML Injection
- Recognizing the importance of input sanitization

---

## Screenshot

![How Websites Work Completion](../../assets/how-websites-work.jpg)

---

## Reflection

This room gave me a solid understanding of how websites function behind the scenes. I learned how browsers interact with web servers, how HTML creates structure, how JavaScript adds interactivity, and how common security issues such as Sensitive Data Exposure and HTML Injection can occur. Understanding these concepts is critical because web applications are one of the most common targets in cybersecurity, and this knowledge forms the foundation for future web security and penetration testing topics.

---

**Platform:** TryHackMe  
**Room:** How Websites Work  
**Completed:** Day 26–27 of My Cybersecurity Learning Journey
