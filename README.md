# ApnaMakan

ApnaMakan is an Angular-based web application designed to help manage household tasks and information for a shared living situation. It includes features for managing bills, groceries, food preparation, waste management, and house information, such as utility consumer numbers.

## Table of Contents

- [Features](#features)
- [Folder Structure](#folder-structure)
- [Installation](#installation)
- [Running the App](#running-the-app)
- [Build](#build)
- [Contributing](#contributing)
- [License](#license)

## Features

- **User Authentication**: Secure login and signup.
- **Bill Management**: Track and manage household bills.
- **Grocery Management**: Manage grocery lists and items.
- **Food Preparation**: Plan and manage meal preparation.
- **Waste Management**: Schedule and manage waste disposal.
- **House Information**: Store and access important house details like address and utility consumer numbers.

## Folder Structure

The project structure is organized as follows:

```
/ghar-manage
│
├── /e2e                      # End-to-end tests
│   ├── /src
│   │   ├── app.e2e-spec.ts   # End-to-end test specs
│   │   ├── app.po.ts         # Page objects for end-to-end tests
│   └── tsconfig.json         # TypeScript configuration for e2e
│
├── /node_modules             # Installed dependencies
│
├── /src                      # Source code
│   ├── /app
│   │   ├── /core             # Core module for singleton services
│   │   │   ├── /services     # Core services (e.g., Auth, API)
│   │   │   ├── /guards       # Route guards
│   │   │   ├── /interceptors # HTTP interceptors
│   │   │   ├── /models       # Data models and interfaces
│   │   │   ├── core.module.ts
│   │   │   ├── index.ts
│   │   │   └── app-config.ts # Configuration settings
│   │   │
│   │   ├── /shared           # Shared module for reusable components, directives, pipes
│   │   │   ├── /components   # Shared components (e.g., navbar, footer)
│   │   │   ├── /directives   # Custom directives
│   │   │   ├── /pipes        # Custom pipes
│   │   │   ├── /utilities    # Utility functions and constants
│   │   │   ├── shared.module.ts
│   │   │   ├── index.ts
│   │   │   └── material.module.ts # Angular Material components
│   │   │
│   │   ├── /features         # Feature modules (lazy-loaded)
│   │   │   ├── /home         # Home feature module
│   │   │   │   ├── /components
│   │   │   │   ├── /services
│   │   │   │   ├── home.component.ts
│   │   │   │   ├── home.module.ts
│   │   │   │   └── home-routing.module.ts
│   │   │   ├── /bills        # Bills management module
│   │   │   │   ├── /components
│   │   │   │   ├── /services
│   │   │   │   ├── bills.component.ts
│   │   │   │   ├── bills.module.ts
│   │   │   │   └── bills-routing.module.ts
│   │   │   ├── /grocery      # Grocery management module
│   │   │   │   ├── /components
│   │   │   │   ├── /services
│   │   │   │   ├── grocery.component.ts
│   │   │   │   ├── grocery.module.ts
│   │   │   │   └── grocery-routing.module.ts
│   │   │   ├── /waste        # Waste management module
│   │   │   │   ├── /components
│   │   │   │   ├── /services
│   │   │   │   ├── waste.component.ts
│   │   │   │   ├── waste.module.ts
│   │   │   │   └── waste-routing.module.ts
│   │   │   ├── /house-info   # House information module
│   │   │   │   ├── /components
│   │   │   │   ├── /services
│   │   │   │   ├── house-info.component.ts
│   │   │   │   ├── house-info.module.ts
│   │   │   │   └── house-info-routing.module.ts
│   │   │   ├── /shared       # Shared feature-specific components and services
│   │   │   │   ├── feature-shared.module.ts
│   │   │   │   ├── index.ts
│   │   │   │   └── ...
│   │   │   ├── features.module.ts # Main features module
│   │   │   ├── features-routing.module.ts
│   │   │   └── index.ts
│   │   │
│   │   ├── /assets           # Static assets like images, fonts, etc.
│   │   │   ├── /images       # Images and icons
│   │   │   ├── /styles       # Global styles (e.g., SCSS files)
│   │   │   └── /fonts        # Custom fonts
│   │   │
│   │   ├── /environments     # Environment configurations
│   │   │   ├── environment.ts      # Development environment
│   │   │   ├── environment.prod.ts # Production environment
│   │   │   └── ...
│   │   │
│   │   ├── app.component.ts  # Main app component
│   │   ├── app.component.html
│   │   ├── app.component.scss
│   │   ├── app.module.ts     # Main app module
│   │   ├── app-routing.module.ts  # App-level routing module
│   │   ├── main.ts           # Main entry point
│   │   ├── index.html        # Main HTML file
│   │   ├── styles.scss       # Global styles
│   │   ├── polyfills.ts      # Polyfills for browser compatibility
│   │   └── ...
│   │
├── .browserslistrc           # Browserslist configuration for target browsers
├── .editorconfig             # Editor configuration
├── .gitignore                # Files and directories to ignore in Git
├── angular.json              # Angular CLI configuration
├── package.json              # NPM dependencies and scripts
├── package-lock.json         # NPM lockfile for dependencies
├── README.md                 # Project documentation
├── tsconfig.json             # TypeScript configuration
└── tslint.json               # TSLint configuration (if using TSLint)
```


## Installation

To set up the development environment for this project, follow these steps:

1. **Clone the Repository**: 
    ```
    git clone <repository-url>
    cd ghar-manage
    ```
2. **Install Dependencies**: 
Make sure you have [Node.js](https://nodejs.org/) and npm installed. Then, run:
    ```
    npm install
    ```


3. **Set Up Firebase (Optional)**:
If you're using Firebase, create a Firebase project, and add the Firebase configuration to `src/environments/environment.ts` and `src/environments/environment.prod.ts`.

## Running the App

To run the app in development mode, use the Angular CLI command:

```
ng serve
```

Navigate to `http://localhost:4200/`. The app will automatically reload if you change any of the source files.

## Build

To build the project for production, use:
```
ng build --prod
```



The build artifacts will be stored in the `dist/` directory. Use the `--prod` flag for a production build.


## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
