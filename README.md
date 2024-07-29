# DemoExternalAuthenProviders

This repository demonstrates how to integrate external authentication providers (Google, Facebook, Microsoft) in an ASP.NET Core application using OAuth 2.0.

## Table of Contents

- [Features](#features)
- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Configuration](#configuration)
- [Running the Application](#running-the-application)
- [Usage](#usage)
- [Contributing](#contributing)
- [License](#license)

## Features

- Integration with Google, Facebook, and Microsoft for external authentication.
- Secure handling of OAuth Client ID and Client Secret using environment variables.
- Example endpoints for logging in and handling authentication callbacks.

## Prerequisites

- [.NET 8 SDK](https://dotnet.microsoft.com/download/dotnet/8.0)
- [Node.js](https://nodejs.org/) (for running the frontend, if applicable)
- [Git](https://git-scm.com/)
- An account on Google, Facebook, and Microsoft Developer platforms to obtain OAuth 2.0 credentials.

## Installation

1. Clone the repository:

    ```sh
    git clone https://github.com/YourUsername/DemoExternalAuthenProviders.git
    cd DemoExternalAuthenProviders
    ```

2. Install the required .NET packages:

    ```sh
    dotnet restore
    ```

## Configuration

1. Set up environment variables for your OAuth credentials:

    - **For Linux and macOS:**

      ```sh
      export GoogleClientId="your-google-client-id"
      export GoogleClientSecret="your-google-client-secret"
      export FacebookAppId="your-facebook-app-id"
      export FacebookAppSecret="your-facebook-app-secret"
      export MicrosoftClientId="your-microsoft-client-id"
      export MicrosoftClientSecret="your-microsoft-client-secret"
      ```

    - **For Windows (PowerShell):**

      ```powershell
      $env:GoogleClientId="your-google-client-id"
      $env:GoogleClientSecret="your-google-client-secret"
      $env:FacebookAppId="your-facebook-app-id"
      $env:FacebookAppSecret="your-facebook-app-secret"
      $env:MicrosoftClientId="your-microsoft-client-id"
      $env:MicrosoftClientSecret="your-microsoft-client-secret"
      ```

2. Create OAuth credentials in the Google, Facebook, and Microsoft Developer Consoles and set the appropriate environment variables as shown above.

3. Update your `appsettings.json` if needed, but avoid including sensitive information directly in the file.

## Running the Application

1. Start the application:

    ```sh
    dotnet run
    ```

2. Open your browser and navigate to `https://localhost:7169` (or the URL shown in the terminal) to see the Swagger UI.

## Usage

### Login Endpoints

Use the following endpoints to initiate the login process with external providers:

- **Google:**
  ```http
  GET /api/account/login?provider=Google
