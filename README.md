# 📦 LAMP + WordPress with Docker Compose

A clean and portable development environment using Docker Compose:
- **MySQL 5.7** for database.
- **WordPress latest** running on Apache + PHP.
- Volumes for persistent database and wp-content storage.

---

## 🛠️ Quick Start

1. Clone or prepare this project directory:

```bash
   git clone <your-repo> lamp-wordpress
   cd lamp-wordpress
```

2. Create .env with your credentials:

```bash
    MYSQL_ROOT_PASSWORD=wordpress
    MYSQL_DATABASE=wordpress
    MYSQL_USER=wordpress
    MYSQL_PASSWORD=wordpress
```

3. Launch the stack:

```bash
    docker network create appnet
    docker-compose up -d
```

4. Visit http://localhost:8000 and complete the WordPress setup wizard.
5. visit http://wordpress.ir/wp-admin/

```bash
    lamp‑wordpress/
    ├── .env                # environment variables (keep private)
    ├── docker-compose.yml  # service definitions for DB & WordPress
    └── www/                # mounted wp-content for plugins, themes, uploads
```


## Helper

```bash
| Command                           | Description                                 |
| --------------------------------- | ------------------------------------------- |
| `docker-compose up -d`            | Start services in detached mode             |
| `docker-compose ps`               | Show running containers                     |
| `docker-compose logs`             | View logs from all services                 |
| `docker-compose logs -f`          | Viewing live logs for all services          |
| `docker-compose logs wordpress`   | View only WordPress logs                    |
| `docker-compose stop`             | Stop services                               |
| `docker-compose start`            | Start stopped services                      |
| `docker-compose down`             | Stop and remove containers & network        |
| `docker-compose down --volumes`   | Remove containers, network, **and volumes** |
```