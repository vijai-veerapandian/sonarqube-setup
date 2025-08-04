
Quick SonarQube Docker Compose setup:

This repository contains a simple Docker Compose configuration to run SonarQube with a PostgreSQL database.

## Prerequisites

- Docker installed on your VM
- Docker Compose installed on your VM

## How to Run

1. Clone or download this repository to your VM.

2. Make sure the `docker-compose.yml` file is present.

3. Start the SonarQube and PostgreSQL containers:


```
docker-compose up -d

```

4. Access SonarQube in your browser at:

```
http://<your-vm-ip>:9000

```

5. Login to SonarQube web UI with default credentials:

- Username: `admin`
- Password: `admin`

6. Change the admin password when prompted.

## Configuration

- The PostgreSQL database credentials are set in `docker-compose.yml`:

```
POSTGRES_USER: sonarqube
POSTGRES_PASSWORD: sonarqube_password
POSTGRES_DB: sonarqube

```

- SonarQube connects to PostgreSQL using these credentials. You can update them both in the `db` and `sonarqube` service environment sections if needed.

## Stopping the Services

To stop and remove the containers, run:

```
docker-compose down

```

## Notes

- The first time you start SonarQube, it may take a few minutes to initialize.
- For production use, consider securing your database and SonarQube access.
- Volumes are used to persist data and configurations.

---

SonarQube is ready to play with analysising the code!

