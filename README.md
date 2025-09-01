# EngBoost Academy E-Learning System

A comprehensive web-based e-learning platform designed to facilitate online education by connecting students and teachers through an intuitive interface for learning management and assessment.

## Overview

EngBoost Academy is a full-featured e-learning system that enables:

-   **Students**: View lessons, complete exercises, and track learning progress
-   **Teachers**: Create, edit, and publish quizzes and educational content
-   **Administrators**: Manage users and oversee platform operations

## Features

### For Students

-   Access enrolled courses and lessons
-   Complete interactive exercises and quizzes
-   Track learning progress and scores
-   User-friendly dashboard for course navigation

### For Teachers

-   Create and manage educational content
-   Design and publish quizzes with various question types
-   Monitor student progress and performance
-   Edit and update existing lessons and exercises

### System Features

-   Secure user authentication and authorization
-   Responsive web design for desktop and mobile devices
-   Database-driven content management
-   Google reCAPTCHA integration for enhanced security

## Technology Stack

-   **Frontend**: HTML5, CSS3, JavaScript
-   **Backend**: PHP
-   **Database**: MySQL/MariaDB
-   **Security**: Google reCAPTCHA v2/v3
-   **Server**: Apache/Nginx compatible

## Installation

### Prerequisites

-   Web server (Apache/Nginx)
-   PHP 7.4 or higher
-   MySQL 5.7 or MariaDB 10.2+
-   Google reCAPTCHA API keys

### Setup Instructions

1. **Clone the repository**

git clone <repository-url>
cd engboost-academy

2. **Database Setup**

-   Create a new MySQL database
-   Import the provided database structure:
    ```
    mysql -u username -p database_name < database.sql
    ```

3. **Configure Environment Variables**

-   Copy `.env.example` to `.env`
-   Update the following configurations:

    ```
    # Database Configuration
    DB_HOST=localhost
    DB_NAME=your_database_name
    DB_USER=your_username
    DB_PASS=your_password

    # Google reCAPTCHA
    RECAPTCHA_SITE_KEY=your_site_key
    RECAPTCHA_SECRET_KEY=your_secret_key
    ```

4. **Google reCAPTCHA Setup**

-   Visit [Google reCAPTCHA](https://www.google.com/recaptcha/)
-   Register your domain and get Site Key and Secret Key
-   Add the keys to your `.env` file

5. **Set Permissions**

chmod 755 /path/to/your/project
chmod 644 .env

6. **Configure Web Server**

-   Point your web server document root to the project directory
-   Ensure PHP is properly configured
-   Enable necessary PHP extensions (mysqli, pdo, etc.)

## Usage

### Getting Started

1. **Access the Platform**

-   Navigate to your domain in a web browser
-   Register as a new user or login with existing credentials

2. **For Students**

-   Browse available courses
-   Enroll in desired courses
-   Complete lessons and exercises
-   View progress and grades

3. **For Teachers**

-   Access the teacher dashboard
-   Create new lessons and quizzes
-   Manage existing content
-   Monitor student performance

### User Roles

-   **Student**: Can enroll in courses, view content, and complete assessments
-   **Teacher**: Can create and manage educational content and assessments
-   **Admin**: Has full system access and user management capabilities

## File Structure

```
engboost-academy/
│
├── assets/
│ ├── css/
│ ├── js/
│ └── images/
│
├── includes/
│ ├── config.php
│ └── functions.php
│
├── pages/
│ ├── student/
│ ├── teacher/
│ └── admin/
│
├── database.sql
├── .env.example
├── index.php
└── README.md
```

## Configuration

### Environment Variables

The `.env` file should contain:

-   Database connection details
-   Google reCAPTCHA keys
-   Application-specific settings
-   Security configurations

### Security Considerations

-   Keep `.env` file secure and never commit it to version control
-   Regularly update Google reCAPTCHA keys
-   Implement proper input validation and sanitization
-   Use HTTPS in production environments

## Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/new-feature`)
3. Commit your changes (`git commit -am 'Add new feature'`)
4. Push to the branch (`git push origin feature/new-feature`)
5. Create a Pull Request

## Troubleshooting

### Common Issues

-   **Database Connection Error**: Verify database credentials in `.env`
-   **reCAPTCHA Not Working**: Check API keys and domain configuration
-   **Permission Denied**: Ensure proper file permissions are set
-   **PHP Errors**: Check PHP version compatibility and enabled extensions

## Support

For technical support or questions:

-   Create an issue in the repository
-   Contact the development team
-   Check the documentation for common solutions

## License

- Copyright © 2025 EngBoost Academy
- This project is made available for educational purposes only. While the source code is publicly viewable for learning and reference, all rights are reserved.

## Acknowledgments

-   Google reCAPTCHA for security features
-   Open source PHP community
-   Contributors and beta testers
