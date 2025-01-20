# Odoo Simplified Setup: One Command ERP/CRM Deployment

Effortlessly deploy Odoo 17.0 with PostgreSQL 16 and Adminer 4.8.1 using Docker. This project simplifies the setup process, enabling you to start a fully functional Odoo environment with just one command.

---

## **What is Odoo?**

Odoo is an open-source Enterprise Resource Planning (ERP) and Customer Relationship Management (CRM) software solution. It offers over 80 modules that cover a wide range of business needs, such as accounting, inventory management, human resources, project management, e-commerce, and more. 

### **Key Features:**
- Modular structure that allows businesses to install only the apps they need.
- User-friendly interface with modern design.
- Open-source platform with a vibrant developer and user community.
- Highly customizable to fit unique business requirements.

- **Website:** [Odoo Official Site](https://www.odoo.com/)
- **Credits:**
  - Odoo is maintained by Odoo S.A.
  - It is distributed under the GNU Lesser General Public License (LGPL).

---

## **Why Neural Inverse Developed This**

The Neural Inverse team created this simplified setup as part of their commitment to empowering developers and businesses. Here’s why:

- **Streamlined Deployment:** ERP and CRM systems often require complex setups. This project reduces the setup to a single command, making it accessible for developers of all skill levels.
- **Accessibility:** By lowering technical barriers, Neural Inverse encourages businesses to adopt Odoo for efficient operations.
- **Developer Empowerment:** Providing a ready-to-use, containerized environment allows developers to focus on extending functionality and innovation rather than struggling with installation issues.
- **Alignment with Mission:** Neural Inverse’s mission is to create tools that simplify complex tasks and enhance productivity, making this project a natural fit.

---

## **Table of Contents**

1. [What is Odoo?](#what-is-odoo)
2. [Why Neural Inverse Developed This](#why-neural-inverse-developed-this)
3. [Requirements](#requirements)
4. [Tested Versions](#tested-versions)
5. [How to Run](#how-to-run)
   - [Prepare Your Environment](#1-prepare-your-environment)
   - [Run the Setup](#2-run-the-setup)
6. [Project Structure](#project-structure)
7. [What’s Inside?](#whats-inside)
8. [Developer Tracking Table](#developer-tracking-table)
9. [Customization Options](#customization-options)
10. [Accessing the Services](#accessing-the-services)
11. [Stopping the Services](#stopping-the-services)
12. [Troubleshooting](#troubleshooting)
13. [Useful Links](#useful-links)
14. [License](#license)
15. [Contributing](#contributing)

---

## **Requirements**

- Docker container virtualization service
- Basic knowledge of running shell or batch scripts

---

## **Tested Versions**

- **PostgreSQL:** 16
- **Odoo:** 17.0
- **Adminer:** 4.8.1

---

## **How to Run**

### **1. Prepare Your Environment**

1. Clone the repository to your local system:
   ```bash
   git clone https://github.com/YourOrganization/YourRepo.git
   cd YourRepo
   ```

2. Create a `.env` file for environment variables:
   - An example `.env` file (`.env.example`) is already provided in the source code.
   - Rename `.env.example` to `.env`:
     ```bash
     mv .env.example .env
     ```
   - Customize the `.env` file as needed. Below are the default values in `.env.example`:

     ```env
     ##################
     ## POSTGRESQL
     ##################
     POSTGRES_HOST=postgres      # postgres container hostname
     POSTGRES_VERSION=16         # postgres version
     POSTGRES_USER=postgres      # superuser username of postgresql
     POSTGRES_PASSWORD=postgres  # superuser password of postgresql
     POSTGRES_DB=postgres        # default database of postgresql
     POSTGRES_PORT=5432          # port on which postgres is running

     ##################
     ## ODOO
     ##################
     ODOO_HOST=odoo              # odoo container hostname
     ODOO_VERSION=17.0           # odoo version
     ODOO_DB_USER=odoo           # username of dedicated user of odoo
     ODOO_DB_PASSWORD=odoo       # password of dedicated user of odoo
     ODOO_DB_NAME=odoo           # database name of odoo
     ODOO_PORT=8069              # port on which odoo is running

     ##################
     ## ADMINER
     ##################
     ADMINER_HOST=adminer        # adminer container hostname
     ADMINER_VERSION=4.8.1       # adminer version
     ADMINER_PORT=8080           # port on which adminer is running
     ```

3. Update variables at the top of the `build_and_run.sh` (Linux/Mac) or `build_and_run.bat` (Windows) script if necessary.

---

### **2. Run the Setup**

#### **For Linux/Mac:**

1. Make the script executable:
   ```bash
   chmod +x ./build_and_run.sh
   ```

2. Run the script to build and start the Docker containers:
   ```bash
   ./build_and_run.sh
   ```

#### **For Windows:**

1. Execute the `build_and_run.bat` script:
   ```
   build_and_run.bat
   ```

---

## **Project Structure**

- `build_and_run.sh`: Shell script for Linux/Mac to set up and run the containers.
- `build_and_run.bat`: Batch script for Windows to set up and run the containers.
- `docker-compose.yml`: Defines the Docker services for Odoo, PostgreSQL, and Adminer.
- `.env.example`: Sample environment variables configuration file.

---

## **What’s Inside?**

This project creates and configures the following containers:

- **Odoo 17.0**: A powerful open-source ERP/CRM system.
- **PostgreSQL 16**: A reliable and robust database to store Odoo data.
- **Adminer 4.8.1**: A lightweight database management tool for PostgreSQL.

All containers are configured using Docker Compose for ease of deployment and management.

---

## **Developer Tracking Table**

| Task ID | Developer Name      | Task Description                        | Status       |
|---------|---------------------|------------------------------------------|--------------|
| 001     | [Your Name Here]    | Set up Docker environment               | In Progress  |
| 002     | [Your Name Here]    | Configure PostgreSQL and Odoo containers| Completed    |
| 003     | [Your Name Here]    | Test Odoo and Adminer accessibility     | Pending      |

---

## **Customization Options**

You can modify the following parameters in the `.env` file:

- **PostgreSQL Configuration:**
  - `POSTGRES_HOST`: Hostname for the PostgreSQL container (default: `postgres`)
  - `POSTGRES_VERSION`: PostgreSQL version (default: `16`)
  - `POSTGRES_USER`: PostgreSQL superuser username (default: `postgres`)
  - `POSTGRES_PASSWORD`: PostgreSQL superuser password (default: `postgres`)
  - `POSTGRES_DB`: Default PostgreSQL database name (default: `postgres`)
  - `POSTGRES_PORT`: Port for PostgreSQL (default: `5432`)

- **Odoo Configuration:**
  - `ODOO_HOST`: Hostname for the Odoo container (default: `odoo`)
  - `ODOO_VERSION`: Odoo version (default: `17.0`)
  - `ODOO_DB_USER`: Odoo database username (default: `odoo`)
  - `ODOO_DB_PASSWORD`: Odoo database password (default: `odoo`)
  - `ODOO_DB_NAME`: Odoo database name (default: `odoo`)
  - `ODOO_PORT`: Port for the Odoo web interface (default: `8069`)

- **Adminer Configuration:**
  - `ADMINER_HOST`: Hostname for the Adminer container (default: `adminer`)
  - `ADMINER_VERSION`: Adminer version (default: `4.8.1`)
  - `ADMINER_PORT`: Port for Adminer (default: `8080`)

---

## **Accessing the Services**

- **Odoo Web Interface:**
  - URL: `http://localhost:<ODOO_PORT>` (default: `http://localhost:8069`)

- **Adminer Database Management:**

URL: `http://localhost:<ADMINER_PORT>` (default: `http://localhost:8080`)

---

## **Stopping the Services**

To stop all running containers, execute the following command:

```bash
docker-compose down
```

This will shut down and remove all containers, networks, and volumes created by the project.

---

## **Troubleshooting**

Here are some common issues and their solutions:

1. **Docker Service Not Running:**
   - Error: "Docker service is not running. Please start Docker and try again."
   - Solution: Start the Docker service using the appropriate command for your operating system.

2. **Port Already in Use:**
   - Error: "Bind for 0.0.0.0:<PORT> failed: port is already allocated."
   - Solution: Check which process is using the port with `netstat` or `lsof` and stop it, or modify the port in the `.env` file.

3. **PostgreSQL Connection Timeout:**
   - Error: "Timed out waiting for PostgreSQL to become available."
   - Solution: Ensure that the PostgreSQL container is running and accessible. Check the container logs with:
     ```bash
     docker-compose logs postgres
     ```

4. **Unable to Access Odoo:**
   - Error: "This site can’t be reached."
   - Solution: Verify that the Odoo container is running and the port is correctly configured in the `.env` file.

---

## **Useful Links**

- [Odoo Official Documentation](https://www.odoo.com/documentation)
- [Docker Documentation](https://docs.docker.com/)
- [PostgreSQL Official Documentation](https://www.postgresql.org/docs/)
- [Adminer Official Site](https://www.adminer.org/)

---

## **License**

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---

## **Contributing**

Contributions are welcome! Please follow these steps:

1. Fork the repository.
2. Create a new branch:
   ```bash
   git checkout -b feature/YourFeatureName
   ```
3. Commit your changes:
   ```bash
   git commit -m "Add some feature"
   ```
4. Push to the branch:
   ```bash
   git push origin feature/YourFeatureName
   ```
5. Open a Pull Request.

---

## **Why Choose This Project?**

This project offers a quick and efficient way to deploy Odoo, PostgreSQL, and Adminer with minimal effort. Its simplicity ensures that:

- Developers save time on setup.
- Businesses can focus on customization and functionality rather than infrastructure.
- Teams benefit from a robust, containerized environment ready for testing and production.

By automating the setup process, Neural Inverse ensures that users can leverage the full potential of Odoo without being hindered by technical complexities.
