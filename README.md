# Portfolio Website

## Deployment Instructions

### Deploying to Vercel

1. **Create a Vercel Account**
   - Sign up at [vercel.com](https://vercel.com) if you don't have an account

2. **Install Vercel CLI** (Optional for command-line deployment)
   ```
   npm install -g vercel
   ```

3. **Deploy via Vercel Dashboard**
   - Go to [vercel.com/dashboard](https://vercel.com/dashboard)
   - Click "New Project"
   - Import your GitHub repository or upload your files
   - Configure project settings if needed
   - Click "Deploy"

4. **Deploy via Command Line** (Alternative)
   - Navigate to your project directory
   - Run `vercel login` and follow the prompts
   - Run `vercel` to deploy
   - Follow the prompts to configure your project

### Configuration

The `vercel.json` file in this project contains the necessary configuration for deployment:

```json
{
  "version": 2,
  "builds": [
    { "src": "*.html", "use": "@vercel/static" }
  ],
  "routes": [
    { "src": "/(.*)", "dest": "/index.html" }
  ]
}
```

This configuration ensures that:
- Static files are properly served
- All routes are directed to the index.html file for proper navigation

## Local Development

To run this website locally:

1. Clone the repository
2. Open the project folder
3. Open `index.html` in your browser

Alternatively, you can use a local server:

```
npx serve
```

or

```
python -m http.server
```