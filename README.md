User Registration Application

Overview
This project provides a simple user registration system built with PHP and MySQL. It includes a registration form, database interaction, and basic password hashing. The application can be deployed using Docker and Ansible.


Key Features
User registration form.
Password hashing with bcrypt.
Basic database interaction.
Docker deployment using Ansible Playbook.
Ansible configuration for testing and production environments.

Files and Directory Structure

register.html: HTML file containing a simple form of Registration form with basic styling for a clean and user-friendly interface.

register.php: PHP script is responsible for handling user interface. It interacts with the database to store the credentials securely.

config.php: Configuration file containing database connection details.

prod_config.yml: Ansible playbook for deploying the application to a production server. It installs Docker, starts the Docker service, and runs the Docker container with the registration application on port 8081.

test_config.yml: Ansible playbook to configure testing and staging environments.

Application Deployment
After successfully creating the application and configuring the database, Docker is used to build and containerize the application. A Jenkins CICD pipeline is created to stage the Docker Container using Ansible Playbook on to the test server . After staging, a seperate CICD pipeline is created for automation testing using selenium. With successful automation testing it is deployed on to the production server with “prod_config.yml”.

	Also integrated GitHub Webhook so that the automation happens with a single commit on GitHub repository.




