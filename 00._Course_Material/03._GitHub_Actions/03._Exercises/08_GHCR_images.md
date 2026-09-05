# GitHub Container Registry (GHCR) Images

## Goal

The goal of this exercise is to pull the Docker image you pushed to the GitHub Container Registry (GHCR) in the previous exercise and run it locally.

## Step 1: Pull the Docker Image

To pull the Docker image from GHCR, you could use the following command: 
```bash
docker pull ghcr.io/YOUR_GITHUB_USERNAME/YOUR_REPOSITORY_NAME:latest
```

Replace `YOUR_GITHUB_USERNAME` and `YOUR_REPOSITORY_NAME` with your actual GitHub username and repository name.

Then run it with Docker commands.

## Step 2: Create a new compose.ghcr.yaml file

You could also use Docker Compose to run the image. To do this, create a new `compose.ghcr.yaml` file in the root of this weeks repository.

Open the `compose.ghcr.yaml` file and add the following content:

```yaml
services:
  app:
    image: ghcr.io/YOUR_GITHUB_USERNAME/YOUR_REPOSITORY_NAME:latest
    ports:
      - "8090:8080"
```

Make sure to replace `YOUR_GITHUB_USERNAME` and `YOUR_REPOSITORY_NAME` with your actual GitHub username and repository name.

## Step 3: Run the Docker Container

To run the Docker container in detached mode using the `compose.ghcr.yaml` file, use the following command:

```bash
docker compose -f compose.ghcr.yaml up -d
```

MacOS users on Apple Silicon will see the following warning: `The requested image's platform (linux/amd64) does not match the detected host platform (linux/arm64/v8) and no specific platform was requested`. But this is just a warning and it will still work.

## Step 4: Verify the Application

To verify that the application is running correctly, you can use the following command to check the health endpoint:
```bash
curl http://localhost:8090/actuator/health
```
You should see a response indicating that the application is healthy.

## Step 5: Stop the Docker Container

To stop and remove the Docker container, use the following command:
```bash
docker compose -f compose.ghcr.yaml down
```

## Step 6: Clean Up

If you want to remove the pulled Docker image from your local machine, you can use the following command:
```bash
docker rmi ghcr.io/YOUR_GITHUB_USERNAME/YOUR_REPOSITORY_NAME:latest
```
Make sure to replace `YOUR_GITHUB_USERNAME` and `YOUR_REPOSITORY_NAME` with your actual GitHub username and repository name.


## Troubleshooting

### Unauthorized Error on Pulling Image
If you encounter an unauthorized error when trying to pull the image from GHCR, you need to authenticate with GHCR.

First, you need to create a Personal Access Token (PAT) with the appropriate scopes. You can do this by going to your GitHub account settings, navigating to "Developer settings" > "Tokens (classic)" ([Link to token page](https://github.com/settings/tokens)), and generating a new token with the `read:packages` scope.

Once you have the token, you can authenticate with GHCR using the following command:

```bash
echo YOUR_PERSONAL_ACCESS_TOKEN | docker login ghcr.io -u YOUR_GITHUB_USERNAME --password-stdin
```
> Replace `YOUR_PERSONAL_ACCESS_TOKEN` with the token you generated, and `YOUR_GITHUB_USERNAME` with your actual GitHub username.

After authenticating, you should be able to pull the image without any issues.

If you still encounter issues, try authenticating again or check if the token has the correct scopes. You could also try to set the package visibility to public in the repository settings, which would allow anyone to pull the image without authentication.
