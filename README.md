# Hello World Nginx

Minimal Nginx server that serves **Hello World!**.

## Run locally

```bash
docker build -t hello-nginx .
docker run --rm -p 8080:80 hello-nginx
```

Open <http://localhost:8080>.

## Publish on GitHub Pages

GitHub Pages is static hosting, so it serves the same `index.html` but does not run
the Nginx container. After pushing this repository to GitHub:

1. Open **Settings → Pages** in the GitHub repository.
2. Under **Build and deployment**, choose **GitHub Actions** as the source.
3. Push to `main` (or re-run the **Deploy static site to GitHub Pages** workflow).
4. The public URL will be shown in the workflow output and will normally be
   `https://<your-github-username>.github.io/<repository-name>/`.

For a deployed Nginx server (rather than static Pages), publish the Docker image
to a container host such as Render, Fly.io, or a VPS.
