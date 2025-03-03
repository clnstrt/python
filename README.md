# CleanStart Python

[![Docker Hub](https://img.shields.io/docker/pulls/cleanstart/python.svg)](https://hub.docker.com/r/cleanstart/python)
[![Docker Image Size](https://img.shields.io/docker/image-size/cleanstart/python/latest)](https://hub.docker.com/r/cleanstart/python)

A **secure, lightweight, and production-ready** Python runtime environment that prioritizes security and performance.

## Features

- **Fast startup times** for improved deployment efficiency
- **Reduced attack surface** with minimal dependencies
- **Easy deployment** across any environment supporting Docker
- **Multiple variants** for both production and development needs

## Why Use CleanStart Python?

- **🔒 Minimal & Secure**: Stripped-down image with no unnecessary dependencies, reducing potential vulnerabilities
- **🚀 Optimized Performance**: Designed for fast execution and lower resource consumption
- **🛠️ Multiple Variants**: Supports standard and development versions for flexibility
- **📦 Fully Containerized**: Run Python anywhere with ease using Docker

## Available Variants

CleanStart provides two image variants:

### Production Variant
Minimal runtime variant optimized for production security:
```sh
docker pull ghcr.io/clnstrt/python:3.11
```

### Development Variant
Includes additional tools helpful during development:
```sh
docker pull ghcr.io/clnstrt/python:3.11-dev
```

## Usage Examples

### Running an Interactive Python Shell
```sh
docker run -it --rm ghcr.io/clnstrt/python:3.11
```

### Executing a Python Script
```sh
docker run --rm -v $(pwd):/app -w /app ghcr.io/clnstrt/python:3.11 python script.py
```

### Accessing a Shell in the Development Variant
```sh
docker run -it --entrypoint /bin/bash ghcr.io/clnstrt/python:3.11
```

### Installing Packages in Development Variant
```sh
docker run -it --user root --entrypoint /bin/bash ghcr.io/clnstrt/python:3.11
```

> ⚠️ **Note:** Running containers as root is not recommended in production environments.

## Docker Hub Repository

This image is available on Docker Hub: [cleanstart/python]([https://hub.docker.com/r/cleanstart/python](https://hub.docker.com/repository/docker/cleanstart/python)

## License

[MIT License](LICENSE)
