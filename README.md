# Reverse Proxy Setup for Simple Voice Chat Mod

This repository provides step-by-step instructions for setting up a reverse proxy to host the Simple Voice Chat mod on your Minecraft server. By following this guide, you'll configure a reverse proxy using Nginx.

## Features:
- **Nginx**: Example configuration files for nginx web server.
- **Firewall Configuration**: Recommended settings to enhance security.
## Prerequisites:
- A running Minecraft server with the Simple Voice Chat mod installed.
- A domain or subdomain pointing to your server (Optional).
- Access to a reverse proxy server (Nginx).

## Getting Started

Follow these steps to set up the reverse proxy for the Simple Voice Chat mod.

### 1. Install Nginx
If you haven't installed a web server like nginx, use the following guide to set up your web server:

#### Nginx Installation Guide for Popular Operating Systems

Below are the commands to install Nginx on different operating systems.

##### Debian/Ubuntu

```bash
sudo apt update
sudo apt install nginx -y
sudo systemctl enable nginx
sudo systemctl start nginx
```
### CentOS/RH
```bash
sudo yum install epel-release -y
sudo yum install nginx -y
sudo systemctl enable nginx
sudo systemctl start nginx
```
### Fedo
```bash
sudo dnf install nginx -y
sudo systemctl enable nginx
sudo systemctl start nginx
```
## Arch Lin
```bash
sudo pacman -S nginx
sudo systemctl enable nginx
sudo systemctl start nginx
```
