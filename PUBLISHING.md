# Publishing To GitHub

This local repository is ready to publish as:

```text
awesome-agent-skills
```

Suggested visibility: public.

## Create The Empty GitHub Repository

Open:

```text
https://github.com/new
```

Use these settings:

- Repository name: `awesome-agent-skills`
- Visibility: Public
- Do not initialize with README, .gitignore, or license

## Push From This Local Repository

Replace `<your-github-username>` with your GitHub username:

```powershell
git remote add origin https://github.com/<your-github-username>/awesome-agent-skills.git
git push -u origin main
```

If `origin` already exists:

```powershell
git remote set-url origin https://github.com/<your-github-username>/awesome-agent-skills.git
git push -u origin main
```

