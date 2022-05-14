# Laravel

![laravel](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSy8NmBAIXPQ_NZHWBwPkg4InkyUXTUHrN4kPswb673Agg3rR7SJ-EqZS3L9lFRXd0-XgI&usqp=CAU)

# What is Laravel

- Laravel is a free, open-source PHP web framework, created on 2011 by Taylor Otwell and intended for the development of web applications following the model–view–controller architectural pattern and based on Symfony
- Laravel is a web application framework with expressive, elegant syntax. We’ve already laid the foundation — freeing you to create without sweating the small things.

# Requirement

- php (php 8 For laravel 9)
- xampp, mamp or wamp
- composer
- php extensions

# Create Project

```
composer create-project laravel/laravel projectName
// with spesific version :
composer create-project laravel/laravel="8.*.*" projectName
```

# Project Structure

...

# Routing

- return view

  ```
  use Illuminate\Support\Facades\Route;

  Route::get("/contact", function(){
    return view("contact", [data]);
  })
  OR
  Route::view("/contact", "contact", [data])
  ```

- return method from controller

  ```
  use App\Http\Controllers\TicketController;

  Route::get("/ticket", [TicketController::class, 'show']);
  ```

# MVC

MVC (Model-View-Controller) is a pattern in software design commonly used to implement user interfaces, data, and controlling logic. It emphasizes a separation between the software's business logic and display. This "separation of concerns" provides for a better division of labor and improved maintenance.

- Model: Manages data and business logic.
- View: Handles layout and display.
- Controller: Routes commands to the model and view parts.

# Create a Model

```
php artisan make:model Name
```

# Create a Controller

```
php artisan make:controller Name
```

# Seeder

seeder a tool to include dummy data to the database automatically

- in the factory : \App\Models\User::factory(10)->create();
- in the terminal :
  ```
  php artisan db:seed
  ```

# Create a View

- View is created manualy in the view folder

# FST Steps

- Create databse in php myadmin

- Edit databse name in .env file

- Routing Controller : in "routes/web.php"

  ```
  Route::get('/url', [controllerName::class, 'method']);
  Route::get('Url','PageName');
  ```

- Create Controller

  ```
  php artisan make:controller CarController -r // with resources
  ```

- nameSpace => right click to import name class name space

- Create view in "resources/views/Cars/index.blade.php"

- Return the view in the controller index method

  ```
  public function index()
  {
  return view("cars/index");
  }
  ```

- Create migration

  ```
  php artisan make:migration create_cars_table
  ```

- Execute the migartion

  ```
  php artisan migrate
  ```

- Create Model

  ```
  php artisan make:model Car
  ```

- Crate Factory

  ```
  php artisan make:factory CarFactory
  ```

- Generate Fake Data

  ```
  php artisan tinker
  >> App\Models\Car::factory(100)->create();
  ```

- add new column to the migration

  ```
  php artisan make:migration add_brand_to_cars
  ```

- Create model, factory, controller and migration

  ```
  php artisan make:model Driver -a
  ```

- Route List

  ```
  php artisan route:list
  ```

- Create Route With ALl methods (create, show, update, destroy, edit)

  ```
  Route::resource('/drivers', DriverController::class);
  ```

- Create model with migration

  ```
  php artisan make:model Product -m
  ```

- Create Controller for API

  ```
  php artisan make:controller API/ProductController -r --api
  ```

- Create Controller related with the model

  ```
  php artisan make:controller API/ProductController -r --api -m Product
  ```
