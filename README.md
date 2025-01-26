# software-lab

this is my third semester practical.

# Createing laravel

Creating a project using PHP Laravel can be an exciting and rewarding experience! Laravel is a powerful and elegant PHP framework that simplifies many common tasks in web development. Here's a step-by-step guide to get you started:

Step 1: Install Laravel
First, ensure you have Composer installed on your machine. Composer is a dependency manager for PHP.

_composer global require laravel/installer_

Step 2: Create a New Laravel Project
Use the Laravel installer to create a new project. Replace project-name with your desired project name.

_laravel new project-name_

Alternatively, you can use Composer to create a new Laravel project:

_composer create-project --prefer-dist laravel/laravel project-name_

Step 3: Set Up Environment Configuration
Navigate to your project directory and set up your environment configuration. Copy the .env.example file to .env:

_cd project-name&_
_cp .env.example .env_

Generate an application key:

_php artisan key:generate_

Step 4: Configure Database
Open the .env file and configure your database settings. For example:

DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=your_database_name
DB_USERNAME=your_database_user
DB_PASSWORD=your_database_password

Step 5: Run Migrations
Laravel uses migrations to manage database schema. Run the following command to create the necessary tables:

_php artisan migrate_

Step 6: Serve Your Application
You can serve your Laravel application using the built-in PHP development server:

_php artisan serve_

Your application will be accessible at http://localhost:8000.

Step 7: Create a Basic Route and Controller
Create a new controller:

_php artisan make:controller HomeController_

Open routes/web.php and add a route:

_Route::get('/', [HomeController::class, 'index']);_

In app/Http/Controllers/HomeController.php, add the index method:

---

namespace App\Http\Controllers;

use Illuminate\Http\Request;

class HomeController extends Controller
{
public function index()
{
return view('welcome');
}
}

---

Step 8: Create a View
Create a new view file in resources/views/welcome.blade.php:

---

<!DOCTYPE html>
<html>
<head>
    <title>Laravel Project</title>
</head>
<body>
    <h1>Welcome to My Laravel Project!</h1>
</body>
</html>
---
