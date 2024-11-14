# Full Stack Application

This project is a full-stack application consisting of a React frontend, a Flask backend, and a PostgreSQL database. The application allows users to add, fetch, and delete text entries.

## Project Structure

## Backend

The backend is a Flask application that provides RESTful API endpoints to interact with the PostgreSQL database.

### Endpoints

- `GET /fetch`: Fetch all text entries.
- `POST /add`: Add a new text entry.
- `DELETE /delete`: Delete all text entries.

### Setup

1. Navigate to the `backend` directory.
2. Build the Docker image:
    ```sh
    docker build -t backend:latest .
    ```
3. Deploy the backend using Kubernetes:
    ```sh
    kubectl apply -f .
    ```

## Database

The database is a PostgreSQL instance initialized with a ConfigMap.

### Setup

1. Navigate to the `database` directory.
2. Deploy the database using Kubernetes:
    ```sh
    kubectl apply -f .
    ```

## Frontend

The frontend is a React application that interacts with the Flask backend.

### Setup

1. Navigate to the `frontend` directory.
2. Build the Docker image:
    ```sh
    docker build -t frontend:latest .
    ```
3. Deploy the frontend using Kubernetes:
    ```sh
    kubectl apply -f .
    ```

## Running the Application

1. Ensure all services are running:
    ```sh
    kubectl get pods
    kubectl get services
    ```
2. Access the frontend application at `http://<node-ip>:30000`.

## References

- [Tutorial: Deploy Full Stack Application in Kubernetes](https://www.swtestacademy.com/deploy-full-stack-application-in-kubernetes/)