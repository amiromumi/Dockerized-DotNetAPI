# Dockerized DotNet API
A simple .NET API running inside a Docker container.

## How to Run
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
│-- Dockerized-DotNetAPI.csproj
│-- Program.cs
```

## Notes
- This project is meant to demonstrate a **basic** .NET API inside a Docker container.
- Make sure Docker is installed and running before executing the commands.

