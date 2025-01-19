# My PHP CRUD Application

This is my simple PHP CRUD application. It allows to manage user data with basic operations.

## Folder Structure

- `index.php`- the main entry point.
- `read.php`- displays the list of users.
- `update.php`- updates user information.
- `php/`- contains the backend PHP scripts for CRUD operations.
    - `create.php`- Handles the creation of new users.
    - `read.php`- gets and displays user data.
    - `update.php`- handles updating user information.
    - `delete.php`- handles deleting users.
- `css/`- It has the css style.
    - `style.css`-  Style for the application.
- `db_conn.php`- database connection script.

## How to Use

1. **Clone the repository:**
     cd PHP-CRUD-Operation

2. **Set up the database:**
     - Create a database named `my_db`.
     - Create a table named `users` with the following structure:
         ```sql
         CREATE TABLE users (
             id INT AUTO_INCREMENT PRIMARY KEY,
             name VARCHAR(255) NOT NULL,
             email VARCHAR(255) NOT NULL
         );
         ```

3. **Configure the database connection:**
     - Update the `db_conn.php` file with your database credentials:
         ```php
         $sname = "localhost";
         $uname = "root";
         $password = "";
         $db_name = "my_db";
         ```

4. **Run the application:**
     - Start your local server (e.g., XAMPP, WAMP).
     - Open your browser and navigate to `http://localhost/php-crud-main/index.php`.


