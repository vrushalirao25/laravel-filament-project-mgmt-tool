# Project Management Tool

A comprehensive project management system built with Laravel, Livewire, and Filament that features Kanban-style board views with customizable workflow stages, robust issue tracking, and advanced state management.

## Features

- **Modern Architecture**
  - Service-oriented design with dedicated business logic layers
  - State pattern implementation for issue statuses
  - Form request validation with specialized rules

- **Robust Issue Tracking**
  - Custom field support for different issue types using enums
  - Rich text editing for detailed issue descriptions
  - File attachment capabilities with MIME validation
  - Granular component-based updates using Livewire

- **Reactive UI Components**
  - Real-time form validation with Livewire
  - Component isolation for optimized re-rendering
  - Granular UI updates without full page reloads

- **Advanced File Handling**
  - Secure file uploads with validation
  - Comprehensive file metadata tracking
  - Storage abstraction for flexible deployment options

- **Role-Based Access Control**
  - Project-specific user roles and permissions
  - Context-aware UI elements based on user capabilities

## Tech Stack

- **Backend**: Laravel 10.x with advanced patterns (Services, States, Enums)
- **Frontend Interactivity**: Livewire 3.x with isolated components
- **Admin Panel**: Filament 3.x with custom resources and widgets
- **Database**: MySQL with optimized relationships
- **Styling**: Tailwind CSS for responsive design

## Installation

### Prerequisites
- PHP 8.1+
- Composer
- Node.js & NPM
- MySQL

### Setup Instructions

1. Clone the repository
```bash

git clone https://github.com/vrushalirao25/laravel-filament-project-mgmt-tool.git
cd laravel-filament-project-mgmt-tool
```

2. Install PHP dependencies
```bash
composer install
```

3. Install NPM dependencies
```bash
npm install
```

4. Create environment file
```bash
cp .env.example .env
```

5. Configure your database in the `.env` file
```
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=task-mgmt
DB_USERNAME=root
DB_PASSWORD=
```

6. Generate application key
```bash
php artisan key:generate
```

7. Run migrations and seed the database
```bash
php artisan migrate --seed
```

8. Build assets
```bash
npm run dev
```

9. Start the development server
```bash
php artisan serve
```

10. Access the application at `http://localhost:8000`

## Project Structure

```
app/
├── Http/
│   ├── Controllers/
│   │   └── IssueController.php       # RESTful controller for issues
│   └── Requests/
│       ├── CreateIssueRequest.php    # Form validation for issue creation
│       └── UpdateIssueRequest.php    # Form validation for issue updates
├── Livewire/
│   └── Issue/
│       ├── CreateIssue.php           # Reactive issue creation component
│       ├── ViewIssue.php             # Issue viewing component
│       ├── EditIssueDescription.php  # Isolated description editing
│       └── EditIssuePriority.php     # Enum-based priority selector
├── Models/
│   ├── Issue.php                     # Issue model with relationships
│   ├── Project.php                   # Project model and relationship definitions
│   ├── IssueFile.php                 # File attachment model
│   └── User.php                      # Extended user model with permissions
├── Services/
│   ├── IssueService.php              # Business logic for issue operations
│   └── FileService.php               # File handling operations
├── States/
│   └── IssueStatus/
│       ├── IssueStatus.php           # Base status class
│       ├── Backlog.php               # Backlog state implementation
│       ├── InProgress.php            # In progress state implementation
│       └── ...                       # Additional status states
└── Enums/
    ├── IssuePriority.php             # Priority enum with helper methods
    └── IssueType.php                 # Issue type definitions
```

This structure demonstrates clean separation of concerns, with dedicated layers for controllers, services, models, and UI components.

## Implementation Details

### Architecture Highlights

The project implements several advanced Laravel patterns:

- **Service Layer Pattern**: Encapsulating business logic in dedicated service classes (e.g., `IssueService`) to maintain clean controllers and improve testability.
- **State Pattern**: Managing issue status transitions through dedicated state classes with proper validation and business rules.
- **Repository Pattern**: Abstracting data access through specialized repositories (optional implementation).
- **Form Request Validation**: Using dedicated request classes to encapsulate validation logic outside controllers.

### Livewire Components

The project leverages Livewire for reactive UI updates without page refreshes:

- `CreateIssue.php` - Implements real-time validation and sophisticated form handling with file uploads
- `ViewIssue.php` - Handles contextual display based on user permissions and view type
- `EditIssueDescription.php` - Demonstrates isolated component updates for inline editing
- `EditIssuePriority.php` - Shows enum integration with dropdown interfaces

### State Management

Advanced state transition system for issues:

- State classes to encapsulate status-specific behavior
- Valid transition rules enforced at the model level
- UI adapting to available state transitions

## Development Approach

This project was developed following these principles:

1. **Component-Based Architecture**: Breaking UI into reusable, isolated Livewire components
2. **Domain-Driven Design**: Organizing code around business domains and concepts
3. **Progressive Enhancement**: Core functionality works without JS, enhanced with Livewire
4. **SOLID Principles**: Following software design principles for maintainable code


