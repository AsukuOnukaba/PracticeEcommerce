# Practice eCommerce Website

This is a practice eCommerce website built with HTML, CSS, JavaScript, and PHP. The website simulates an online shopping experience, where users can browse products, add items to their shopping cart, and complete a simulated checkout process.

## Features

- **Home Page**: Displays featured products with categories and a navigation menu for other pages.
- **Product Pages**: Shows product details, including images, descriptions, and prices, with an option to add items to the shopping cart.
- **Shopping Cart**: Allows users to view their cart, update quantities, and remove items.
- **User Authentication**: Users can register and log in to manage their accounts and view their order history.
- **Order Processing**: Simulated checkout process to simulate order placement.

## Technologies Used

- **Frontend**:
  - HTML5
  - CSS3
  - JavaScript

- **Backend**:
  - PHP for server-side scripting
  - MySQL for product and user data storage

- **Authentication**:
  - PHP sessions or cookies for user login and registration

## Installation

To run this project locally, follow these steps:

### 1. Clone the repository

```bash
git clone https://github.com/yourusername/ecommerce-practice.git
cd ecommerce-practice
```

### 2. Set up a local server

This project uses PHP, so you'll need a local server environment such as [XAMPP](https://www.apachefriends.org/index.html) or [MAMP](https://www.mamp.info/en/) to run PHP and MySQL.

1. Install XAMPP or MAMP.
2. Start the Apache and MySQL services from the XAMPP or MAMP control panel.
3. Move your project folder into the `htdocs` folder (XAMPP) or the `www` folder (MAMP).

### 3. Set up the database

1. Open phpMyAdmin (http://localhost/phpmyadmin).
2. Create a new database, e.g., `ecommerce_db`.
3. Import the database schema if provided (or manually create tables such as `products`, `users`, `orders`).

### 4. Configure the database connection

In your PHP files (e.g., `db.php`), configure the database connection as follows:

```php
<?php
$host = "localhost"; // or your database server
$dbname = "ecommerce_db"; // the name of your database
$username = "root"; // your database username (usually 'root' for local setups)
$password = ""; // your database password (usually empty for XAMPP/MAMP)
$conn = new mysqli($host, $username, $password, $dbname);

if ($conn->connect_error) {
    die("Connection failed: " . $conn->connect_error);
}
?>
```

### 5. Run the project

1. Open your browser and navigate to `http://localhost/ecommerce-practice` (or the appropriate folder if you renamed it).
2. The website should now be live and ready to use locally.

## Usage

- **Home Page**: View available products and categories.
- **Product Pages**: Click on a product to view more details and add it to the shopping cart.
- **Shopping Cart**: Add, remove, or update quantities of items in your cart.
- **Checkout**: Proceed to the checkout page to simulate placing an order (without real payment integration).
- **User Registration/Login**: Users can create an account and log in to view their order history.

## Project Structure

### Frontend

- `/css` - Contains all CSS stylesheets for the site.
- `/js` - Contains JavaScript files for handling dynamic content and interactivity.
- `/images` - Image folder for product photos and other assets.

### Backend

- `/includes` - Includes for common PHP elements such as header, footer, and database connection.
- `/pages` - PHP pages for displaying the home page, product details, shopping cart, etc.
- `/auth` - PHP scripts for user authentication (e.g., login, registration).

### Database

The database includes tables such as `products`, `users`, and `orders` for handling data related to the website.

## Contributing

1. Fork the repository.
2. Create a new branch (`git checkout -b feature-name`).
3. Commit your changes (`git commit -am 'Add feature'`).
4. Push to your branch (`git push origin feature-name`).
5. Open a Pull Request.

## License

This project is open-source and available under the [MIT License](LICENSE).

## Acknowledgments

- This is a practice project created for learning purposes and is not intended for production use.
- Special thanks to tutorials and resources for PHP and MySQL integration, such as [PHP.net](https://www.php.net/) and [DailyTuition](https://www.youtube.com/@DailyTuition).
