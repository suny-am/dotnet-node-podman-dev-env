ARG VERSION=21-bookworm
FROM node:${VERSION}
USER node
WORKDIR /Workspace
COPY . .
RUN \
    curl -fsSL https://bun.sh/install | bash