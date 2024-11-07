Inventory Management System
A basic Inventory Management System built with Laravel 11.x that demonstrates core concepts of MVC architecture, routing, middleware, and deployment with Podman.

Features
Create, update, and delete inventory items (including name, category, quantity, and price)
View inventory items in a structured format
Requirements
PHP >= 8.0
Composer
MySQL
Podman
Setup
1. Clone and Install Dependencies
bash
Copy code
git clone https://github.com/yourusername/inventory-management.git
cd inventory-management
composer install
2. Configure Environment
Copy the environment file and configure your settings:

bash
Copy code
cp .env.example .env
Set up your database credentials in the .env file:

plaintext
Copy code
DB_CONNECTION=mysql
DB_DATABASE=inventory_management
DB_USERNAME=your_username
DB_PASSWORD=your_password
Generate the application key:

bash
Copy code
php artisan key:generate
3. Migrate Database
Run migrations to create database tables:

bash
Copy code
php artisan migrate
4. Run the Application
To start the server locally:

bash
Copy code
php artisan serve
Or, to deploy with Podman, create a Dockerfile and podman-compose.yml file.

Build and run containers:

bash
Copy code
podman-compose up -d
Access the application at http://localhost:8000.

Folder Structure
app/Models/Inventory.php - Model for inventory items
app/Http/Controllers/InventoryController.php - Controller for CRUD operations
resources/views/inventory - Blade templates for UI
routes/web.php - Application routes
License
This project is licensed under the MIT License.
