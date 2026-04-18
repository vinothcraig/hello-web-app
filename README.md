# Hello Web App

Simple Docker-based hello world application for DevOps learning.

## Files

- `index.html` - Simple hello world web page
- `Dockerfile` - Nginx-based Docker image
- `.github/workflows/ci-cd.yml` - GitHub Actions workflow

## Usage

Build locally:
```bash
docker build -t hello-web-app .
docker run -d -p 80:80 hello-web-app
```

## GitHub Secrets Required

For deployment job to work, add these repository secrets:
- `EC2_HOST` - Your EC2 instance IP/hostname
- `EC2_USER` - SSH username (e.g., ubuntu)
- `EC2_SSH_KEY` - SSH private key