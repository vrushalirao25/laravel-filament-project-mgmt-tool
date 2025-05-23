# Project Management System (Laravel, Livewire, Filament)

This project provides a comprehensive and intuitive project management system built using the robust Laravel framework, the reactive Livewire library for dynamic interfaces, and the elegant Filament admin panel for efficient backend management. It offers a range of features designed to streamline project workflows, enhance team collaboration, and improve overall project visibility.

##  Tech Stack

* **Backend:** Laravel 11
* **Admin Panel:** Filament 3
* **Frontend Interactivity:** Livewire
* **Styling:** Tailwind CSS
* **Styling:** Tailwind CSS

### Installation Steps

1.  **Clone the repository:**
    ```bash
    git clone https://github.com/vrushalirao25/laravel-filament-project-mgmt-tool.git
    cd laravel-filament-project-mgmt-tool
    ```

2.  **Install Composer dependencies:**
    ```bash
    composer install
    npm install
    ```

3.  **Copy the `.env.example` file to `.env` and configure your database connection:**
    ```bash
    cp .env.example .env
    # Edit the .env file with your database credentials
    # DB_CONNECTION=mysql
    # DB_HOST=127.0.0.1
    # DB_PORT=3306
    # DB_DATABASE=task-mgmt
    # DB_USERNAME=root
    # DB_PASSWORD=your_password_here
    ```

4.  **Generate an application key:**
    ```bash
    php artisan key:generate
    ```

5.  **Run database migrations:**
    ```bash
    php artisan migrate --seed 
    ```

6.  **Install frontend dependencies and build assets:**
    ```bash
    npm install # or yarn install
    npm run dev # or yarn run dev
    ```

7.  **Serve the application:**
    ```bash
    php artisan serve
    ```

    This will typically start the development server at `http://127.0.0.1:8000`.
