# Setup Instructions for your Personal Website

You have successfully set up the local environment for your personal website using the `al-folio` template.

## Next Steps to Publish on GitHub

1.  **Create a Repository on GitHub**
    *   Go to [GitHub.com](https://github.com) and create a new repository.
    *   **Repository Name:** `Jinsook-Jennie-Lee.github.io` (This is important! It must match exactly).
    *   **Public/Private:** Public is easier for GitHub Pages, but Private works with Pro. Public is recommended for personal sites.
    *   **Initialize:** Do *not* initialize with README, .gitignore, or License. Create an empty repository.

2.  **Push your Local Code**
    Open your terminal in this directory (`/Users/jennie/Desktop/personal_website`) and run the following commands:

    ```bash
    # Add the remote repository
    git remote add origin https://github.com/Jinsook-Jennie-Lee/Jinsook-Jennie-Lee.github.io.git

    # Stage all files
    git add .

    # Commit
    git commit -m "Initial setup of al-folio website"

    # Rename branch to main if not already
    git branch -M main

    # Push to GitHub
    git push -u origin main
    ```

3.  **Configure GitHub Actions**
    *   Go to your new repository on GitHub.
    *   Click on the **Actions** tab.
    *   Click the button to **Enable GitHub Actions** (if prompted).
    *   Go to **Settings** -> **Actions** -> **General**.
    *   Scroll down to **Workflow permissions**.
    *   Select **Read and write permissions**.
    *   Click **Save**.

4.  **Trigger Deployment**
    *   Make a small change to a file (e.g., edit `_config.yml` or a blog post) and push it, OR just wait. The initial push might have triggered a failure if permissions weren't set yet.
    *   To manually trigger: Go to **Actions** tab -> **Deploy** workflow -> **Run workflow**.

5.  **Configure GitHub Pages**
    *   Once the "Deploy" action completes successfully (it will create a `gh-pages` branch), go to **Settings** -> **Pages**.
    *   Under **Build and deployment** -> **Source**, select **Deploy from a branch**.
    *   Under **Branch**, select `gh-pages` and `/ (root)`.
    *   Click **Save**.

Your website should now be live at [https://Jinsook-Jennie-Lee.github.io](https://Jinsook-Jennie-Lee.github.io).

## Local Development

To preview changes locally:

```bash
bundle exec jekyll serve
```

Then open [http://localhost:4000](http://localhost:4000) in your browser.
