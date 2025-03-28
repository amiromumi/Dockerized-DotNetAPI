# Dockerized DotNet API
A simple .NET API running inside a Docker container.

## How to run
1. Build the image: `docker build -t dockerized-dotnetapi .`
2. Run the container: `docker run -d -p 2501:80 --name mydockerapi-container dockerized-dotnetapi`
3. Open `http://localhost:2501` in your browser.
