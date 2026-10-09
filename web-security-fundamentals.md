# Web Security Fundamentals

## 1. Introduction

Web security focuses on protecting websites, web applications, servers, and user data from unauthorized access and attacks.

Cybersecurity professionals study how web applications process requests, manage authentication, store information, and enforce access controls.

## 2. How HTTP Works

HTTP (Hypertext Transfer Protocol) is used for communication between clients and web servers.

A typical request-response cycle:

1. A client sends an HTTP request.
2. The server processes the request.
3. The server returns an HTTP response.
4. The browser displays or processes the response.

Common HTTP methods:

- `GET` — Requests a resource.
- `POST` — Submits data for processing.
- `PUT` — Creates or replaces a resource, depending on the API.
- `DELETE` — Requests deletion of a resource.

## 3. HTTP vs HTTPS

- **HTTP:** Does not provide transport encryption by itself.
- **HTTPS:** Uses TLS to protect data in transit and authenticate the server.

HTTPS does not guarantee that a website is legitimate or free from vulnerabilities.

## 4. Cookies and Sessions

**Cookies** are pieces of data stored by a browser and sent with requests according to their configured scope.

**Sessions** allow an application to maintain state across multiple requests, often using a session identifier.

Security best practices include:

- Set `Secure` on cookies that should only travel over HTTPS.
- Set `HttpOnly` to prevent JavaScript from reading sensitive cookies.
- Use an appropriate `SameSite` setting.
- Regenerate session identifiers after authentication or privilege changes.
- Expire sessions appropriately and invalidate them during logout.

## 5. Common Web Vulnerabilities

### SQL Injection

Occurs when untrusted input changes the structure of a database query.

**Prevention:** Use parameterized queries, avoid unsafe query construction, and restrict database privileges.

### Cross-Site Scripting (XSS)

Occurs when untrusted content is interpreted as executable script in a user's browser.

**Prevention:** Apply context-appropriate output encoding, sanitize HTML where necessary, and use Content Security Policy as an additional defense.

### Broken Access Control

Occurs when users can access resources or perform actions beyond their authorization.

**Prevention:** Enforce authorization on the server for every sensitive operation. Do not rely only on hiding buttons or links in the interface.

### Cross-Site Request Forgery (CSRF)

Can occur when a browser is tricked into submitting an unwanted authenticated request to an application.

**Prevention:** Use appropriate CSRF tokens, cookie settings, and origin checks for relevant requests.

### Security Misconfiguration

Occurs when applications or servers use insecure settings, unnecessary services, exposed debugging features, or improper permissions.

**Prevention:** Use secure defaults, remove unnecessary services, update software, and review configurations.

## 6. Authentication vs Authorization

- **Authentication:** Verifies who a user is.
- **Authorization:** Determines what an authenticated user is allowed to do.

Strong authentication does not replace authorization checks.

## 7. Useful Security Headers

- `Content-Security-Policy` — Restricts permitted sources of content.
- `Strict-Transport-Security` — Tells browsers to use HTTPS for a configured period.
- `X-Content-Type-Options: nosniff` — Helps prevent MIME-type sniffing.
- `Referrer-Policy` — Controls referrer information sent by browsers.

Headers should be configured according to the application's requirements and tested for compatibility.

## 8. Safe Practice

When learning web security, use an intentionally vulnerable training application, a local test application, or a lab where testing is explicitly authorized.

Practice identifying:

- HTTP request methods and response status codes.
- Cookie attributes and session behavior.
- Authentication and authorization boundaries.
- Security headers.
- Input validation and output encoding.

Never test a website without permission.

## 9. Key Takeaways

- HTTP defines request-response communication.
- HTTPS protects data in transit but does not guarantee application security.
- Cookies and sessions require secure configuration.
- SQL injection, XSS, CSRF, and broken access control have different causes and defenses.
- Authentication and authorization solve different problems.
- Secure coding, testing, and configuration reduce web application risk.

## Learning Progress

**Status:** Web security fundamentals notes drafted.

**Next goal:** Study HTTP requests and responses in an authorized practice environment and record original observations.

---

*Original educational study notes. This document is not a walkthrough of a specific TryHackMe room.*
