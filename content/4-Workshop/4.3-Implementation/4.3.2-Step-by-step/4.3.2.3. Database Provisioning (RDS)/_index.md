---
title: "Database Provisioning (RDS)"
weight: 3
pre: "<b> 4.3.2.3. </b>"
---

### Objective
Deploy a managed MySQL database instance to handle structured data for the **Classic Groove** platform, ensuring high availability and data integrity.

### Execution Steps

#### 1. RDS Instance Creation
*   **Service:** Navigate to the **RDS Dashboard** and select **Create database**.
*   **Engine Options:** Select **MySQL**.
*   **Templates:** Choose **Free Tier** to optimize costs.
*   **Settings:**
    *   **DB instance identifier:** `classic-groove-db`.
    *   **Master username:** `admin`.
    *   **Master password:** Set a secure password (e.g., `ClassicGroove2026`).
*   **Instance Configuration:** Select `db.t3.micro`.
*   **Connectivity:**
    *   **Public access:** Select **Yes** (for initial configuration and migration).
    *   **VPC Security Group:** Create a new group named `classic-groove-db-sg`.
*   **Additional Configuration:**
    *   **Initial database name:** `classic_groove`.

#### 2. Security Configuration
To allow the EC2 web server to communicate with the database:
*   Access the **Security Group** `classic-groove-db-sg`.
*   Add an **Inbound Rule**:
    *   **Type:** MySQL/Aurora (Port 3306).
    *   **Source:** Select the Security Group ID of the EC2 instance or `0.0.0.0/0` for testing.

#### 3. Database Migration & Connectivity
*   **Install MySQL Client on EC2:**
    ```bash
    sudo dnf install mysql -y
    ```
*   **Connect to RDS:**
    ```bash
    mysql -h <rds-endpoint> -u admin -p
    ```
*   **Import Schema:** Transfer the SQL dump from the local machine and import it into the RDS instance:
    
```bash
    mysql -h <rds-endpoint> -u admin -p classic_groove < classic-groove.sql
```

#### 4. Application Integration
Update the PHP configuration file (e.g., `dataProvider.php`) to point to the RDS endpoint:
```php
mysqli_real_connect(
    $connection,
    "classic-groove-db.<id>.<region>.rds.amazonaws.com",
    "admin",
    "your_password",
    "classic_groove",
    3306
);
```