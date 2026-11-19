# Odoo 20 Community - Docker

Docker-based deployment of Odoo 20 Community with PostgreSQL 16.

## Components

- Odoo: `odoo:20.0`
- PostgreSQL: `postgres:16`
- Custom addons: `./addons`
- Odoo persistent data: `./data`
- PostgreSQL data: `./postgres`
- Odoo web port: `8071`

## Requirements

- Docker Desktop
- Docker Compose v2
- Git

## Initial setup

1. Clone this repository.
2. Create the required Docker network:

   ```powershell
   docker network create odoo20-network
   ```

   If the network already exists, do not create it again.

3. Create your local environment file:

   ```powershell
   Copy-Item .env.example .env
   notepad .env
   ```

   Replace the placeholder passwords with secure values.
   Use the same PostgreSQL credentials for `POSTGRES_USER` and
   `ODOO_DB_USER`, and for their respective passwords.

4. Create your local Odoo configuration:

   ```powershell
   Copy-Item config/odoo.conf.example odoo.conf
   notepad odoo.conf
   ```

   Set a strong `admin_passwd`. Never commit this file.

5. Create persistent data directories if they do not exist:

   ```powershell
   New-Item -ItemType Directory -Force postgres, data
   ```

6. Start the services:

   ```powershell
   docker compose up -d
   ```

7. Open Odoo:

   http://localhost:8071

## Important notes

- `.env` and `odoo.conf` contain local secrets and are excluded from Git.
- PostgreSQL data, Odoo filestore, and backups are not stored in this repository.
- Custom addons are stored in `addons/`.
- A fresh deployment creates a new database. This repository does not contain production database backups.
- Keep database and filestore backups separately.
- The Docker network `odoo20-network` is configured as an external network.
- If containers with the same names already exist on the machine, review them before starting Compose to avoid container-name conflicts.

## Repository structure

```text
Odoo20-Docker/
├── addons/
├── config/
│   └── odoo.conf.example
├── .env.example
├── .gitignore
├── docker-compose.yml
└── README.md
```
