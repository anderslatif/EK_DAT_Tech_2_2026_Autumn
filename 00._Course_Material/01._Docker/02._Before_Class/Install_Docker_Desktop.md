# Docker Desktop installation guide

This guide will help you install Docker Desktop on your machine (**MacOS**, **Windows** or **Linux**).

---

## Step 1: Download Docker Desktop

1. Go to the [Docker Desktop download page](https://www.docker.com/products/docker-desktop/). [Alternative link](https://docs.docker.com/get-started/get-docker/)

2. Choose the version for your operating system (Windows, macOS, or Linux) and download the installer. For Apple M-chips, choose the version for Apple Silicon.

---

## Step 2: Install Docker Desktop

### Installation guide for MacOS:

1. Follow step 2 through 7 [here](https://docs.docker.com/desktop/install/mac-install/).

### Installation guide for Windows:

1. Install WSL 2 (Windows Subsystem for Linux) if you haven't already. You can follow the instructions [here](https://docs.docker.com/desktop/setup/install/windows-install/#wsl-verification-and-setup).

2. Follow step 2-6 [here](https://docs.docker.com/desktop/setup/install/windows-install/#install-docker-desktop-on-windows).


## Step 3: Verify Docker Installation

1. Open a terminal (Windows: GitBash, MacOS: Terminal).

2. Run the following command to check if Docker is installed correctly:

    ```bash
    docker --version
    ```

You should see the Docker version information displayed in the terminal.

## Step 4: Hello world with Docker

1. To verify that Docker is running correctly, you can run a simple "Hello World" container. Run the following command in your terminal:
    ```bash
    docker run hello-world
    ```

2. If Docker is installed correctly, you should see a the following mesasage:
    ```bash
    Unable to find image 'hello-world:latest' locally
    latest: Pulling from library/hello-world
    198f93fd5094: Pull complete
    Digest: sha256:a0dfb02aac212703bfcb339d77d47ec32c8706ff250850ecc0e19c8737b18567
    Status: Downloaded newer image for hello-world:latest

    Hello from Docker!
    This message shows that your installation appears to be working correctly.

    To generate this message, Docker took the following steps:
    1. The Docker client contacted the Docker daemon.
    2. The Docker daemon pulled the "hello-world" image from the Docker Hub.
        (arm64v8)
    3. The Docker daemon created a new container from that image which runs the
        executable that produces the output you are currently reading.
    4. The Docker daemon streamed that output to the Docker client, which sent it
        to your terminal.

    To try something more ambitious, you can run an Ubuntu container with:
    docker run -it ubuntu bash

    Share images, automate workflows, and more with a free Docker ID:
    https://hub.docker.com/

    For more examples and ideas, visit:
    https://docs.docker.com/get-started/
    ```

3. Try to run the following command again:

    ```bash
    docker run hello-world
    ```

    - Docker has now already downloaded the `hello-world` image, so it executes straight away.