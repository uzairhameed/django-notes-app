# Django Notes App

A simple notes application built with **React** and **Django**, containerized with **Docker** and **Docker Compose**.

This project was Dockerized as a hands-on **DevOps learning project**, with separate services for the application, MySQL database, and Nginx reverse proxy.

## Tech Stack

* **Frontend:** React
* **Backend:** Django
* **Database:** MySQL
* **Containerization:** Docker
* **Container Orchestration:** Docker Compose
* **Web Server / Reverse Proxy:** Nginx

## Project Structure

```text
django-notes-app/
├── backend/              # Django backend
├── frontend/             # React frontend
├── nginx/                # Nginx configuration
├── Dockerfile            # Django application image
├── docker-compose.yml    # Multi-container configuration
├── requirements.txt      # Python dependencies
└── .gitignore
```

## Prerequisites

If running the application with Docker, you only need:

* Docker
* Docker Compose

You do not need to install Python, Node.js, or MySQL separately when running the complete application through Docker Compose.

## Running with Docker Compose

### 1. Clone the repository

```bash
git clone https://github.com/uzairhameed/django-notes-app.git
cd django-notes-app
```

### 2. Build the containers

```bash
docker compose build
```

### 3. Start the application

```bash
docker compose up -d
```

### 4. Check running containers

```bash
docker compose ps
```

### 5. View application logs

```bash
docker compose logs -f
```

## Services

The application consists of multiple containers:

### Django

Runs the backend application and handles API requests.

### MySQL

Provides the database used by the Django application.

### Nginx

Acts as a reverse proxy and handles incoming HTTP requests before forwarding them to the appropriate application service.

## Nginx

The Nginx configuration is located at:

```text
nginx/default.conf
```

Nginx is used as a reverse proxy to make the application accessible through a single entry point.

If installing Nginx directly on an Ubuntu server instead of using the Dockerized configuration:

```bash
sudo apt update
sudo apt install nginx -y
```

Check the Nginx service:

```bash
sudo systemctl status nginx
```

## Useful Docker Commands

Stop the application:

```bash
docker compose down
```

Rebuild the application:

```bash
docker compose build
```

Start the application in the background:

```bash
docker compose up -d
```

View logs:

```bash
docker compose logs -f
```

View running containers:

```bash
docker compose ps
```

## DevOps Concepts Practiced

This project was used to practice:

* Docker containerization
* Dockerfile creation
* Docker Compose
* Multi-container application deployment
* Nginx reverse proxy configuration
* MySQL containerization
* Linux server administration
* Application troubleshooting and container logs
* Environment and configuration management

## Note

This repository is primarily a **DevOps learning and portfolio project** demonstrating the process of containerizing an existing Django/React application and running its services using Docker Compose.
