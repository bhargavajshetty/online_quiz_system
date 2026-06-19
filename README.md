# Online Quiz System

A full-stack web-based quiz platform built with PHP and MySQL, featuring user authentication, timed quizzes, automatic scoring, and an admin dashboard for managing questions and results.

## Features

- **User Authentication** — Secure registration and login system with hashed password storage
- **Quiz Participation** — Users can take quizzes with automatic score calculation upon submission
- **Results Tracking** — View quiz results and track performance after each attempt
- **Admin Dashboard** — Dedicated admin interface to manage quiz content
- **Question Management** — Add and edit quiz questions through the admin panel
- **Role-Based Access** — Separate flows and permissions for regular users and administrators
- **Responsive Design** — Clean, accessible UI styled with custom CSS

## Tech Stack

- **Backend:** PHP
- **Database:** MySQL
- **Frontend:** HTML, CSS
- **Local Environment:** XAMPP (Apache + MySQL)

## Project Structure

```
.
├── index.php                  # Landing/home page
├── register.php               # User registration
├── login.php                  # User login
├── logout.php                 # Session termination
├── dashboard.php               # User dashboard after login
├── quiz.php                   # Quiz-taking interface
├── result.php                  # Displays quiz results after submission
├── admin_dashboard.php          # Admin panel landing page
├── add_question.php            # Admin: add new quiz questions
├── edit_questions.php          # Admin: edit/update existing questions
├── hash_admin_password.php      # Utility script for hashing admin credentials
├── db.php                      # Database connection configuration
└── styles.css                  # Application styling
```

## How It Works

1. **Registration & Login** — New users sign up via `register.php`; credentials are validated and securely stored. Returning users authenticate through `login.php`.
2. **Taking a Quiz** — Once logged in, users are directed to `dashboard.php`, where they can start a quiz via `quiz.php`. Questions are pulled from the database and presented with a scoring mechanism that runs on submission.
3. **Viewing Results** — After completing a quiz, `result.php` calculates and displays the user's score.
4. **Admin Management** — Administrators access `admin_dashboard.php` to manage the question bank, using `add_question.php` to create new questions and `edit_questions.php` to update existing ones.
5. **Security** — Admin credentials are hashed using `hash_admin_password.php` rather than stored in plaintext, and all dynamic content is served through parameterized database queries via `db.php`.

## Setup & Installation

1. Install [XAMPP](https://www.apachefriends.org/) (or any Apache + PHP + MySQL stack).
2. Clone this repository into your `htdocs` folder:
   ```bash
   git clone https://github.com/bhargavajshetty/online_quiz_system.git
   ```
3. Start Apache and MySQL from the XAMPP control panel.
4. Create a MySQL database and import the schema (update `db.php` with your database name, host, username, and password).
5. Visit `http://localhost/online_quiz_system/index.php` in your browser to launch the application.

## Future Improvements

- Add quiz timer functionality with auto-submission on timeout
- Support multiple quiz categories and difficulty levels
- Add a leaderboard to display top scores across users
- Migrate raw SQL queries to prepared statements throughout for stronger SQL injection protection

## Author

**Bhargava J Shetty**
[GitHub](https://github.com/bhargavajshetty) · [LinkedIn](https://linkedin.com/in/bhargava-j-shetty)
