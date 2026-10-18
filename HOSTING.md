# Project Hosting Documentation

## Project Name

Midhin Personal Website

## Technologies Used

- HTML
- CSS
- Git
- GitHub
- GitHub Pages

## 1. GitHub Hosting

The project source code is stored in a public GitHub repository.

Repository:

https://github.com/PGMIDHIN/Midhinpg-personal-website

The website contains multiple HTML pages and a CSS stylesheet.

The main files include:

- index.html
- about.html
- skills.html
- projects.html
- learning.html
- contact.html
- style.css

## 2. GitHub Pages Deployment

GitHub Pages is used to publish the static website.

The deployment configuration uses the main branch and GitHub Actions.

The deployment workflow:

1. The website files are stored in the GitHub repository.
2. Changes are committed and pushed to GitHub.
3. GitHub Actions starts the deployment workflow.
4. The website files are uploaded as a Pages artifact.
5. GitHub Pages deploys the artifact.
6. The website becomes available through the GitHub Pages URL.

Live Website:

https://pgmidhin.github.io/Midhinpg-personal-website/

## 3. HTTPS

The website is served using HTTPS.

HTTPS helps protect communication between the visitor's browser and the website from being viewed or modified in transit.

GitHub Pages provides HTTPS for the default GitHub Pages domain.

## 4. Cloud Hosting Basics

Cloud hosting means using computing and storage resources provided by a cloud provider through the internet.

Examples of cloud providers include:

- Amazon Web Services (AWS)
- Microsoft Azure
- Google Cloud

Cloud hosting can be used for websites, applications, databases, storage and other services.

## 5. AWS S3

Amazon S3 (Simple Storage Service) is an object storage service.

For a static website, HTML, CSS, JavaScript and other website files can be stored in an S3 bucket.

Basic architecture:

Internet
   |
   v
AWS S3
   |
   v
Static Website Files

S3 is suitable for static websites because the website does not require a server-side application to generate pages.

## 6. AWS EC2

Amazon EC2 (Elastic Compute Cloud) provides virtual servers in the AWS cloud.

An EC2 instance can run an operating system and software such as:

- Nginx
- Apache
- Application servers
- Databases
- Security tools

Basic architecture:

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

## 7. Security Groups

An AWS Security Group acts as a virtual firewall for an EC2 instance.

For a basic web server, common rules are:

| Protocol | Port | Purpose |
|----------|------|---------|
| HTTP | 80 | Web traffic |
| HTTPS | 443 | Secure web traffic |
| SSH | 22 | Server administration |

HTTP and HTTPS may need to be available to visitors.

SSH should normally be restricted to trusted IP addresses rather than being unnecessarily exposed to the entire internet.

Example:

SSH:
Port 22
Source: My trusted IP address

HTTP:
Port 80
Source: Internet

HTTPS:
Port 443
Source: Internet

## 8. Access Control

AWS IAM is used to manage identities and permissions.

Access should follow the principle of least privilege.

Users and services should receive only the permissions required to perform their tasks.

Examples include:

- User authentication
- Permission policies
- IAM roles
- Resource access control

## 9. Security Considerations

Basic security measures for cloud hosting include:

- Use HTTPS.
- Restrict administrative access.
- Avoid unnecessary open ports.
- Use strong authentication.
- Apply least-privilege permissions.
- Keep server software updated.
- Monitor access and activity.
- Protect credentials and secret keys.

## 10. Conclusion

The Midhin Personal Website is hosted using GitHub Pages and is publicly accessible through HTTPS.

GitHub Pages is suitable for this project because it is a static HTML and CSS website.

AWS S3 can also be used for static website hosting, while AWS EC2 can be used when a virtual server and server-side software are required.
