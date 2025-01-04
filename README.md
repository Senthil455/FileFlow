# FileFlow

## About FileFlow

FileFlow is a full-stack Single Page Application (SPA) built for educational and demonstrational purposes.

It simulates hierarchical file system management and implements a file browser with a tree structure, allowing users to manage files and folders directly in the browser through an intuitive interface. The application mimics traditional file system functionality while leveraging modern web technologies to deliver a responsive, interactive experience with full CRUD (Create, Read, Update, Delete) operations, validation, sorting, and hierarchical organization.

Based on tech stack:

- HTML
- PHP
- Laravel
- Jetstream
- Sanctum
- Inertia
- MySQL
- JavaScript
- Vue
- Pinia
- Axios
- CSS
- Tailwind CSS
- Docker
- Sail

## Key Features

### Hierarchical File Management

- Tree Structure Navigation: Visual folder hierarchy with expandable/collapsible nodes
- Visual Selection: Highlighting of selected files/folders across components
- Parent-Child Relationships: Nested folder structure with proper relationship management
- Real-time Updates: Instant reflection of changes across the file tree

### Full CRUD Operations

- Folder Management: Create, rename, and delete folders
- File Operations: Create, edit content, rename, and delete files
- Recursive Operations: Automatic handling of nested content during deletions

### File System Analytics

- Size Calculation: Automatic computation of folder sizes including all nested content
- Metadata Tracking: File counts, folder counts, and storage statistics
- Format Conversion: Human-readable byte formatting (KB, MB, GB, etc.)

### Security & Authentication

- User Authentication: Registration, login, and session management
- Protected Routes: API endpoints secured with Laravel Sanctum
- Profile Management: User settings, password updates, and two-factor authentication

### Real-time Interactions

- Live Editing: In-browser file content editing with instant save
- Dynamic Updates: Automatic UI updates without page reloads
- Form Validation: Client-side and server-side validation with error display

### State Management

- Centralized Store: Pinia-based state management for file system data
- Reactive Components: Vue.js Composition API with reactive data flow
- API Integration: Axios-based communication with Laravel backend

### Modern Technology Stack and User Interface

- Laravel Backend: Robust API with RESTful endpoints
- Vue.js Frontend: Component-based architecture with Composition API
- Inertia.js: Seamless SPA experience without building a separate API client
- Tailwind CSS: Utility-first styling for consistent design
- Responsive Design: Adaptive interface for desktop, tablet, and mobile devices
- Dual Theme Support: Light and dark modes with persistent user preferences

## Getting Started

- Clone the repository:

```bash
git clone [repository-url]
```

- Change directory to project:

```bash
cd FileFlow
```

- Install php dependencies:

```bash
composer install
```

- Create .env file:

```bash
cp .env.example .env
```

- Generate application key:

```bash
php artisan key:generate
```

- Run Docker Desktop (with wsl - for Windows only)

- Run wsl (for Windows only):

```bash
wsl
```

- Run Sail:

```bash
./vendor/bin/sail up
```

- Add new tab in terminal and connect to container:

```bash
docker exec -it fileflow-laravel.test-1 bash
```

- Install php dependencies (optional, if missing some required php extension in base system):

```bash
composer install
```

- Run migrations:

```bash
php artisan migrate
```

- Install node dependencies:

```bash
npm install
```

- Build project:

```bash
npm run build
```

- In browser go to the welcome page at the local application URL

- Register a new user on the registration page (enter your name, email, password)

- Or you can seed the database with random users (name, email: random - look in database, password: password), folders and files:

```bash
php artisan migrate:fresh --seed
```

- Log in on the login page

That's it! Thank you!

## ⭐ If You Found This Useful

If this project helped you - whether it saved you time, taught you something, or gave you an idea - please consider leaving a star or a like.

A ⭐, 👍, ❤️, or 💎 tells me that the work matters. It's a small gesture that genuinely fuels my motivation to keep improving the project and building new tools.

Thanks for your interest in this project!

## License

FileFlow is open-sourced software licensed under the MIT license. See the LICENSE file for details.

## Third-Party Licenses

This project uses third-party software components. Their respective licenses can be found in the LICENSE-3rd-party.md file.
