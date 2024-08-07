# Local AI with Docker

This project sets up a simple local (CPU only) AI environment with Docker.

## Prerequisites

- Docker

## Instructions

### 1. Clone the GitHub Repository
Clone the GitHub repository for this project and change into the directory:

```sh
git clone https://github.com/mikeydiamonds/docker-AI-stack.git && cd docker-AI-stack
```

### 2. Run Docker Compose

Start the services using Docker Compose:

```sh
docker-compose up -d
```

### 7. Access the Application

Open your browser and navigate to [http://chat.localhost](http://chat.localhost).

You should now have access to the Open Web UI running locally on your Mac.

## Additional Information

- (**Open WebUI**)[https://docs.openwebui.com/] does have authentication built in but I have disabled the feature for this local only project. To enable, just remove `- WEBUI_AUTH=false` from `compose.yml`.
- (**Traefik**)[https://traefik.io/] is used as a reverse proxy to manage routing for the Open Web UI and SearXNG.
- (**SearXNG**)[https://github.com/searxng/searxng] is configured for web searches and integrated with the Open Web UI.

If you encounter any issues, refer to the documentation of the respective tools or the project's GitHub issues page for troubleshooting.

## Troubleshooting

- **Docker Issues**: Make sure Docker is running and you have granted necessary permissions. Adjust resource limits in the settings.
- **Model Pull Issues**: Ensure you have a stable internet connection while pulling the model using Ollama.
- **Network Issues**: If you can't access `http://chat.localhost`, verify your Docker network settings and ensure no other services are conflicting with port 80.

Feel free to open an issue on this GitHub repository if you encounter any problems not covered in this guide.

And above all, have fun with local AI!
