# Portfolio CI/CD Website

A responsive personal portfolio website built with **HTML, CSS, and JavaScript**, with an automated **CI/CD pipeline using GitHub Actions** and zero-cost deployment through **GitHub Pages**.

The purpose of this project is to demonstrate how a simple static website can be connected to a production-style deployment workflow where every change pushed to the `main` branch is automatically deployed.

---

## 🚀 Tech Stack

* HTML5
* CSS3
* JavaScript
* Git & GitHub
* GitHub Actions
* GitHub Pages

---

## 🔄 CI/CD Workflow

The deployment pipeline follows this flow:

```text
Developer
    │
    │ git push
    ▼
GitHub Repository
    │
    │ triggers workflow
    ▼
GitHub Actions
    │
    ├── Checkout repository
    │
    ├── Configure GitHub Pages
    │
    ├── Package website
    │
    └── Deploy
    ▼
GitHub Pages
    │
    ▼
Live Website
```

Whenever a change is pushed to the `main` branch, GitHub Actions automatically runs the deployment workflow.

No manual file uploads or deployment steps are required.

---

## ⚙️ How CI/CD Is Implemented

The workflow is defined in:

```text
.github/
└── workflows/
    └── deploy.yml
```

The workflow is triggered whenever code is pushed to `main`:

```yaml
on:
  push:
    branches:
      - main
```

It then:

1. Checks out the latest repository contents.
2. Configures GitHub Pages.
3. Packages the website files as a deployment artifact.
4. Deploys the artifact to GitHub Pages.

The project is a static website, so there is no compilation or build process required.

---

## 🧪 Automated Deployment

After making a change locally:

```bash
git add .
git commit -m "Update portfolio"
git push
```

GitHub Actions automatically detects the push and starts the deployment workflow.

The deployment can be monitored from:

```text
GitHub Repository
→ Actions
→ Deploy Portfolio
```

Once the workflow succeeds, the updated website is available through GitHub Pages.

---

## 🍴 Fork & Deploy Your Own Version

You can use this repository as a template for your own portfolio.

### 1. Fork the repository

Fork this repository to your own GitHub account.

### 2. Clone your fork

```bash
git clone https://github.com/YOUR-USERNAME/portfolio-cicd-website.git
cd portfolio-cicd-website
```

### 3. Customize the website

Edit the HTML, CSS and JavaScript files:

```text
index.html
style.css
script.js
```

Add your own assets inside:

```text
assets/
├── images/
└── resume/
```

### 4. Enable GitHub Pages

In your GitHub repository:

```text
Settings
→ Pages
→ Build and deployment
→ Source
→ GitHub Actions
```

### 5. Push your changes

```bash
git add .
git commit -m "Customize portfolio"
git push
```

GitHub Actions will automatically deploy your website.

Your portfolio will then be available at:

```text
https://YOUR-USERNAME.github.io/REPOSITORY-NAME/
```

---

## 📁 Project Structure

```text
portfolio-cicd-website/
│
├── .github/
│   └── workflows/
│       └── deploy.yml
│
├── assets/
│   ├── images/
│   └── resume/
│
├── index.html
├── style.css
├── script.js
├── .gitignore
└── README.md
```

---

## 💡 Why CI/CD?

Without CI/CD, deploying a static website can involve manually uploading or replacing files after every change.

With this setup:

```text
Code Change
     ↓
git push
     ↓
GitHub
     ↓
GitHub Actions
     ↓
Automatic Deployment
     ↓
Live Website
```

This provides a simple introduction to the same core principles used in larger software delivery pipelines:

* Version control
* Automated workflows
* Continuous integration
* Automated deployment
* Repeatable releases

---

## 💰 Cost

This project can be hosted at **zero cost** using:

* GitHub repository
* GitHub Actions
* GitHub Pages

The setup is particularly suitable for static websites that do not require a backend or database.

---

## 📌 Future Improvements

Possible extensions include:

* Custom domain
* Automated HTML/CSS validation
* Link checking in CI
* Lighthouse performance checks
* Automated testing
* Deployment notifications
* Preview deployments for pull requests

---

## 📄 License

This project is available for learning and personal use. Feel free to fork it, customize it, and use the CI/CD workflow for your own static website.
