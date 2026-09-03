FROM alpine:latest

RUN apk add --no-cache curl bash tar wget grep

# Get the bashcrawl source code
RUN wget https://gitlab.com/slackermedia/bashcrawl/-/archive/stable-2024.02.09/bashcrawl-stable-2024.02.09.tar.gz && tar xzf bashcrawl-stable-2024.02.09.tar.gz && mv bashcrawl-stable-2024.02.09 bashcrawl

# Set the working directory (where the commands will be executed)
WORKDIR /bashcrawl/entrance

ENTRYPOINT ["/bin/bash"]
