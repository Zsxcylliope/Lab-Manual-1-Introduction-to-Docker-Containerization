# Lab Manual 1: Introduction to Docker Containerization

This repository contains the output for Lab Manual 1, covering the basics of Docker containerization, creating a Dockerfile, and building/running a Docker image.

## Installation Guide

To run this project on a Windows machine, you need to install Docker Desktop and configure Windows Subsystem for Linux (WSL).

### 1. Install WSL (Windows Subsystem for Linux)
1. Open PowerShell or Windows Command Prompt as **Administrator**.
2. Run the following command:
   ```powershell
   wsl --install
   ```
3. Restart your computer if prompted. This will install Ubuntu as the default Linux distribution.

### 2. Install Docker Desktop
1. Download **Docker Desktop for Windows** from the [official Docker website](https://www.docker.com/products/docker-desktop/).
2. Run the installer and follow the on-screen instructions.
3. During installation, make sure the option **"Use WSL 2 instead of Hyper-V"** is checked (this is usually the default).
4. Once installed, launch Docker Desktop. It may take a minute to start the Docker Engine.
5. Verify the installation by opening your terminal and running:
   ```powershell
   docker --version
   ```

## Guide Questions & Answers

**1. What role does the Dockerfile play in containerization?**
A Dockerfile is a text document that contains a set of instructions and commands used to build a Docker image. It acts as a blueprint or recipe that Docker follows to automatically create the image layer by layer. The Dockerfile specifies the base operating system, installs dependencies, copies application files, and defines the default command to run when the container starts.

**2. Why are Docker containers lighter than virtual machines?**
Docker containers are lighter than virtual machines because they share the host machine’s Operating System (OS) kernel and do not require a separate guest OS for each application. In contrast, Virtual Machines (VMs) use a hypervisor and run a full guest OS for every instance. Because of this shared architecture, containers start faster and consume less disk space, memory, and CPU resources compared to VMs.

**3. What happens when the container finishes execution?**
When the primary process inside the container finishes execution (for example, when python app.py completes running), the container automatically stops and enters an “exited” state. The container still exists on the system with its files and state preserved, and it can either be restarted or permanently removed using the docker rm command.
