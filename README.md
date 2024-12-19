# FilmCRUD

<img src="./assets/github-banner.png" alt="banner" style="border-radius: 15px;"/>

A web-based movie management system that allows users to Create, Read, Update, and Delete movie entries using PHP and MySQL.

## Technologies Used
- [About](#about)
- [Features](#features)
- [Technologies](#technologies)
- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Usage](#usage)
- [Database Structure](#database-structure)
- [Contributing](#contributing)
- [License](#license)

## Overview
FilmCRUD is a simple yet powerful web application that helps you manage a movie database. With an intuitive interface, users can easily add new movies, view the existing collection, update movie information, and remove entries. Perfect for movie enthusiasts who want to keep track of their film collection.

## Features
- Create new movie entries with details like:
  - Title
  - Release Year
  - Director
  - Genre
  - Duration
  - Synopsis
- List all movies with pagination
- Search movies by title, director, or genre
- Update movie information
- Delete movie entries
- Responsive design for mobile and desktop
- Input validation and sanitization
- User-friendly interface

## Technologies
- PHP 8.0+
- MySQL 5.7+
- HTML5
- CSS3
- JavaScript
- Bootstrap 5
- Apache/Nginx

## Prerequisites
- PHP installed on your server (version 8.0 or higher)
- MySQL server
- Web server (Apache/Nginx)
- Composer (for dependencies)

## Installation
1. Clone the repository:
```bash
git clone https://github.com/juliaboifaciio/FilmCRUD.git
```

2. Navigate to the project directory:
```bash
cd FilmCRUD
```

3. Install dependencies:
```bash
composer install
```

4. Create a MySQL database and import the structure:
```bash
mysql -u your_username -p your_database_name < database/structure.sql
```

5. Configure your database connection:
```bash
cp config/database.example.php config/database.php
```
Then edit `config/database.php` with your database credentials.

6. Configure your web server to point to the `public` directory

## Database Structure
```sql
CREATE TABLE movies (
    id INT PRIMARY KEY AUTO_INCREMENT,
    title VARCHAR(255) NOT NULL,
    release_year INT,
    director VARCHAR(100),
    genre VARCHAR(50),
    duration INT,
    synopsis TEXT,
    created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP,
    updated_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP ON UPDATE CURRENT_TIMESTAMP
);
```

## Usage
1. Access the application through your web browser
2. Use the navigation menu to:
   - View all movies
   - Add a new movie
   - Search for specific movies
3. Click on a movie entry to:
   - View complete details
   - Edit information
   - Delete the entry

## API Endpoints
### Movies
- `GET /api/movies` - List all movies
- `GET /api/movies/{id}` - Get a specific movie
- `POST /api/movies` - Create a new movie
- `PUT /api/movies/{id}` - Update a movie
- `DELETE /api/movies/{id}` - Delete a movie

## License
This project is under the MIT license.

## Author
- **Julia Bonifacio** - [juliabonifaciio](https://github.com/juliabonifaciio)# FilmCRUD
