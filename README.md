# Dockerized DotNet API
A simple .NET API running inside a Docker container.

## How to Run (Using Docker CLI)
1. **Build the Docker image:**  
   ```sh
   docker build -t dockerized-dotnetapi .
   ```
2. **Run the Docker container:**  
   ```sh
   docker run -d -p 2501:80 --name mydockerapi-container dockerized-dotnetapi
   ```
3. **Access the API:**  
   - Open your browser and go to: [http://localhost:2501](http://localhost:2501)  
   - For environment check, visit: [http://localhost:2501/env](http://localhost:2501/env)

## How to Run (Using Docker Compose)
1. **Start the container:**  
   ```sh
   docker-compose up -d
   ```
2. **Stop and remove containers:**  
   ```sh
   docker-compose down
   ```
3. **Rebuild the image (if changes are made):**  
   ```sh
   docker-compose up --build -d
   ```
4. **Access the API:**  
   - Open your browser and go to: [http://localhost:2501](http://localhost:2501)  
   - For environment check, visit: [http://localhost:2501/env](http://localhost:2501/env)

## Environment Configuration
By default, the API runs in **Production mode** inside the Docker container.  
You can override this setting by passing an environment variable when running the container:

```sh
docker run -d -p 2501:80 -e ASPNETCORE_ENVIRONMENT=Development --name mydockerapi-container dockerized-dotnetapi
```

To verify the environment mode, open:  
- [http://localhost:2501/env](http://localhost:2501/env)

## Project Structure
```
Dockerized-DotNetAPI/
│-- Dockerfile
│-- docker-compose.yml
│-- Dockerized-DotNetAPI.csproj
│-- Program.cs
```

## Notes
- This project demonstrates a **basic** .NET API inside a Docker container.
- Supports both **Docker CLI** and **Docker Compose** for running the application.
- Ensure Docker is installed and running before executing the commands.

