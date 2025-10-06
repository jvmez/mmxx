# Next.js Starter - GitHub Pages Deployment

This is a Next.js starter project configured for deployment to GitHub Pages.

## Features

- ✅ Next.js 14 with App Router
- ✅ TypeScript support
- ✅ Tailwind CSS
- ✅ Static export for GitHub Pages
- ✅ GitHub Actions automatic deployment
- ✅ Responsive design

## Deployment

This project is automatically deployed to GitHub Pages whenever you push to the `main` branch.

### Manual Deployment Steps

1. **Push your code to GitHub:**
   ```bash
   git add .
   git commit -m "Deploy to GitHub Pages"
   git push origin main
   ```

2. **Enable GitHub Pages:**
   - Go to your repository settings
   - Navigate to "Pages" section
   - Select "GitHub Actions" as the source
   - The deployment will happen automatically via the workflow

3. **Your site will be available at:**
   ```
   https://jvmez.github.io/jvmez.github.io/
   ```

## Local Development

```bash
# Install dependencies
npm install

# Run development server
npm run dev

# Build for production
npm run build

# Preview production build
npm run start
```

## Configuration

The project is configured for static export with:
- `output: 'export'` in `next.config.js`
- Unoptimized images for static hosting
- Trailing slashes for GitHub Pages compatibility
- `.nojekyll` file to bypass Jekyll processing

## GitHub Actions Workflow

The deployment workflow (`.github/workflows/deploy.yml`) automatically:
1. Builds the Next.js application
2. Exports static files to the `out` directory
3. Deploys to GitHub Pages

## Customization

- Edit `app/page.tsx` to modify the homepage
- Update `app/layout.tsx` for global layout changes
- Modify `tailwind.config.ts` for styling customization
- Add new pages in the `app` directory

## Troubleshooting

If deployment fails:
1. Check the Actions tab in your GitHub repository
2. Ensure GitHub Pages is enabled in repository settings
3. Verify the workflow file is in `.github/workflows/`
4. Make sure you have the correct permissions for the repository
