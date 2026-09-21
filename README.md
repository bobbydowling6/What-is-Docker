# What-is-Docker
# Questions
1. What happens when you docker run the same image twice?
When you execute docker run on the same image twice, Docker creates two completely separate, independent container instances.
2. What happens to files created inside a container when it stops?
When a container stops, files created or modified inside it remain saved within that specific container's writable layer.
3. How is the -p flag used to map ports?
The -p (or --publish) flag forwards network traffic from a port on your host machine (or Codespace environment) to a port inside the running container.

docker --version
Docker version 29.8.1, build 4a63305

Bypass Docker and run FastAPI directly
Recommended for Codespaces
Since GitHub Codespaces is already an isolated container environment, you can run your API directly using Python and Uvicorn without needing the Docker daemon at all:

Bash
cd app
pip install -r requirements.txt
uvicorn app:app --reload --port 8000