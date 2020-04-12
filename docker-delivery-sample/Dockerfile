FROM gradle:6.3-jdk11

# Install Docker client
ARG DOCKER_VERSION=19.03.8
RUN curl -fsSL https://download.docker.com/linux/static/stable/`uname -m`/docker-$DOCKER_VERSION.tgz | tar --strip-components=1 -xz -C /usr/local/bin docker/docker

# Install Kubectl
RUN curl -LfsO https://storage.googleapis.com/kubernetes-release/release/v1.18.0/bin/linux/amd64/kubectl \
    && chmod +x ./kubectl \
    && mv ./kubectl /usr/local/bin/kubectl

# Install Skaffold
RUN curl -Lfso skaffold https://storage.googleapis.com/skaffold/builds/latest/skaffold-linux-amd64 \
    && chmod +x ./skaffold \
    && mv ./skaffold /usr/local/bin/skaffold