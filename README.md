# TASK-3
# terraform-docker-container

# Deploying NGINX with Terraform and Docker

In this project, I used **Terraform** to automate the process of pulling an NGINX Docker image and running it as a container locally.

# What is Terraform?

* Terraform is an open-source **Infrastructure as Code (IaC)** tool developed by HashiCorp.  
* It allows you to define and provision infrastructure using simple configuration files, instead of doing everything manually.

# Why I Used Terraform Here

- To **automate** the creation of a Docker container  
- To **standardize** the setup (so anyone can recreate it easily)  
- To practice real-world DevOps skills using Terraform with Docker  
- Because using code for infrastructure makes it **reproducible, version-controlled, and efficient**

# Technologies Used

- **Terraform** – Infrastructure as Code (IaC) tool  
- **Docker** – Containerization platform  
- **NGINX** – Lightweight web server used for testing  

# Prerequisites
- Docker installed and running  
- Terraform installed (v1.0 or above)

# Terraform Configuration

Create a file named `main.tf` and paste this code:

![Screenshot 2025-04-10 130518](https://github.com/user-attachments/assets/1bd9b664-e623-40f6-acc1-ca015ca0fde9)

# Steps to Run
Initialize Terraform
* terraform init

![Screenshot 2025-04-10 130539](https://github.com/user-attachments/assets/27e9d56b-ee4d-4f4d-ade3-230836329e5e)

Apply the Configuration
* terraform apply
* Type yes when prompted.

![Screenshot 2025-04-10 130556](https://github.com/user-attachments/assets/417cd24d-10db-4617-9eb8-901cf2cfd4a7)

![Screenshot 2025-04-10 130610](https://github.com/user-attachments/assets/da53c9c4-9610-46ce-89ad-c9354cb0d086)

Open your browser and visit:
* http://localhost:8080
* 
![Screenshot 2025-04-10 130722](https://github.com/user-attachments/assets/dbdc6e20-da84-431b-a975-c2679fa27a16)

To Destroy the Setup
If you want to remove everything created by Terraform:
* terraform destroy

![Screenshot 2025-04-10 130655](https://github.com/user-attachments/assets/fb3eadd0-fe74-4e47-9795-a032f125fee6)

![Screenshot 2025-04-10 132800](https://github.com/user-attachments/assets/394ce15f-5e6d-4c71-ab4d-26526bb439e2)

# Understanding the Code
Here’s what each block does:
* terraform & provider: Sets up the Docker provider so Terraform can interact with Docker.
* docker_image: Pulls the official NGINX image from Docker Hub.
* docker_container: Creates a container named asma-nginx-container from that image and exposes it on port 8080.

# Terraform Commands and What They Do
terraform init
→ Initializes the working directory and downloads necessary provider plugins (like Docker)

terraform fmt
→ Formats the Terraform code to make it clean and readable

terraform validate
→ Checks for syntax errors or misconfigurations in the code

terraform plan
→ Shows a preview of what Terraform will create or change

terraform apply
→ Actually creates the resources (container, image) as defined in the code
→ Type yes when asked for confirmation

terraform destroy
→ Destroys all resources created by Terraform (removes the container & image)



