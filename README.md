# GitHub Actions EC2 Deployment with Ansible

## Overview

This project automates the process of spinning up a new EC2 instance and configuring it with a demo HTML page every time a new commit is pushed to the `main` branch of a GitHub repository.

The automation leverages **GitHub Actions** for CI/CD and **Ansible** for server provisioning and configuration.

---

## How It Works

1. A **push** to the `main` branch triggers a **GitHub Actions** workflow.
2. The workflow:
   - Launches a new **EC2 instance** (Amazon Linux or Ubuntu).
   - Connects to the instance via SSH.
   - Uses **Ansible** to:
     - Install **Python** and **Git**.
     - Install and configure **NGINX**.
     - Deploy a **demo HTML page** to be served by NGINX.

---

## Technologies Used

- **GitHub Actions** — Workflow automation
- **Ansible** — Provisioning and configuration management
- **AWS EC2** — Hosting the server
- **NGINX** — Web server to serve the demo page
- **Python** and **Git** — Installed on the EC2 instance

---

## Requirements

- An AWS account with permissions to create EC2 instances.
- Ansible installed locally (or via the GitHub Action runner).
- GitHub repository with the configured GitHub Actions workflow.
- SSH keypair for accessing the EC2 instance.
- Proper IAM permissions (via environment variables or GitHub secrets).

---

## Project Structure

