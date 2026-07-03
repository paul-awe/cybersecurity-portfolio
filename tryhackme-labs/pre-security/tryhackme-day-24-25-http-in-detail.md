# TryHackMe: HTTP in Detail

## Room Overview

The **HTTP in Detail** room provided a comprehensive introduction to how web browsers communicate with web servers using the HyperText Transfer Protocol (HTTP). I learned how websites are requested and delivered, how URLs are structured, the differences between HTTP and HTTPS, common HTTP methods, status codes, headers, and how cookies help websites remember users.

Understanding HTTP is essential for cybersecurity professionals because web applications are among the most common attack surfaces targeted by attackers.

---

## Tasks Completed

* Understanding HTTP and HTTPS
* Learning URL Structure
* Understanding HTTP Requests and Responses
* Exploring HTTP Methods
* Learning HTTP Status Codes
* Understanding HTTP Headers
* Learning How Cookies Work

---

## Key Concepts Learned

### What is HTTP?

HTTP (HyperText Transfer Protocol) is the protocol used by web browsers and web servers to communicate.

HTTP was developed by **Tim Berners-Lee** and his team between 1989 and 1991.

HTTP allows the transfer of:

* HTML Pages
* Images
* Videos
* CSS Files
* JavaScript Files
* Documents

Every time a website is visited, HTTP requests and responses are exchanged between the browser and the server.

---

### What is HTTPS?

HTTPS (HyperText Transfer Protocol Secure) is the secure version of HTTP.

HTTPS encrypts communication between the client and the server.

Benefits include:

* Data confidentiality
* Data integrity
* Server authentication
* Protection against interception

Without HTTPS, attackers could potentially view transmitted information.

---

## What is a URL?

A URL (Uniform Resource Locator) is the address used to access resources on the internet.

Example:

```text
http://user:password@tryhackme.com:80/view-room?id=1#task3
```

A URL contains several important components.

---

### Scheme

The scheme specifies the protocol used.

Examples:

```text
http
https
ftp
```

---

### User Information

Some services allow authentication directly through the URL.

Example:

```text
user:password
```

---

### Host

The host identifies the server.

Examples:

```text
tryhackme.com
google.com
192.168.1.1
```

---

### Port

The port identifies which service should receive the request.

Common ports:

```text
80  = HTTP
443 = HTTPS
```

Valid ports range from:

```text
1 - 65535
```

---

### Path

The path identifies the resource being requested.

Example:

```text
/view-room
/blog
/login
```

---

### Query String

Additional information can be sent using query parameters.

Example:

```text
/blog?id=1
```

This tells the application which specific content should be returned.

---

### Fragment

Fragments reference a specific section of a webpage.

Example:

```text
#task3
```

This allows users to jump directly to a section of a page.

---

## HTTP Requests

An HTTP request is sent by a client (browser) to a web server.

Example:

```http
GET / HTTP/1.1
Host: tryhackme.com
User-Agent: Mozilla/5.0 Firefox/87.0
Referer: https://tryhackme.com/
```

### Request Breakdown

#### Line 1

```http
GET / HTTP/1.1
```

Contains:

* Request Method
* Requested Resource
* HTTP Version

---

#### Host Header

```http
Host: tryhackme.com
```

Identifies the target website.

---

#### User-Agent Header

```http
User-Agent: Mozilla/5.0 Firefox/87.0
```

Identifies the browser and version.

---

#### Referer Header

```http
Referer: https://tryhackme.com/
```

Indicates which page referred the user.

---

#### Blank Line

Every HTTP request ends with a blank line.

This tells the server the request is complete.

---

## HTTP Responses

After processing a request, the server sends a response.

Example:

```http
HTTP/1.1 200 OK
Server: nginx/1.15.8
Date: Fri, 09 Apr 2021 13:34:03 GMT
Content-Type: text/html
Content-Length: 98
```

Followed by the requested content.

---

### Response Breakdown

#### Status Line

```http
HTTP/1.1 200 OK
```

Contains:

* HTTP Version
* Status Code
* Status Message

---

#### Server Header

```http
Server: nginx/1.15.8
```

Identifies the server software.

---

#### Date Header

Provides:

* Current date
* Time
* Time zone

---

#### Content-Type Header

Identifies the type of content being returned.

Examples:

```text
text/html
image/png
application/pdf
application/json
```

---

#### Content-Length Header

Specifies the size of the response.

This helps verify that all data was received.

---

## HTTP Methods

HTTP methods indicate the intended action being performed.

---

### GET

Used to retrieve information from a server.

Examples:

* Viewing webpages
* Downloading files
* Retrieving API data

---

### POST

Used to submit data to a server.

Examples:

* Logging in
* Creating accounts
* Submitting forms

---

### PUT

Used to update existing information.

Examples:

* Updating user profiles
* Editing records

---

### DELETE

Used to remove resources.

Examples:

* Deleting accounts
* Removing files
* Deleting records

---

## HTTP Status Codes

Status codes inform the client about the outcome of a request.

---

### 100–199 Informational

Indicates that the request has been received and processing continues.

---

### 200–299 Success

Indicates successful processing.

---

### 300–399 Redirection

Indicates that the client should access another resource.

---

### 400–499 Client Errors

Indicates a problem with the client's request.

---

### 500–599 Server Errors

Indicates a problem on the server.

---

## Common HTTP Status Codes

### 200 OK

The request completed successfully.

---

### 201 Created

A new resource was successfully created.

Examples:

* New user account
* New blog post

---

### 301 Moved Permanently

The resource has permanently moved to a new location.

---

### 302 Found

A temporary redirect.

---

### 400 Bad Request

The request contains missing or invalid information.

---

### 401 Unauthorized

Authentication is required.

---

### 403 Forbidden

Access is denied even if authenticated.

---

### 404 Not Found

The requested resource does not exist.

One of the most common HTTP errors.

---

### 405 Method Not Allowed

The requested HTTP method is not permitted.

Example:

```text
Sending GET when POST was required.
```

---

### 500 Internal Server Error

A server-side error occurred.

---

### 503 Service Unavailable

The server is overloaded or under maintenance.

---

## HTTP Headers

Headers provide additional information during communication.

---

### Common Request Headers

#### Host

Specifies the target website.

---

#### User-Agent

Identifies browser software and version.

---

#### Content-Length

Specifies the amount of data being sent.

---

#### Accept-Encoding

Identifies supported compression methods.

Examples:

```text
gzip
br
deflate
```

---

#### Cookie

Sends previously stored cookie data.

---

### Common Response Headers

#### Set-Cookie

Stores cookie data on the client.

---

#### Cache-Control

Determines how long content should be cached.

---

#### Content-Type

Specifies the type of returned content.

---

#### Content-Encoding

Specifies the compression method used.

---

## Cookies

Cookies are small pieces of information stored in a user's browser.

Since HTTP is stateless, cookies allow websites to remember users between requests.

Examples of stored information:

* Login sessions
* User preferences
* Shopping cart contents
* Authentication tokens

---

### How Cookies Work

1. User visits a website.
2. Server sends a Set-Cookie header.
3. Browser stores the cookie.
4. Future requests automatically include the cookie.
5. Server recognizes the user.

This process enables persistent user sessions.

---

### Why Cookies Matter

Cookies are commonly used for:

* Authentication
* Personalization
* Session management
* User tracking
* Security controls

Most modern websites rely heavily on cookies.

---

## Why This Matters in Cybersecurity

HTTP knowledge is fundamental in cybersecurity because web applications are one of the primary targets of cyberattacks.

Security professionals use HTTP knowledge to:

* Analyze web traffic
* Identify vulnerabilities
* Investigate malicious requests
* Perform penetration testing
* Secure web applications
* Troubleshoot network issues

A strong understanding of HTTP is essential for web security assessments and incident investigations.

---

## Practical Skills Gained

* Understanding HTTP and HTTPS
* Identifying URL components
* Understanding request and response structures
* Learning HTTP methods
* Understanding status codes
* Analyzing headers
* Understanding cookies and session management
* Building foundational web application security knowledge

---

## Screenshot

![HTTP in Detail Completion](../../assets/http-in-detail.jpg)

---

## Reflection

This room gave me a deeper understanding of how web browsers and servers communicate using HTTP and HTTPS. I learned how requests and responses are structured, how URLs identify resources, and how status codes, headers, and cookies play critical roles in web functionality. Since web applications are a major focus area in cybersecurity, understanding HTTP provides a strong foundation for future topics such as web application security, penetration testing, vulnerability assessment, and incident response.

---

**Platform:** TryHackMe
**Room:** HTTP in Detail
**Completed:** Day 24–25 of My Cybersecurity Learning Journey
