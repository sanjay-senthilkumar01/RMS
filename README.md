# Open Source Documentation: Odoo Simplified Setup

Welcome to the **Odoo Simplified Setup** project! This open-source initiative is designed to streamline the deployment of **Odoo 17.0**, **PostgreSQL 16**, and **Adminer 4.8.1** using Docker. It is tailored for developers and businesses seeking a quick, reliable way to implement an ERP/CRM system.

This project is developed by the **Neural Inverse Developer Team** as part of the **Neural Inverse OpenSrc **, with the goal of making ERP/CRM deployment accessible and efficient for everyone.

---

## Key Features

- **One-Command Deployment**: Effortlessly deploy a complete Odoo environment.
- **Dockerized Setup**: Ensures consistent and isolated environments.
- **Customizable**: Environment variables and configuration options for tailored deployments.
- **Cross-Platform Support**: Works seamlessly on Windows, Linux, and macOS.
- **Lightweight Database Management**: Includes Adminer for easy PostgreSQL administration.

---

## System Overview

This project deploys the following components:

1. **Odoo 17.0**: A powerful open-source ERP/CRM solution.
2. **PostgreSQL 16**: The reliable database backend for Odoo.
3. **Adminer 4.8.1**: A user-friendly database management tool.

All services are containerized and managed using Docker Compose for simplicity and scalability.

---

## Getting Started

Follow these steps to deploy the Odoo Simplified Setup:

### **Requirements**

- **Docker**: Ensure Docker is installed and running on your system.
- **Basic Command-Line Knowledge**: Familiarity with running scripts and Docker commands.

### **Step 1: Clone the Repository**

```bash
git clone https://github.com/OpenSrc-NeuralInverse/Odoo-Simplified-Setup.git
cd Odoo-Simplified-Setup
```

### **Step 2: Configure the Environment**

1. Rename the provided `.env.example` file to `.env`:
   ```bash
   mv .env.example .env
   ```

2. Customize the `.env` file as needed. Default values are provided:

   ```env
   POSTGRES_USER=postgres
   POSTGRES_PASSWORD=postgres
   POSTGRES_DB=postgres
   ODOO_DB_USER=odoo
   ODOO_DB_PASSWORD=odoo
   ODOO_PORT=8069
   ADMINER_PORT=8080
   ```

3. Update variables in the `build_and_run.sh` or `build_and_run.bat` scripts if necessary.

### **Step 3: Deploy the Setup**

#### For Linux/Mac:

1. Make the script executable:
   ```bash
   chmod +x ./build_and_run.sh
   ```

2. Run the script:
   ```bash
   ./build_and_run.sh
   ```

#### For Windows:

1. Execute the batch script:
   ```
   build_and_run.bat
   ```

---

## Accessing the Services

- **Odoo Web Interface**: [http://localhost:8069](http://localhost:8069)
- **Adminer Database Management**: [http://localhost:8080](http://localhost:8080)

---

## Customization Options

You can modify the following parameters in the `.env` file:

- **PostgreSQL**:
  - `POSTGRES_USER`, `POSTGRES_PASSWORD`, `POSTGRES_DB`
- **Odoo**:
  - `ODOO_PORT`, `ODOO_DB_USER`, `ODOO_DB_PASSWORD`
- **Adminer**:
  - `ADMINER_PORT`

---

## Troubleshooting

- **Docker Not Running**: Ensure Docker is installed and running before deploying.
- **Port Conflicts**: Check that the ports in `.env` are not in use by other applications.
- **Container Logs**: Use `docker-compose logs` to debug issues.
- **Connection Errors**: Verify database credentials and configurations in the `.env` file.

---

## Project Structure

- `build_and_run.sh`: Shell script for Linux/Mac setup.
- `build_and_run.bat`: Batch script for Windows setup.
- `docker-compose.yml`: Docker Compose configuration for all services.
- `.env.example`: Example environment variables.
- `README.md`: Quick setup guide.

---

## For Developers

### Extending the Project

1. **Add Custom Modules**:
   - Place custom Odoo modules in the `addons` directory.
   - Update `docker-compose.yml` to include the new module paths.

2. **Modify Configuration**:
   - Edit the `.env` file or directly update `docker-compose.yml`.

3. **Rebuild Containers**:
   ```bash
   docker-compose down
   docker-compose up --build
   ```

### Contributing

We welcome contributions! Here’s how you can help:

1. Fork the repository and create a feature branch.
2. Submit a pull request with your changes.
3. Report issues or suggest features via GitHub Issues.

---

## For Businesses

### Use Cases

1. **ERP Deployment**: Quickly deploy Odoo to manage business operations.
2. **CRM Integration**: Centralize customer data and interactions.
3. **Database Management**: Use Adminer for simplified database tasks.

### Benefits

- **Cost-Effective**: No licensing fees for open-source tools.
- **Scalable**: Deploy additional services as your business grows.
- **Customizable**: Tailor the setup to your specific needs.

---

## Credits

This project leverages the following tools:

- **Odoo 17.0**: [Odoo](https://www.odoo.com/) - A robust open-source ERP/CRM system.
- **PostgreSQL 16**: [PostgreSQL](https://www.postgresql.org/) - An advanced, open-source relational database.
- **Adminer 4.8.1**: [Adminer](https://www.adminer.org/) - A lightweight database management tool.
- **Docker & Docker Compose**: [Docker](https://www.docker.com/) - For containerization and orchestration.

Special thanks to the developers and maintainers of these tools for enabling this project.

---

## License

This project is licensed under the [MIT License](LICENSE), making it free for commercial and personal use.

---

## Support

For assistance, reach out to the development team via:
- **Email**: support@neuralinverse.com
- **GitHub Issues**: [Submit an issue](https://github.com/YourOrganization/YourRepo/issues)

---

Enjoy seamless ERP/CRM deployment with **Odoo Simplified Setup**! 🚀


