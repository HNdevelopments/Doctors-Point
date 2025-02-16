npm run db:push
```

### 2. GitHub Repository Configuration
1. Go to repository Settings → Secrets and variables → Actions
2. Add these required secrets:
   - `DATABASE_URL`: Your external PostgreSQL connection URL
   - `SESSION_SECRET`: A secure random string for session management
   - `MASTER_PASSWORD`: Admin password for managing doctors
   - `VITE_API_URL`: Will be your GitHub Pages URL (https://[username].github.io/[repo-name])

### 3. GitHub Pages Setup
1. Go to repository Settings → Pages
2. Source: Deploy from a branch
3. Branch: gh-pages → /(root) → Save

### 4. Deployment Process
The existing workflow in `.github/workflows/deploy.yml` will:
- Trigger on pushes to main branch
- Build the frontend
- Deploy to GitHub Pages
- Use the configured secrets for environment variables

### 5. Verify Deployment
1. Push your code to trigger deployment:
```bash
git add .
git commit -m "Configure GitHub Pages deployment"
git push origin main