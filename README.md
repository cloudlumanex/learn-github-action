# GitHub Actions CI/CD for Nginx Deployment on AWS EC2

This project demonstrates how to automate the deployment of a personal `index.html` page to an **Ubuntu EC2 instance** running **Nginx** using **GitHub Actions**. It showcases a CI/CD workflow for DevOps engineers and those exploring AI automation.

---

## Project Overview

- **Objective:** Automatically deploy an HTML website to an AWS EC2 instance whenever code is pushed to the `main` branch.  
- **Tools & Services Used:**
  - GitHub Actions (CI/CD)
  - appleboy/ssh-action for remote SSH execution
  - Ubuntu EC2 instance on AWS
  - Nginx web server
  - webfactory/ssh-agent for secure key handling
- **Use Case:** Learn DevOps automation and practice deploying web content using CI/CD pipelines.

---

## Features

- Installs and configures Nginx on an Ubuntu server
- Copies a custom `index.html` from the GitHub repository to the server
- Sets proper ownership for Nginx to serve the page
- Automatically restarts Nginx after deployment
- Verifies deployment by listing and displaying the deployed HTML file

---

## Workflow Details

1. **Checkout Code:** Pulls the repository contents using `actions/checkout`.
2. **Setup SSH:** Uses `webfactory/ssh-agent` to securely authenticate with the EC2 instance.
3. **Deploy Nginx:** Installs and configures Nginx on the server if not already installed.
4. **Deploy index.html:** Copies the HTML file from the repo to `/var/www/html/`.
5. **Verify Deployment:** Checks the deployed file exists and displays its content via SSH.

---

## Repository Structure

├── .github/
│ └── workflows/
│ └── deploy-nginx.yml # GitHub Actions workflow
├── index.html # Personal website
└── README.md # Project documentation


## Sample index.html

This HTML page introduces you as a **DevOps Engineer exploring AI automation**:

```html
<h1>Hi, I'm Emmanuel</h1>
<p>DevOps Engineer | Exploring AI & Automation</p>

```

