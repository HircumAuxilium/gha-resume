# Deploy to GitHub Pages
This GitHub Actions workflow automates the deployment of a website to GitHub Pages. It publishes an index.html file (resume) formatted using a styles.css file.

## Workflow Details
- Name: Deploy to GitHub Pages
- Trigger: Triggered on push to the main branch and manually triggered using the workflow_dispatch event.
- Runs on: Ubuntu latest

## Workflow Steps
1. Checkout code: Checks out the code using actions/checkout@v4.
2. Deploy to GitHub Pages: Deploys the website using peaceiris/actions-gh-pages@v3.
  - GitHub Token: Uses a GitHub token stored in secrets (${{ secrets.RESUME_TOKEN }}) for authentication.
  - Publish Directory: Specifies the directory to publish (. indicates the root directory).

## Usage
To use this workflow:

1. Ensure your website files (`index.html`, `styles.css`, etc.) are in the root directory of your repository.
2. Add the GitHub Actions workflow file (e.g., `.github/workflows/deploy.yml`) with the provided workflow configuration.
3. Set up the `RESUME_TOKEN` secret in your repository settings with the required permissions for GitHub Pages deployment.

After pushing changes to the main branch or manually triggering the workflow, your website will be automatically deployed to GitHub Pages.


For more information about GitHub Pages deployment using actions-gh-pages, refer to the peaceiris/actions-gh-pages repository.
