# Blazor Reusable Form Component Exercise

This repository contains a solution for "Exercise #2 - Reusable Form Component". It demonstrates a clean, component-based architecture using Blazor, focusing on reusability, proper data binding, and separation of concerns.

## Project Structure
* `Models/UserModel.cs`: Contains the data model and all DataAnnotation validation rules.
* `Components/UserForm.razor`: The reusable UI component. It contains no business logic and relies entirely on parameters and `EventCallback` to communicate with the parent.
* `Pages/UserRegistration.razor`: The parent page that implements the `UserForm`, passes the model, and handles the simulated data submission.

## Features & Optional Enhancements Implemented
* ✅ **Complete Separation of Concerns**: The form only handles UI state and delegates submission logic to the parent.
* ✅ **DataAnnotations Validation**: Inline validation messages and an optional toggleable validation summary.
* ✅ **Processing State**: The submit button disables and shows a spinner while the parent processes the submission.
* ✅ **Customizable Submit Text**: Parent can inject custom text for the submit button.
* ✅ **Bootstrap 5 Styling**: Utilizes standard Bootstrap classes for a clean, responsive, and business-ready UI.

## Prerequisites
* .NET 10.0 SDK (or later) installed.

## How to Build and Run
1.  Clone this repository to your local machine.
    ```bash
    git clone <your-repo-url>
    ```
2.  Navigate to the project directory.
    ```bash
    cd BlazorUserForm
    ```
3.  Run the application using the .NET CLI.
    ```bash
    dotnet run
    ```
4.  Open a browser and navigate to `http://localhost:<port>/user-registration` (check your console output for the exact local port).

## Assumptions / Notes
* **Styling**: Assumed the standard Blazor template inclusion of Bootstrap 5 is acceptable for meeting the "UI and usability" requirements without introducing external CSS file bloat.
* **Interactivity**: Designed to work under any Blazor render mode (Server, WebAssembly, or Auto) by relying entirely on standard Blazor binding and event callbacks.