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

# How to Access and Edit Nginx Configuration

This guide will help you locate, access, and edit the Nginx configuration file (`nginx.conf`) on your server. Modifying the Nginx configuration is crucial for setting up reverse proxies.

## 1. Locating the Nginx Configuration File

The main Nginx configuration file, `nginx.conf`, is usually located in one of the following directories depending on your operating system:

### Common Locations:
- **Debian/Ubuntu**: `/etc/nginx/nginx.conf`
- **CentOS/RHEL**: `/etc/nginx/nginx.conf`
- **Fedora**: `/etc/nginx/nginx.conf`
- **Arch Linux**: `/etc/nginx/nginx.conf`
## 2. Accessing the Nginx Configuration File

To access the Nginx configuration file, follow these steps:

### 2.1 Use SSH to Connect to Your Server (If Remote)
If you're working on a remote server, you'll need to connect via SSH. Run this command in your terminal (replace `user` and `server_ip` with your server's details):

```bash
ssh user@server_ip
```
### 2.2 Open the Configuration File
Once connected, you can open the Nginx configuration file using a text editor such as nano or vim. Use the following command:

```bash
sudo nano (location)
or 
sudo vim (location)
```
Once opened, go to the bottom of your nginx.conf and paste this code.
```nginx
    server {
        listen 24454 udp; #Replace the port with your actual minecraft server port.
        proxy_pass YOUR_SERVER_IP:24454; #You can replace the port with any open port you want.
    }
```
# 3. Opening ports in firewall
Now you need to open the ports of both the server and your reverse proxy server.

And that is it, you have successfully installed a reverse proxy for simple voice chat mod.
