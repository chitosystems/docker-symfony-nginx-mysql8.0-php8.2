# docker-nginx-mysql8.0-php8.2

This repository provides a Docker environment for running a PHP 8.2 application with Nginx as a proxy and MySQL 8.0 as the database. Follow the steps below to set up and run your web application.

## Prerequisites
- Docker installed on your machine
- Docker Compose installed on your machine

## Getting Started

1. Clone this repository to your local machine.

    ```bash
    git clone git@github.com:chitosystems/docker-symfony-nginx-mysql8.0-php8.2.git my-app
    cd my-app
    ```

2. Create a `.env` file from the provided `example.env` file.

    ```bash
    cp example.env .env
    ```

3. Run the following command to build and start the Docker containers:

    ```bash
    docker-compose up -d --build
    ```

4. Access the application container's bash shell:

    ```bash
    docker-compose exec app /bin/bash
    ```

5. Inside the container, check Symfony requirements:

    ```bash
    symfony check:requirements
    ```

6. Create a new Symfony project:

    ```bash
    symfony new .
    ```

7. Navigate to the `app` directory and add your web application's Git repository:

    ```bash
    cd app
    git remote add origin <your-git-repo-url>
    ```

Now your PHP 8.2 application with Nginx proxy and MySQL 8.0 is set up and running. Access it in your browser at [http://localhost:8080/](http://localhost:8080/).

Feel free to customize the configuration files and add your application-specific settings as needed.

## Folder Structure

```plaintext
web-app-name
|-- .docker
|   |-- app
|-- mysql
|-- .gitignore
|-- compose.yml
|-- example.env
|-- Readme.md
|-- LICENCE
````

# Licence 
This project is licensed under the MIT Licence - see the [LICENCE] (https://github.com/chitosystems/docker-symfony-nginx-mysql8.0-php8.2/blob/main/LICENCE). file for details.
