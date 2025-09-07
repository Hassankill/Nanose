# Use the official Node.js 20 image
FROM node:20-bookworm

# Set the working directory
WORKDIR /workspace

# Install dependencies for shadcn-ui and development tools
RUN apt-get update && apt-get install -y \
    git \
    curl \
    && rm -rf /var/lib/apt/lists/*

# Set up npm to use the correct user
RUN npm config set prefix /usr/local

# Create a non-root user
RUN useradd -m -s /bin/bash vscode
RUN chown -R vscode:vscode /workspace
USER vscode

# Set the default command
CMD ["sleep", "infinity"]
