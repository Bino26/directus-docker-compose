# Directus with PostGIS and Redis (Docker Compose)

This repository provides a pre-configured `docker-compose` setup to run [Directus](https://directus.io/) with integrated [PostGIS](https://postgis.net/) (a spatial database extender for PostgreSQL) and [Redis](https://redis.io/) for caching and real-time functionality.

## 📦 Features

- 🔧 **Directus** – Headless CMS for managing data.
- 🗺️ **PostGIS** – Adds spatial capabilities to PostgreSQL for GIS support.
- ⚡ **Redis** – Enhances performance and supports real-time features in Directus.

## 🚀 Quick Start

### 1. Clone the Repository

```bash
git clone https://github.com/Bino26/directus-docker-compose.git
cd directus-docker-compose
```
### 2. Configure Environment Variables

```bash
cp .env.example .env
```

### 3. Build an Run your Directus app 

```bash
docker compose up -build
```
You can shut down with :
```bash
docker compose down
```

### Import Snapshot at startup
When the container is started, the data is automatically imported from snapshot.yaml

```bash
Create snapshot.yaml:
npx directus schema snapshot ./snapshot.yaml
```

### 4. Access Directus
Visit: [http://localhost:8055](http://localhost:8055).

Enter those credentials below to  enter in the admin panel and feel free to create your concent !

```bash
e-mail: admin@example.com
password:d1r3ctu5
```

Update your admin user password:

```bash
npx directus users passwd --email user-email --password new-password
```
### 4. Deployment
🔒 Important: Edit this file to set your own KEY, SECRET,ADMIN_EMAIL,ADMIN_PASSWORD,CORS_ORIGIN and database credentials for production use.
