# Application Architecture

This document describes the software architecture for the Nemeno Quiz App.

## Architectural Pattern: MVVM

The app will follow the **Model-View-ViewModel (MVVM)** pattern, which is the recommended architecture for modern Android applications. This pattern separates the UI from the business logic, making the code more modular, testable, and maintainable.

## Core Components

*   **View (Composables)**
    *   The UI layer will be built entirely with **Jetpack Compose**.
    *   Each screen (e.g., Dashboard, Quiz, Profile) will be a Composable function.
    *   Views are responsible for displaying data and forwarding user events to the ViewModel.

*   **ViewModel**
    *   `DashboardViewModel`, `QuizViewModel`, `ProfileViewModel`, etc.
    *   ViewModels will contain the business logic for each screen.
    *   They will expose state (e.g., using `StateFlow` or `LiveData`) to the UI and handle user interactions.

*   **Model**
    *   These will be Kotlin `data class` objects representing the application's data.
    *   Examples: `Course`, `Subject`, `Quiz`, `Question`, `User`.

*   **Repository**
    *   A single source of truth for the application's data.
    *   The repository will abstract the data sources, whether it's a remote API, a local database (like Room), or both.

## Navigation

*   **Jetpack Navigation**: We will use the Jetpack Navigation component to manage navigation between different screens (Composables) in the app.

## Dependency Injection

*   To manage dependencies and further decouple components, we will use a dependency injection framework like **Hilt** or **Koin**.
