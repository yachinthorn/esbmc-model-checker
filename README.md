
# 🚀 Docker Image - ESBMC 7.8.1 on Ubuntu 24.04

📝 This is a **Docker image** with **ESBMC version 7.8.1** installed on **Ubuntu 24.04**.  
Using Docker helps you **avoid operating system and library installation issues**, ensuring a consistent development environment.

---

## 👍 Installation Guide

### 🔹 Requirements
- **Software**: Docker, Docker Desktop
- **IDE**: Visual Studio Code
- **Required Extensions**:
  - Remote - SSH
  - Dev Containers
  - Docker

### 🔹 Installation Steps
1. **Clone the repository**:
   ```bash
   git clone https://github.com/thinhle96/esbmc.git
   ```
2. **Start Docker Compose**:
   ```bash
   docker compose up -d
   ```
3. **Open VS Code and connect to the container**:
   - Select **Docker** from the left sidebar.
   - Right-click on the container -> **Attach Visual Studio Code**.
   - When VS Code opens, go to **File > Open Folder**, and select the **`/workspace`** folder.

   ![Docker VS Code](image.png)

---

## ▶️ Running ESBMC
1. **Navigate to the working directory**:
   ```bash
   cd /workspace/esbmc-demo
   ```
2. **Run ESBMC with `k-induction`**:
   ```bash
   esbmc sample.c --k-induction
   ```

---

## ⚠️ Notes
- **The `/workspace` directory already contains the code folder**: `esbmc-demo`.
- **It's recommended to write code inside the `/workspace` directory** to avoid data loss when the container is removed, as this directory is mounted with Docker Volumes.
