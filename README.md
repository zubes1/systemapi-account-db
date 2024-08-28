# System API - Account Database

This repository contains a MuleSoft API project that interacts with a MySQL database backend. The API is designed to perform CRUD operations on account data. The project includes MUnit tests to validate the API functionality, as well as a Docker Compose file to easily spin up the required dependencies for testing, including a MySQL database. A database initialization script is also provided to set up the schema and insert test data.

## Features

- **MuleSoft API**: Developed using MuleSoft's Anypoint Studio, this API connects to a MySQL database and provides endpoints for account management.
- **MUnit Tests**: Includes MUnit tests to ensure the API's functionality is thoroughly tested.
- **Docker Compose**: A Docker Compose file is included to spin up the necessary dependencies (e.g., MySQL) locally for testing.
- **Database Initialization**: A SQL script is provided to set up the database schema and populate it with test data.

## Prerequisites

Before cloning and setting up this project, ensure you have the following installed:

- **Anypoint Studio**: MuleSoft's IDE for developing, testing, and deploying Mule applications.
  - [Download Anypoint Studio](https://www.mulesoft.com/lp/dl/studio)
- **Docker Desktop**: To run Docker Compose and manage containers locally.
  - [Download Docker Desktop](https://www.docker.com/products/docker-desktop)

## Getting Started

Follow these steps to clone the project and set it up in Anypoint Studio.

### 1. Clone the Repository

Open a terminal and run the following command to clone the repository:

```bash
git clone https://github.com/zubes1/systemapi-account-db.git
cd systemapi-account-db

## 2. Open the Project in Anypoint Studio

1. Launch **Anypoint Studio**.
2. Go to **File** → **Import…**.
3. Select **Anypoint Studio Project from File System** and click **Next**.
4. Browse to the cloned repository’s directory and select it.
5. Click **Finish** to import the project.

## 3. Set Up and Run the Dependencies with Docker Compose

This project includes a `docker-compose.yml` file that will set up a MySQL database required by the API.

1. Open a terminal in the project’s root directory (where the `docker-compose.yml` file is located).
2. Run the following command to start the MySQL container:

```bash
docker-compose up -d

### This command will:

- Spin up a MySQL database container.
- Initialize the database schema and insert test data using the provided SQL script.

### 4. Run MUnit Tests

To ensure the API is functioning correctly, you can run the MUnit tests provided in the project.

1. In **Anypoint Studio**, navigate to the **MUnit Tests** section of the project.
2. Right-click on the test suite or individual tests.
3. Select **Run As** → **MUnit Test**.

The tests will execute against the MySQL database running in the Docker container, validating the API’s behavior.

### Additional Information

- **Docker Compose**: The `docker-compose.yml` file includes configuration to spin up a MySQL database container, exposing it on the default MySQL port (3306). The database is initialized with the provided `init.sql` script.
- **Database Initialization**: The `init.sql` script creates the necessary database schema and populates it with initial test data, ensuring that the MUnit tests have the required data to run.
   
   