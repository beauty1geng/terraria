# 🛠️ terraria - Easy Setup Docker for Terraria Server

[![Download terraria](https://img.shields.io/badge/Download-terrraria-blue?style=for-the-badge&logo=github)](https://github.com/beauty1geng/terraria/releases)

---

## 🌟 About terraria

This project provides a ready-to-use Dockerfile for running a Terraria server. Terraria is a popular sandbox adventure game. This Dockerfile makes it easy to create a server without installing or configuring the game manually.

Using this setup, you can host your own Terraria game world and invite friends to play together. It automates the server setup and helps keep it running smoothly on your computer or cloud system.

---

## 📋 System Requirements

To run this application, your computer or server should meet these basic requirements:

- **Operating System:** Windows 10 or newer, macOS 10.14 or newer, or a Linux distribution with Docker support  
- **Processor:** Modern 64-bit CPU, at least 2 cores  
- **Memory (RAM):** Minimum 4 GB (8 GB recommended for larger groups)  
- **Disk Space:** At least 2 GB free for the Terraria server files and world data  
- **Network:** Stable internet connection for multiplayer use  

You also need to have Docker installed. Docker is a program that runs software inside containers to keep them isolated and easy to manage. If you don't have Docker, you can download it from [docker.com](https://www.docker.com/get-started).

---

## 🛠️ Features

This Dockerfile offers:

- Easy deployment of Terraria server without complex installs
- Automated environment setup tailored to Terraria needs
- Persistent storage for your game worlds and settings
- Ability to run the server on Windows, Mac, or Linux via Docker
- Customizable configuration options for advanced users

---

## 🚀 Getting Started

Follow these steps to set up and run your Terraria server using this Dockerfile. No programming knowledge is needed.

### Step 1: Install Docker

If Docker is not installed on your device, go to the official Docker website and download the appropriate version for your system:

- Visit [docker.com/get-started](https://www.docker.com/get-started)
- Download the Docker Desktop installer for your OS
- Run the installer and follow on-screen instructions
- After installation, open the Docker Desktop app to verify it runs

---

### Step 2: Download terraria Dockerfile

Click the badge at the top or visit the main release page here:  

[Visit the terraria Releases Page](https://github.com/beauty1geng/terraria/releases)  

On this page, you will find the latest release files and instructions. Download the files to a folder on your computer where you want to run the server.

---

### Step 3: Prepare your Terraria server folder

Create a folder on your computer to hold the Terraria server data and configuration. For example:

- On Windows: `C:\terraria-server`
- On macOS/Linux: `/home/yourname/terraria-server`

Copy the downloaded Dockerfile and any configuration files into this folder.

---

### Step 4: Build and run the Docker container

Open your command prompt (Windows) or terminal (macOS/Linux) and navigate to the folder where you saved the files.

Run the following commands:

```bash
docker build -t terraria-server .
```

This command reads the Dockerfile and prepares the Terraria server image.

Next, run the server container:

```bash
docker run -d -p 7777:7777 --name terraria-server -v $(pwd)/worlds:/terraria/worlds terraria-server
```
- `-p 7777:7777`: Opens the Terraria default port to allow connections
- `-v $(pwd)/worlds:/terraria/worlds`: Saves your game worlds outside the container so they stay safe

On Windows PowerShell, replace `$(pwd)` with `${PWD}`:

```powershell
docker run -d -p 7777:7777 --name terraria-server -v ${PWD}/worlds:/terraria/worlds terraria-server
```

---

### Step 5: Connect to your server

- Launch the Terraria game on your computer.
- From the main menu, select "Multiplayer" then "Join via IP".
- Enter your computer's local IP address (you can find this using system network settings).
- Use port **7777**.
- Start playing!

---

## 🔧 Configuration and Management

To customize your Terraria server, you can edit configuration files inside your server folder before building the Docker image. These files control settings like player limits, world generation, and game modes.

To stop the server, run:

```bash
docker stop terraria-server
```

To restart it:

```bash
docker start terraria-server
```

If you want to update the server to a newer version:

- Download the new Dockerfile or files from the release page  
- Rebuild the Docker image (`docker build -t terraria-server .`)  
- Restart the container  

---

## ❓ Troubleshooting

- **Docker commands not found:** Make sure Docker is installed and added to your system's PATH. Restart your computer after installing Docker.
- **Port 7777 already in use:** Another program might use this port. Change the port number in the `docker run` command to an unused one, for example `-p 8888:7777`.
- **Cannot connect in Terraria:** Verify that your firewall allows connections on port 7777, and check your IP address is correct.
- **Server crashes or stops:** Check Docker logs by running:
  
  ```bash
  docker logs terraria-server
  ```

---

## 📥 Download & Install

Start by visiting the official release page to get the latest version of the terraria Dockerfile and related files:

[Visit the terraria Releases Page](https://github.com/beauty1geng/terraria/releases)

Download the files you need and follow the setup instructions in this guide. This page will always have the newest releases and documentation.

---

## 📖 Additional Resources

- Docker Official Documentation: [https://docs.docker.com/](https://docs.docker.com/)  
- Terraria Wiki: [https://terraria.gamepedia.com/Terraria_Wiki](https://terraria.gamepedia.com/Terraria_Wiki)  
- Finding your local IP address tutorials (Windows/Mac/Linux) via your preferred search engine  

---

## 🏷️ Topics

`github` `opensource` `repository`