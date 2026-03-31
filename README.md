# Portfolio Thesis Monitor

AI Agent Economy portfolio monitoring tool with signal engine, guardrails, and thesis journal.

## Deploy to DigitalOcean App Platform

### Option A: One-click from GitHub (recommended)

1. **Create a GitHub repo:**
   - Go to github.com → New Repository
   - Name it `portfolio-monitor` (private repo recommended)
   - Upload the contents of this folder (index.html and .do/app.yaml)

2. **Deploy on App Platform:**
   - Go to cloud.digitalocean.com/apps
   - Click "Create App"
   - Select "GitHub" as source
   - Authorize DigitalOcean to access your repo
   - Select your `portfolio-monitor` repo
   - App Platform auto-detects the `.do/app.yaml` config
   - Select the **Starter (Free)** plan for static sites
   - Click "Create Resources"

3. **Done.** You'll get a URL like `portfolio-monitor-xxxxx.ondigitalocean.app`

### Option B: Deploy via CLI

```bash
# Install doctl
brew install doctl  # macOS

# Authenticate
doctl auth init

# Create app from spec
doctl apps create --spec .do/app.yaml
```

### Option C: Just drag and drop

DigitalOcean App Platform also lets you upload files directly without GitHub:
1. Go to cloud.digitalocean.com/apps
2. Click "Create App"
3. Choose "Sample App" then edit to upload your own files
4. Upload index.html

## Usage

- Open the deployed URL in Chrome
- Go to **Data** tab
- Paste your screener TSV data or upload a file
- All data persists in your browser's localStorage
- Works on phone/tablet too

## Security Note

This is a static HTML file — no data leaves your browser. Your financial data stays in localStorage on whatever device you access it from. The DigitalOcean server only serves the HTML file itself.

If you want to access your data from multiple devices, you'd need to paste/upload data on each device separately.
