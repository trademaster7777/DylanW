# Git Deployment Workflow

## Initial Setup

1. **Initialize Git Repository**:
   ```bash
   git init
   git add .
   git commit -m "Initial commit: Dylan Wallace Resume Deck"
   ```

2. **Connect to GitHub** (recommended):
   ```bash
   git remote add origin https://github.com/yourusername/dylan-resume-deck.git
   git branch -M main
   git push -u origin main
   ```

## Deployment Workflows

### Option 1: Vercel with GitHub Integration

1. **Connect Repository to Vercel**:
   - Go to [vercel.com](https://vercel.com)
   - Import your GitHub repository
   - Vercel will auto-deploy on every push to main

2. **Custom Domain**:
   - Add your domain in Vercel dashboard
   - Update DNS settings as instructed

### Option 2: GitHub Pages

1. **Enable GitHub Pages**:
   - Go to repository Settings > Pages
   - Select source: Deploy from a branch
   - Choose main branch / root folder

2. **Custom Domain**:
   - Add CNAME file with your domain
   - Configure DNS with GitHub's IPs

### Option 3: Manual GoDaddy Upload

1. **Build for Production**:
   ```bash
   git archive --format=zip --output=deploy.zip HEAD
   ```

2. **Upload to GoDaddy**:
   - Extract deploy.zip
   - Upload contents to public_html via cPanel

## Git Workflow for Updates

### Making Changes

1. **Create Feature Branch**:
   ```bash
   git checkout -b update/slide-content
   ```

2. **Make Changes and Commit**:
   ```bash
   git add .
   git commit -m "Update: Add new project details to slide 8"
   ```

3. **Push and Create PR**:
   ```bash
   git push origin update/slide-content
   # Create Pull Request on GitHub
   ```

4. **Merge to Main**:
   ```bash
   git checkout main
   git pull origin main
   git merge update/slide-content
   git push origin main
   ```

### Quick Updates (Direct to Main)

```bash
# Make changes
git add .
git commit -m "Fix: Update contact information"
git push origin main
```

## Useful Git Commands

### Check Status
```bash
git status
git log --oneline
```

### Undo Changes
```bash
# Undo last commit (keep changes)
git reset --soft HEAD~1

# Undo changes to specific file
git checkout -- filename.html
```

### Branching
```bash
# List branches
git branch -a

# Delete branch
git branch -d branch-name
```

## File Management

### What to Commit
- ✅ All HTML files
- ✅ CSS and JS files
- ✅ Optimized images (JPG, PNG)
- ✅ Configuration files (vercel.json)
- ✅ Documentation (README.md)

### What NOT to Commit
- ❌ Original/unoptimized images
- ❌ Development notes
- ❌ System files (.DS_Store)
- ❌ Editor configs (.vscode)
- ❌ Temporary files

## Security Notes

- Never commit API keys or secrets
- Use environment variables for sensitive data
- Keep the .gitignore file updated
- Review commits before pushing

## Backup Strategy

1. **GitHub serves as primary backup**
2. **Keep local backups of source materials**
3. **Export presentation periodically**:
   ```bash
   git archive --format=zip --output=backup-$(date +%Y%m%d).zip HEAD
   ```

