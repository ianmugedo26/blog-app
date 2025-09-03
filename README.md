# Magenta

A comprehensive full-stack project tutorial built from scratch with **PHP**, **MySQL**, **JavaScript**, **HTML**, and **CSS**—no frameworks, no shortcuts.

---

##  Video Tutorial

Watch the full development process on YouTube (FreeCodeCamp):

::contentReference[oaicite:2]{index=2}


---

##  Features
- Full **CRUD functionality** for managing blog posts
- **User-friendly UI** crafted with vanilla HTML, CSS, and JavaScript
- **Live update effects** using dynamic JS DOM manipulation
- Organized **backend logic** written in clean PHP using MySQLi
- **Secure database interactions** with proper escaping and error handling

---

##  Tech Stack
- **Backend**: PHP (MySQLi)
- **Database**: MySQL
- **Frontend**: HTML, CSS, JavaScript (vanilla)
- **Server**: Apache (via XAMPP or LAMP/WAMP/MAMP)

---

##  File Structure

project-root/
├── index.php # Displays blog posts and triggers modal forms
├── script.php # Contains database connection & CRUD logic
├── postHandler.php # Handles form submissions (Create/Edit/Delete)
├── styles.css # Layout and styles for blog and modal
├── app.js # Controls UI actions and AJAX calls
└── database.sql # SQL to initialize blog posts table


---

##  Setup Instructions

1. Clone or copy the project into your server’s root directory (e.g. `htdocs/` for XAMPP).
2. Import the database schema:
   ```sql
   CREATE DATABASE blog_project;
   USE blog_project;

   CREATE TABLE posts (
     id INT AUTO_INCREMENT PRIMARY KEY,
     title VARCHAR(255) NOT NULL,
     content TEXT NOT NULL,
     created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
   );

  Set up database connection in script.php:
```php
$conn = new mysqli("localhost", "root", "", "blog_project");
if ($conn->connect_error) {
  die("Connection failed: " . $conn->connect_error);
}
```
Launch the application by visiting:

http://localhost/your-project-folder/

## How It Works

- index.php presents the post list and provides UI controls (add/edit/delete).

- JavaScript triggers modals to show forms or delete confirmations.

- CRUD operations are processed by backend PHP and persistently stored in MySQL.

- The UI reflects changes instantly without manual page reloads.

## Enhancements

- Add user authentication and authorization

- Improve UI with modern CSS frameworks

- Implement AJAX endpoints for dynamic CRUD operations

- Add postfix SEO or image upload features

Project by Mugedo Ian. Crafted while following the tutorial to understand the fundamentals of full-stack web development with no dependencies.
