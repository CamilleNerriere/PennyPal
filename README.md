# PennyPal – Full Application

**PennyPal** is a simple and secure budget management application built with React (frontend) and .NET 8 (backend).  
It allows users to track expenses, manage categories, and visualize spending trends.

This repository contains the full Docker setup to run the entire stack locally: frontend, backend, and SQL Server.

---

##  Architecture

- **Frontend** – React + TypeScript  
  [See frontend README](https://github.com/CamilleNerriere/PennyPal-front/blob/main/README.md)

- **Backend** – ASP.NET Core + SQL Server  
  [See backend README](https://github.com/CamilleNerriere/PennyPalAPI/blob/main/README.md)

- **Database** – SQL Server with seed scripts

---

##  Quick Start (Development)

> You must have **Docker** and **Docker Compose** installed on your machine.

1. Clone the repository:
   ```bash
   git clone https://github.com/CamilleNerriere/PennyPal.git
   cd PennyPal
   ```

2. Create your .env file from the example:

    ```bash
        cp .env.example .env
    ```

    Update the variables to match your environment (API URL, DB password, etc.)

3. Start the full application 

```bash
    docker-compose -f docker-compose.yml up --build
```

4. Access the app at: 

    * Frontend: http://localhost:5173
    * API: http://localhost:5001

##  Demo Accounts

The following demo accounts are preloaded into the database and can be used to explore the application without registration:

| Email                      | Password |
|---------------------------|----------|
| john.doe@example.com      | test     |
| jane.smith@example.com    | test     |
| charlie.brown@example.com | test     |
| demo.user@example.com     | test     |

Each account includes predefined categories and example expenses to demonstrate the application's features.

## API Reference

For detailed information about the available endpoints, authentication system, and request structure, please refer to the [backend README](./PennyPalAPI/README.md).


## Production Setup

A sample Docker Compose file for production is included as a reference:  
[`docker-compose.prod.example.yml`](./docker-compose.prod.example.yml)

>  This file is **not intended for direct deployment**. It references private configuration files (e.g., `nginx.conf`) that are not included in this repository.
>

You can use the example as a starting point to build your own production setup.

---

## TODO

Planned improvements for upcoming versions:

- Improve mobile responsiveness and fix input focus issues on small screens (e.g. auto zoom not resetting after input blur)
- Add unit and integration tests for backend and frontend


## Licence

This project is open-source and available under the MIT License.
