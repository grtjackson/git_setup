# Git Setup Guide: Working with a New GitHub Account and Repository

## 1. Configure Your Git Identity
Before pushing to GitHub, ensure your local Git is set with your new account’s identity:

```bash
git config --global user.name "Your Name"
git config --global user.email "youremail@example.com"
```

## 2. Set Up SSH Keys for GitHub (Preferred Method)

1. **Generate a new SSH key:**
```bash
ssh-keygen -t ed25519 -C "youremail@example.com"
```
Press Enter through prompts.

2. **Add your SSH key to GitHub:**
- Copy the public key:
```bash
cat ~/.ssh/id_ed25519.pub
```
- Go to GitHub → Settings → SSH and GPG keys → New SSH key.
- Paste and save.

3. **Test your SSH connection:**
```bash
ssh -T git@github.com
```
You should see: `Hi username! You've successfully authenticated.`

## 3. Create a New Repository on GitHub
- Create a new repo on GitHub (don’t initialize with README if you have local files).

## 4. Set Up the Local Repository

**If starting from an existing folder:**
```bash
cd /path/to/project
git init
git checkout -b main  # create main branch
```

**If cloning an empty GitHub repo:**
```bash
git clone git@github.com:username/reponame.git
```

## 5. Add Remote and Push
```bash
git remote add origin git@github.com:username/reponame.git
git add .
git commit -m "Initial commit"
git push -u origin main
```

## 6. Handle Conflicts (if needed)
If you see:
```
Updates were rejected because the remote contains work that you do not have locally
```
Run:
```bash
git pull origin main --allow-unrelated-histories
# Resolve conflicts if prompted
git add .
git commit -m "Merge remote main"
git push -u origin main
```

Or to force overwrite remote history:
```bash
git push -u origin main --force
```

## 7. HTTPS Fallback
If SSH fails, set remote to HTTPS:
```bash
git remote set-url origin https://github.com/username/reponame.git
```
Git will prompt for username and personal access token (PAT) on push.

## 8. Verify
Go to your GitHub repo page. You should see your files and commits.

---
