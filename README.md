# Laravel API with Sanctum Authentication

A Laravel 12 backend API with Sanctum authentication for secure API access. This project is a simple API for a web application.

## Prerequisites

-   PHP 8.2 or higher
-   Composer
-   SQLite (comes with PHP)

## Installation

1. **Clone the repository**

    ```bash
    git clone <your-repo-url>
    cd laravel-nuxt-api
    ```

2. **Install PHP dependencies**

    ```bash
    composer install
    ```

3. **Environment setup**

    ```bash
    cp .env.example .env
    php artisan key:generate
    ```

    Make sure `SESSION_DOMAIN` and `SANCTUM_STATEFUL_DOMAINS` are set to your frontend host. Example:

    ```env
    SESSION_DOMAIN=localhost
    SANCTUM_STATEFUL_DOMAINS=localhost:3000,localhost:5000
    ```

4. **Database setup**
    ```bash
    php artisan migrate
    ```

## Running the Application

### Development Mode

Run all services concurrently (Laravel server, queue worker, and logs):

```bash
composer run dev
```

This command will start:

-   Laravel development server on `http://localhost:8000`
-   Queue worker for background jobs
-   Log monitoring

### Alternative: Run services separately

**Backend only:**

```bash
php artisan serve
```
