# Dockerized Full Stack Application

This is a Dockerized full-stack application consisting of a Node.js backend, a React frontend, and a MongoDB database. The objective of this application is to stored goals set by its user. Please note that the code for the app, including the JavaScript, JSON, HTML and CSS is not authored by the repository owner.

## Prerequisites

Before you begin, ensure you have Docker and Docker Compose installed on your system.

## Project Structure

- `Backend`: Contains the Node.js backend application.
- `Frontend`: Houses the React frontend application.
- `Env`: Contains environment configuration files for the services.
- `Docker-Commands.txt`: Lists Docker commands used in the project.
- `docker-compose.yaml`: Defines the services, volumes, and networks for Docker Compose.

## Usage

Before running the Docker-Compose file make sure to provide the required credentials by creating a mongo.env file in the Env directory. Example content:

**MONGO_INITDB_ROOT_USERNAME**=`<your-user>`

**MONGO_INITDB_ROOT_PASSWORD**=`<your-password>`

Ensure you've provided the required environment variables by creating a backend.env file in the Env directory. Example content:

**MONGO_INITDB_ROOT_USERNAME**=`<your-user>`

**MONGO_INITDB_ROOT_PASSWORD**=`<your-password>`

This is very important that both files have the exact same user and password due to this is the way to authenticate the access of the backend to the database.


## Building and Running the MongoDB Container, Backend Container and Frontend Container

1. Run the docker-compose yaml file.

   ```docker    
    docker-compose up -d
     ```


## Access the Application
- Backend: http://localhost:80
- Frontend: http://localhost:3000

Notes

- The MongoDB data is persisted in a volume named data.
- Backend logs are stored in the logs volume.
- Live updates are supported for both backend and frontend through Bind Mounts.

## Stopping the Containers

To stop all containers, use:

    ```docker      
    docker-compose down
    ``` 

# Contributing

If you'd like to contribute to this project, feel free to open an issue or submit a pull request on the GitHub repository.

# License

This project is licensed under the MIT License. See the LICENSE file for details. 