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

### SSH
```text
Protocol: TCP
Port: 22
Source: My trusted IP address
Purpose: Server administration
```

### HTTP

```text
Protocol: TCP
Port: 80
Source: Internet
Purpose: Web traffic
```

### HTTPS

```text
Protocol: TCP
Port: 443
Source: Internet
Purpose: Secure web traffic
```

## 12. Access Control

Access control determines who can access a resource and what actions they are allowed to perform.

For a website, access control can include:

- User authentication
- Authorization
- File permissions
- Repository permissions
- Cloud access policies

The principle of least privilege should be followed by giving users and services only the permissions they need.

### Authentication

Authentication verifies the identity of a user.

For example, a website may ask for a username and password before allowing a user to access their account.

### Authorization

Authorization determines what an authenticated user is allowed to do.

For example:

- A normal user may view their profile.
- An administrator may manage users.
- A website visitor may view public pages.

Authentication answers:

"Who are you?"

Authorization answers:

"What are you allowed to do?"

### File Permissions

File permissions control who can read, write, or execute files.

Sensitive files should not be publicly accessible.

Examples of sensitive files include:

- Configuration files
- Password files
- Private keys
- API credentials
- Database credentials

### Repository Permissions

GitHub repository permissions should be configured carefully.

Only trusted users should be given permission to modify important project files.

Repository access should follow the principle of least privilege.

### Cloud Access Policies

Cloud resources should use appropriate access policies.

Users and services should receive only the permissions required for their tasks.

Unnecessary permissions should be removed.

### Least Privilege

Least privilege means giving a user, application, or service only the minimum permissions required to perform its job.

This reduces the possible damage if an account or service is compromised.

Example:

```text
User
  |
  v
Authentication
  |
  v
Identity verified
  |
  v
Authorization
  |
  v
Check permissions
  |
  v
Allow or deny access
```

## 13. Backup and Recovery

Backups are copies of important files and data that can be used when the original data is lost, damaged, deleted, or compromised.

Regular backups help protect against:

- Accidental deletion
- Hardware failure
- Malware
- Ransomware
- Configuration mistakes
- Server failure

### Website Backup

Important website files should be backed up regularly.

Examples include:

- HTML files
- CSS files
- JavaScript files
- Images
- Configuration files
- Database backups, if a database is used

### Backup Best Practices

- Keep regular backups.
- Store backups separately from the main system.
- Protect backups from unauthorized access.
- Test backups regularly.
- Keep more than one backup copy when possible.

### Recovery

Recovery is the process of restoring a website or system after a failure or security incident.

A basic recovery process can be:

```text
Identify the problem
       |
       v
Stop or isolate the affected system
       |
       v
Find a clean backup
       |
       v
Restore the required files
       |
       v
Test the website
       |
       v
Return the website to normal operation
```

## 14. Security Best Practices

Website security should be considered throughout development, deployment, and maintenance.

### Basic Security Practices

- Use HTTPS.
- Use strong authentication.
- Protect administrator accounts.
- Use strong passwords.
- Enable multi-factor authentication where available.
- Keep software and dependencies updated.
- Remove unnecessary services.
- Restrict unnecessary network ports.
- Protect sensitive files.
- Validate user input.
- Review permissions regularly.
- Keep backups.
- Monitor logs for suspicious activity.

### Protect Sensitive Information

Do not store sensitive information in public repositories.

Examples of sensitive information include:

- Passwords
- API keys
- Private keys
- Database credentials
- Access tokens
- Cloud credentials

Sensitive information should be stored using appropriate secret-management methods rather than directly inside source code.

### GitHub Security

When using GitHub:

- Do not commit passwords or API keys.
- Review repository permissions.
- Use strong authentication.
- Enable multi-factor authentication.
- Check repository contents before making them public.
- Remove accidentally exposed secrets immediately.
- Use `.gitignore` for files that should not be committed.

### User Input Security

If a website accepts user input through forms, the input should be validated.

Examples include:

- Name
- Email address
- Phone number
- Message

Input validation helps reduce security problems caused by unexpected or malicious input.

## 15. Git Version Control

Git is used to track changes made to the website project.

Git allows developers to:

- Track changes.
- Restore previous versions.
- Work on different versions of a project.
- Collaborate with other developers.
- Store project history.

### Basic Git Workflow

The basic workflow is:

```text
Edit files
    |
    v
git add
    |
    v
git commit
    |
    v
git push
    |
    v
GitHub repository
```


