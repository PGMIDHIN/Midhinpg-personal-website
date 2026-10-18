# Project Hosting Documentation

## Project Name

Midhin Personal Website

---

## Technologies Used

- HTML
- CSS
- Git
- GitHub
- GitHub Pages
- GitHub Actions
- HTTPS

---

# 1. Project Overview

The Midhin Personal Website is a static personal website developed using HTML and CSS.

The website contains information about my background, cybersecurity skills, projects, learning journey, and contact details.

The website consists of multiple pages and is designed to be responsive, simple, accessible, and easy to navigate.

The main website pages are:

- Home
- About
- Skills
- Projects
- Learning
- Contact

---

# 2. GitHub Hosting

The project source code is stored in a public GitHub repository.

GitHub is a platform used to store, manage, and collaborate on source code using Git.

The project repository is:

https://github.com/PGMIDHIN/Midhinpg-personal-website

The repository contains the following main website files:

- index.html
- about.html
- skills.html
- projects.html
- learning.html
- contact.html
- style.css
- favicon.png

The repository also contains the GitHub Actions workflow used for deployment.

---

# 3. GitHub Pages Deployment

GitHub Pages is used to publish the static website.

The project uses the `main` branch and GitHub Actions for deployment.

The deployment process is:

1. The website files are created using HTML and CSS.
2. The files are stored in the GitHub repository.
3. Changes are committed to the repository.
4. Changes are pushed to the `main` branch.
5. GitHub Actions starts the deployment workflow.
6. The workflow checks out the repository files.
7. GitHub Pages prepares the website files for deployment.
8. The website files are uploaded as a Pages artifact.
9. GitHub Pages deploys the artifact.
10. The website becomes publicly accessible through the GitHub Pages URL.

The live website is:

https://pgmidhin.github.io/Midhinpg-personal-website/

---

# 4. Hosting Method Used for This Project

The actual deployment of this project was completed using GitHub Pages.

GitHub Pages is suitable for this project because the website is a static website consisting primarily of HTML, CSS, images, and other static files.

No server-side application is required to generate the pages.

The final hosting architecture is:

Internet
   |
   v
GitHub Pages
   |
   v
Midhin Personal Website
   |
   +-- index.html
   +-- about.html
   +-- skills.html
   +-- projects.html
   +-- learning.html
   +-- contact.html
   +-- style.css
   +-- favicon.png

The website is publicly accessible through the GitHub Pages URL.

---

# 5. HTTPS

The website is served using HTTPS.

HTTPS stands for Hypertext Transfer Protocol Secure.

HTTPS helps protect communication between a visitor's browser and the website by encrypting the connection.

The GitHub Pages website is accessible through an HTTPS URL:

https://pgmidhin.github.io/Midhinpg-personal-website/

Using HTTPS is important because it helps protect data while it is being transferred between the user's browser and the website.

---

# 6. GitHub Actions

GitHub Actions is used to automate the deployment process.

The project contains a workflow inside:

`.github/workflows/`

The workflow performs the following major operations:

1. Checks out the repository.
2. Configures GitHub Pages.
3. Uploads the website files as a deployment artifact.
4. Deploys the artifact to GitHub Pages.

The workflow is triggered when changes are pushed to the `main` branch.

A manual workflow dispatch option is also available.

This provides an automated deployment process instead of manually uploading the website every time a change is made.

---

# 7. Cloud Hosting Basics

Cloud hosting means using computing, storage, and networking resources provided by a cloud service provider through the internet.

Cloud platforms can be used to host:

- Websites
- Web applications
- Databases
- Files
- Virtual machines
- APIs
- Other online services

Examples of major cloud service providers include:

- Amazon Web Services (AWS)
- Microsoft Azure
- Google Cloud

Cloud hosting allows applications and websites to use infrastructure provided by a cloud provider instead of relying only on a physical server owned by the developer.

---

# 8. AWS S3

AWS S3 stands for Amazon Simple Storage Service.

S3 is an object storage service provided by Amazon Web Services.

S3 can be used to store static website files such as:

- HTML
- CSS
- JavaScript
- Images
- Documents
- Other static files

For a static website, the basic architecture can be represented as:

Internet
   |
   v
AWS S3
   |
   v
Static Website Files
   |
   +-- HTML
   +-- CSS
   +-- JavaScript
   +-- Images

S3 is suitable for static websites because the website does not require a server-side application to generate the pages.

---

# 9. AWS EC2

AWS EC2 stands for Amazon Elastic Compute Cloud.

EC2 provides virtual servers in the AWS cloud.

An EC2 instance can run an operating system and different types of software.

For example, an EC2 instance can run:

- Nginx
- Apache
- Application servers
- Databases
- Security tools
- Other server software

A basic EC2 website architecture can be represented as:

Internet
   |
   v
Security Group
   |
   v
EC2 Instance
   |
   v
Web Server
   |
   v
Website

Unlike a simple static hosting service, EC2 provides a virtual server where the administrator can install and configure software.

---

# 10. Static Hosting vs Server Hosting

A static website mainly consists of files that are delivered to the user's browser.

Examples:

- HTML
- CSS
- JavaScript
- Images

The Midhin Personal Website is a static website.

A dynamic website can contain server-side processing.

For example:

- PHP
- Node.js
- Python
- Databases
- Server-side APIs

A simple comparison is:

| Static Hosting | Server/Dynamic Hosting |
|---|---|
| Mainly serves static files | Runs server-side software |
| Simple to deploy | More configuration required |
| Suitable for HTML/CSS websites | Suitable for dynamic applications |
| Example: GitHub Pages | Example: EC2 |

---

# 11. Security Groups

An AWS Security Group acts as a virtual firewall for an EC2 instance.

It controls network traffic that is allowed to reach the instance.

For a basic web server, common ports include:

| Protocol | Port | Purpose |
|---|---:|---|
| HTTP | 80 | Web traffic |
| HTTPS | 443 | Secure web traffic |
| SSH | 22 | Server administration |

HTTP and HTTPS may need to be accessible to website visitors.

SSH is used for remote administration of an EC2 server.

SSH access should normally be restricted to trusted IP addresses instead of unnecessarily allowing access from the entire internet.

Example security configuration:

# SSH

```text

Protocol: TCP
Port: 22
Source: My trusted IP address
Purpose: Server administration

# 12. Access Control

Access control determines who can access a resource and what actions they are allowed to perform.

AWS IAM stands for Identity and Access Management.

IAM can be used to manage:

- Users
- Roles
- Permissions
- Policies
- Access to AWS resources

A basic security principle is **least privilege**.

Least privilege means giving a user or service only the permissions required to perform its intended task.

For example, a person who only needs to upload website files should not automatically receive unnecessary administrative permissions.

---

# 13. Public and Private Access

Websites need to be accessible to visitors, but administrative resources should not be unnecessarily exposed.

For a public website:

```text
Website
   |
   v
Public visitors
   |
   v
HTTP / HTTPS

Administrator
   |
   v
Restricted access
   |
   v
Server


# 14. Basic Cloud Security Practices

Basic security practices for cloud hosting include:

- Use HTTPS whenever possible.
- Restrict administrative access.
- Avoid unnecessary open ports.
- Use strong authentication.
- Apply least-privilege permissions.
- Keep server software updated.
- Protect AWS credentials.
- Never publish secret keys or passwords in a GitHub repository.
- Monitor access and activity.
- Remove or disable resources that are no longer required.
- Review permissions regularly.

Cloud resources should be configured according to the principle of least privilege.

---

# 15. Deployment and Update Process

The website can be updated by modifying the files in the project repository.

The general workflow is:

```text
Edit Website
     |
     v
Save Changes
     |
     v
Git Commit
     |
     v
Push to GitHub
     |
     v
GitHub Actions
     |
     v
GitHub Pages Deployment
     |
     v
Updated Live Website

# 16. Website Verification

After deployment, the website was tested using the public GitHub Pages URL.

The website successfully loads in a web browser and the different pages can be accessed through the navigation menu.

The website was also tested using Google Chrome Lighthouse.

The Lighthouse Performance score reached:

**100/100**

The performance testing was performed using an Incognito browser session to avoid interference from browser extensions and stored browsing data.

This confirms that the website meets the assignment requirement of achieving a Performance score above 90.

---

# 17. Project Hosting Security

The project follows basic security practices appropriate for a static personal website.

The website:

- Uses HTTPS.
- Does not require server-side administrative access.
- Does not expose unnecessary server ports.
- Does not store passwords or secret keys in the repository.
- Uses GitHub for source-code management.
- Uses GitHub Pages for static website deployment.

For cloud-hosted server environments such as EC2, security groups and restricted administrative access would be used to control network access.

---

# 18. Advantages of GitHub Pages for This Project

GitHub Pages is suitable for this project because:

- The website is static.
- The project files are already stored in GitHub.
- Deployment can be automated using GitHub Actions.
- The website can be accessed publicly.
- HTTPS is available.
- Website updates can be deployed from repository changes.

It is a simple hosting solution for a personal static website.

---

# 19. Cloud Hosting Concepts Studied

As part of this project, the following cloud-hosting concepts were studied:

- Cloud hosting
- Static website hosting
- AWS S3
- AWS EC2
- Security Groups
- Network ports
- HTTP
- HTTPS
- SSH
- IAM
- Access control
- Least privilege
- Public and private access
- Basic cloud security

These concepts provide an understanding of how websites can be hosted using cloud infrastructure.

---

# 20. Conclusion

The Midhin Personal Website was successfully hosted on GitHub using GitHub Pages.

The project source code is maintained in a GitHub repository, and GitHub Actions is used to automate the deployment process.

The live website is accessible through HTTPS.

Cloud hosting concepts were also studied, including AWS S3 for static website hosting and AWS EC2 for virtual server hosting.

Security concepts including Security Groups, network ports, IAM, access control, and least privilege were studied as part of the project-hosting process.

The project demonstrates the complete basic workflow of developing, storing, deploying, testing, and documenting a static website.

---

# Project Links

## GitHub Repository

https://github.com/PGMIDHIN/Midhinpg-personal-website

## Live Website

https://pgmidhin.github.io/Midhinpg-personal-website/

## Lighthouse Performance

**100/100**

---

# Topic 4 Completion Summary

### 4a. Host the project on GitHub

**Completed.**

The project is stored in a public GitHub repository and deployed through GitHub Pages.

### 4b. Introduce cloud hosting basics

**Completed as a learning/documentation activity.**

AWS S3 and AWS EC2 were studied as examples of cloud hosting services.

### 4c. Document the hosting process, including basic security groups and access

**Completed.**

The documentation covers GitHub Pages deployment, HTTPS, AWS Security Groups, network ports, IAM, access control, least privilege, and basic cloud security practices.


