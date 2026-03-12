
---

# 🛠️ Lab Setup: Damn Vulnerable Web App (DVWA)

**Purpose:** This guide outlines the manual installation of DVWA on a Debian-based Linux system (like Kali or Ubuntu) for cybersecurity testing and practice.

### 1. Repository Initialization

Clone the source code into the web server's root directory.

```bash
cd /var/www/html
sudo git clone https://github.com/digininja/DVWA.git

```

* **Why:** `/var/www/html` is the default directory where Apache looks for website files.

### 2. Permissions Management

Grant full read/write/execute permissions to the folder.

```bash
sudo chmod -R 777 /var/www/html/DVWA

```

* **Security Note:** `777` is used here for lab convenience so the web app can write to its own logs and uploads, but **never** use this in a production environment.

### 3. Application Configuration

Create the active config file from the template provided by the developers.

```bash
cd /var/www/html/DVWA/config
cp config.inc.php.dist config.inc.php
sudo mousepad config.inc.php

```

* **Action:** Ensure the `db_user` and `db_password` match what you create in Step 6.

### 4. Database Service Initiation

Ensure the MariaDB/MySQL service is active.

```bash
sudo systemctl start mysql
sudo systemctl status mysql # Press 'q' to exit status view

```

### 5. Backend Database Setup

Log in to the database to create the environment for DVWA.

```bash
sudo mysql -u root

```

Once inside the MySQL prompt, run:

```sql
CREATE DATABASE dvwa;
CREATE USER 'admin'@'127.0.0.1' IDENTIFIED BY 'password';
GRANT ALL PRIVILEGES ON dvwa.* TO 'admin'@'127.0.0.1';
FLUSH PRIVILEGES;
EXIT;

```

* **Note:** These credentials must match your `config.inc.php` file exactly.

### 6. Web Server Deployment

Start Apache and verify it is handling requests.

```bash
sudo systemctl start apache2
sudo systemctl restart apache2

```

### 7. PHP Environment Check

Navigate to your PHP config to ensure modules are loaded (common for troubleshooting `allow_url_include`).

```bash
cd /etc/php/$(php -r 'echo PHP_MAJOR_VERSION.".".PHP_MINOR_VERSION;')/apache2

```

### 8. Finalization

1. Navigate to: `http://localhost/DVWA/setup.php`
2. Click **Create / Reset Database**.
3. Default Login: `admin` / `password`.

---

