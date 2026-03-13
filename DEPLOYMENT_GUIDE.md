# Deployment & Sharing Guide

Follow these steps to publish this workshop repository to GitHub and share it with your students.

## 1. Initialize Local Git Repository

Open your terminal in the `github-copilot-workshop-2026` directory:

```bash
cd github-copilot-workshop-2026
git init
git add .
git commit -m "Initial commit: Workshop structure and content"
```

## 2. Create GitHub Repository

1.  Go to [github.com/new](https://github.com/new).
2.  **Repository name**: `github-copilot-workshop-2026`.
3.  **Description**: "GitHub Copilot Advanced Practical Training Resources".
4.  **Public/Private**: Choose **Public** (easier for students) or **Private** (if proprietary).
5.  **Initialize**: Do **NOT** check "Add a README", .gitignore, or license (we already have them).
6.  Click **Create repository**.

## 3. Push to GitHub

Copy the commands from the "…or push an existing repository from the command line" section, or use these:

```bash
# Replace YOUR_USERNAME with your actual GitHub username
git remote add origin https://github.com/YOUR_USERNAME/github-copilot-workshop-2026.git
git branch -M main
git push -u origin main
```

## 4. Sharing with Students

### Option A: Public Repository
-   Simply share the URL: `https://github.com/YOUR_USERNAME/github-copilot-workshop-2026`
-   Students can `git clone` without needing an account.

### Option B: Private Repository
-   Go to **Settings** > **Collaborators**.
-   Click **Add people**.
-   Enter the usernames or email addresses of your students.
-   Alternatively, if you are in an Organization, you can add a Team.

## 5. Updates during Workshop
If you make changes during the live demo:

```bash
git add .
git commit -m "Update demo code"
git push
```
Students can then pull the changes:
```bash
git pull
```
