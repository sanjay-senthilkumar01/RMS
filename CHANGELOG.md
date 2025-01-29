# Changelog

## [1.0.0] - YYYY-MM-DD
### Initial Release
- Launched the Odoo Simplified Setup project.
- Included support for Odoo 17.0, PostgreSQL 16, and Adminer 4.8.1.
- Dockerized setup using Docker Compose for seamless deployment.
- One-command deployment for quick setup.
- Cross-platform support: Windows, Linux, and macOS.
- Customizable environment variables for tailored configurations.
- Included lightweight database management with Adminer.

## [1.0.1] - YYYY-MM-DD
### Enhancements & Fixes
- Improved error handling in `build_and_run.sh` and `build_and_run.bat`.
- Updated `.env.example` with clearer default values.
- Enhanced documentation for deployment steps and troubleshooting.
- Minor optimizations in `docker-compose.yml` for better performance.

## [1.0.2] - YYYY-MM-DD
### New Features
- Added support for external database connections.
- Introduced logging for better debugging.
- Improved modularity for adding custom Odoo modules.
- Enhanced security by allowing custom PostgreSQL credentials.

## [1.1.0] - YYYY-MM-DD
### Major Update
- Restructured the project directory for better maintainability.
- Implemented versioning for Docker images to ensure stability.
- Added a health check mechanism for containers.
- Improved compatibility with Odoo community and enterprise editions.

## [1.1.1] - YYYY-MM-DD
### Bug Fixes
- Fixed permission issues in `build_and_run.sh`.
- Resolved database connectivity issues when restarting containers.
- Updated Adminer version to the latest stable release.

## [Upcoming]
### Planned Features
- Support for automated backups and restore functionality.
- Integration with third-party authentication systems.
- Enhanced CI/CD pipeline for seamless updates.
- Improved scalability for high-load environments.

---
For detailed updates and contributions, visit our [GitHub Repository](https://github.com/OpenSrc-NeuralInverse/Odoo-Simplified-Setup).
