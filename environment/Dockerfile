# Pin the base image and the repository commit.
FROM python:3.12-slim-bookworm

# tmux is required: the agent works in a tmux session. Keep it in the image.
RUN apt-get update && apt-get install -y --no-install-recommends git tmux && rm -rf /var/lib/apt/lists/*
WORKDIR /app
RUN git clone https://github.com/ralphdelara/GoCobalt . && git checkout main
RUN pip install --no-cache-dir -e .
