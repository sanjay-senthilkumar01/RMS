# Odoo Simplified Setup: One Command ERP/CRM Deployment

Effortlessly deploy Odoo 17.0 with PostgreSQL 16 and Adminer 4.8.1 using Docker. This project simplifies the setup process, enabling you to start a fully functional Odoo environment with just one command.

---

## **What is Odoo?**

Odoo is an open-source ERP and CRM solution that provides a wide range of business applications, including accounting, inventory management, HR, and more. It is modular, highly customizable, and integrates seamlessly to support business operations of any size. 

- **Website:** [Odoo Official Site](https://www.odoo.com/)
- **Credits:**
  - Odoo is maintained by Odoo S.A.
  - It is distributed under the GNU Lesser General Public License (LGPL).

---

## **Why Neural Inverse Developed This**

The Neural Inverse team created this simplified setup to:

- **Streamline Deployment:** Reduce the complexity of setting up an ERP/CRM system for businesses and developers.
- **Promote Accessibility:** Enable developers to get started with Odoo without requiring deep technical expertise.
- **Enhance Productivity:** Provide a ready-to-use environment that developers can easily adapt and extend for their specific use cases.

This project aligns with Neural Inverse's vision of empowering developers and organizations with efficient, user-friendly solutions.

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
  - URL: `http://localhost:<ADMINER_PORT>` (default: `http://localhost:8080`)

---

## **Stopping the Services**

To stop and remove all containers, run:

```bash
docker-compose down
```

---

## **Troubleshooting**

- Ensure Docker is installed and running before executing the scripts.
- Verify that the ports configured in the `.env` file are not in use by other applications.
- Check the logs of the Docker containers for errors:
  ```bash
  docker-compose logs
  ```
- If PostgreSQL fails to start, ensure its hostname and port configurations in `.env` match those in `docker-compose.yml`.
- For any connection issues, verify user credentials and database names in the `.env` file.

---

## **Useful Links**

- [Odoo Documentation](https://www.odoo.com/documentation)
- [PostgreSQL Documentation](https://www.postgresql.org/docs/)
- [Adminer Official Site](https://www.adminer.org/)
- [Docker Documentation](https://docs.docker.com/)

---

## **License**

This project is open source and available under the [MIT License](LICENSE).

---

## **Contributing**

Contributions are welcome! Feel free to submit issues or pull requests to enhance the project.

---

### **Author**

- Neural Inverse Open Source Initiative

Enjoy effortless ERP/CRM deployment with Odoo Simplified Setup! 🚀


