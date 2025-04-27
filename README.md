# 🐦 Pterohost - Docker Images for Pterodactyl  
## Java GraalVM (AMD64 / ARM64)

A collection of multi-architecture Docker images pre-configured for **[Pterodactyl Panel](https://pterodactyl.io)** that ship the blazing-fast **GraalVM** runtime.  
All images are published to **GitHub Container Registry** and include both `amd64` and `arm64` layers.

### 📦 Supported tags

| Runtime | Image tag | Pull command |
|---------|-----------|--------------|
| **Java 8 (GraalVM CE)**  | `ghcr.io/pterohost/pterodactyl-images:java_8_graalvm`  | `docker pull ghcr.io/pterohost/pterodactyl-images:java_8_graalvm` |
| **Java 11 (GraalVM JDK)** | `ghcr.io/pterohost/pterodactyl-images:java_11_graalvm` | `docker pull ghcr.io/pterohost/pterodactyl-images:java_11_graalvm` |
| **Java 17 (GraalVM JDK)** | `ghcr.io/pterohost/pterodactyl-images:java_17_graalvm` | `docker pull ghcr.io/pterohost/pterodactyl-images:java_17_graalvm` |
| **Java 21 (GraalVM JDK)** | `ghcr.io/pterohost/pterodactyl-images:java_21_graalvm` | `docker pull ghcr.io/pterohost/pterodactyl-images:java_21_graalvm` |
| **Java 22 (GraalVM JDK)** | `ghcr.io/pterohost/pterodactyl-images:java_22_graalvm` | `docker pull ghcr.io/pterohost/pterodactyl-images:java_22_graalvm` |
| **Java 24 (GraalVM JDK)** | `ghcr.io/pterohost/pterodactyl-images:java_24_graalvm` | `docker pull ghcr.io/pterohost/pterodactyl-images:java_24_graalvm` |

> **Tip:** All tags include both `linux/amd64` and `linux/arm64` layers, so Docker will automatically fetch the right architecture for you.

### 🚀 Quick start

```bash
# Example: run a Java 24 GraalVM server
docker run -it --rm \
  -p 25565:25565 \
  --name graal-java24 \
  ghcr.io/pterohost/pterodactyl-images:java_24_graalvm
```

When deploying on **Pterodactyl Panel**, simply paste the desired image tag into the "Docker Image" field of your egg or server configuration.  
Everything else (user, working directory, common environment variables) is set up to match Pterodactyl best practices out of the box.

### 🔧 What’s inside?

* **GraalVM Community Edition** with `native-image` toolchain where available  
* Minimal Alpine/Ubuntu base layers to keep images lightweight  
* `curl`, `tzdata`, `bash`, and common CA certificates pre-installed  
* Non-root `container` user mapped to UID 1000 for Pterodactyl compatibility  
* Default working directory `/home/container`

### 📝 License & attribution
Copyright © 2022-2025 trenutoo/pterodactyl-images

Portions of the Dockerfiles and documentation in this repository were adapted from  
<https://github.com/trenutoo/pterodactyl-images> and are redistributed under
the terms of the original MIT License.

### 🙏 Special thanks

Huge appreciation to everyone who has contributed to the original open-source effort — check out the contributor graph here: <https://github.com/trenutoo/pterodactyl-images/graphs/contributors>
Their work laid the foundation for these images. ❤️ 
