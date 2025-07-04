Here is a simple system design for an extremely simple task management app based on your requirements and preferred stack (JavaScript, jQuery, PHP, MariaDB/MySQL):

## System Design Overview

### 1. Architecture
- **Client-side:** HTML + CSS + JavaScript + jQuery for UI interactions and AJAX calls.
- **Server-side:** PHP scripts handling authentication, session management, and CRUD operations.
- **Database:** MariaDB/MySQL to store users and tasks.

---

### 2. Database Design

Two main tables:

- **users**
  - `id` INT AUTO_INCREMENT PRIMARY KEY
  - `username` VARCHAR(50) UNIQUE NOT NULL
  - `password` VARCHAR(255) NOT NULL (store hashed passwords)
  - `name` VARCHAR(100) (optional)

- **tasks**
  - `id` INT AUTO_INCREMENT PRIMARY KEY
  - `user_id` INT NOT NULL (foreign key to users.id)
  - `title` VARCHAR(255) NOT NULL
  - `description` TEXT (optional)
  - `status` ENUM('pending', 'in progress', 'completed') DEFAULT 'pending'
  - `created_at` TIMESTAMP DEFAULT CURRENT_TIMESTAMP
  - `updated_at` TIMESTAMP DEFAULT CURRENT_TIMESTAMP ON UPDATE CURRENT_TIMESTAMP

---

### 3. Authentication & Security

- Use PHP sessions to manage logged-in state (`session_start()`, store user ID in `$_SESSION`).
- Passwords hashed with `password_hash()` and verified with `password_verify()` in PHP.
- Use prepared statements (mysqli or PDO) for all database queries to prevent SQL injection.
- Validate and sanitize all user inputs on server-side (e.g., using `filter_var()` and escaping output with `htmlspecialchars()`).
- Implement login, logout, and registration pages.
- Redirect logged-in users away from login/register pages.
- Use HTTPS to secure data in transit (requires server config, outside app code).
- Set secure, HttpOnly cookies for sessions.
- Limit error messages on login failures to generic messages to avoid information disclosure.

---

### 4. Application Flow

**User Authentication:**
- Registration page: User signs up with username and password; password is hashed and stored.
- Login page: User submits credentials; PHP verifies and sets session variables.
- Logout page: Destroys session and redirects to login.

**Task CRUD Operations:**
- After login, user sees a dashboard listing their tasks.
- User can create a new task via a form.
- Tasks can be edited or deleted.
- Use AJAX calls with jQuery to perform CRUD without full page reloads.
- Server-side PHP scripts handle CRUD requests, validate session, and operate on the database.

---

### 5. Example File Structure

```
/app
  /css
    styles.css
  /js
    app.js (jQuery AJAX calls)
  /php
    database_connection.php  (connects to MariaDB)
    register.php
    login.php
    logout.php
    authenticate.php (handles login POST)
    tasks_crud.php (handles AJAX CRUD operations)
  index.php (dashboard, shows tasks)
```

---

### 6. Key Implementation Details

**database_connection.php**
- Use mysqli with error reporting and exceptions enabled.
- Central place to include in all PHP scripts needing DB.

**Authentication (login.php & authenticate.php)**
- On POST, check username/password using prepared statements.
- If success, set session variables (`$_SESSION['user_id']`, `$_SESSION['username']`).
- Redirect to index.php (dashboard).
- If failure, show generic error message.

**Session Protection**
- On all pages except login/register, check if `$_SESSION['user_id']` is set.
- If not, redirect to login.

**CRUD Operations (tasks_crud.php)**
- Accept AJAX requests for create, read, update, delete.
- Verify session user_id matches task user_id for update/delete.
- Use prepared statements for all queries.
- Return JSON responses for success/error.

**Client-side (app.js)**
- Use jQuery AJAX to call PHP endpoints for CRUD.
- Update UI dynamically without page reload.

---

### 7. Basic Security Protocols

- Use HTTPS.
- Use prepared statements to prevent SQL injection.
- Sanitize and validate all user inputs.
- Hash passwords securely.
- Use session management best practices.
- Limit error messages.
- Escape output to prevent XSS.
- Set secure cookie flags.

---

### Summary

This design provides a minimal but secure task management app with:

- User registration, login, logout with secure authentication.
- CRUD operations on tasks linked to authenticated users.
- PHP backend with prepared statements and password hashing.
- MariaDB/MySQL database.
- jQuery AJAX frontend for smooth user experience.
- Basic security best practices implemented.

This approach is simple yet robust enough for a basic task management application using your specified technologies[1][2][3][4][6].

If you want, I can also provide example code snippets for key parts like authentication or CRUD operations.

[1] http://www.hashbangcode.com/article/creating-authentication-system-php-and-mariadb
[2] https://wpwebinfotech.com/blog/php-security/
[3] https://phppot.com/php/user-authentication-using-php-and-mysql/
[4] https://tutorialrays.in/php-mysql-register-and-login-logout-with-dashbaord-page-authenticated/
[5] https://www.youtube.com/watch?v=HMuThowRpeQ
[6] https://www.itsolutionstuff.com/post/simple-php-jquery-ajax-crudinsert-update-delete-tutorial-example-with-source-codeexample.html
[7] https://www.vaadata.com/blog/php-security-best-practices-vulnerabilities-and-attacks/
[8] https://github.com/vijaythapa333/task-manager
[9] https://github.com/Ankurac7/TaskEase
[10] https://satoricyber.com/mysql-security/mariadb-security-threats-and-best-practices/
[11] https://www.sourcecodester.com/php/15624/simple-task-managing-system-php-mysqli-free-source-code.html
[12] https://codeshack.io/secure-login-system-php-mysql/
[13] https://codewithawa.com/posts/to-do-list-application-using-php-and-mysql-database
[14] https://mariadb.com/kb/en/securing-connections-for-client-and-server/
[15] https://dev.to/ettalibi02assia/building-a-secured-user-authentication-system-with-php-mysql-pdo-and-hashed-password-4mpj
[16] https://www.sourcecodester.com/php/17217/employee-management-system-php-and-mysql-free-download.html
[17] https://www.bocasay.com/best-security-practices-php-applications/
[18] https://phpgurukul.com/employee-task-management-system-using-php-and-mysql/
[19] https://www.youtube.com/watch?v=Y0qjUBVkk1E
[20] https://www.jeasyui.com/tutorial/app/crud.php