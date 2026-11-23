# Lab 1: Deploying an AWS EC2 Linux Web Server

## Objective
Deploy an Ubuntu Linux server on AWS EC2, install Apache, and publish a webpage accessible through the internet.

## Environment
- Cloud provider: Amazon Web Services (AWS)
- Region: Stockholm (`eu-north-1`)
- Operating system: Ubuntu Server 24.04 LTS
- Web server: Apache2
- Local computer: macOS

## 1. Launching an EC2 Instance
- Launched an Ubuntu EC2 instance.
- Configured an AWS Security Group.
- Allowed SSH traffic on port 22 from my IP address.
- Allowed HTTP traffic on port 80.

## 2. Connecting Through SSH

Connected to the EC2 instance from my Mac:

```bash
ssh -i cloud-lab-key.pem ubuntu@YOUR_PUBLIC_IP
```

Verified the connected Linux user:

```bash
whoami
```

Result: `ubuntu`

## 3. Installing Apache

```bash
sudo apt update
sudo apt upgrade -y
sudo apt install apache2 -y
sudo systemctl start apache2
sudo systemctl enable apache2
sudo systemctl status apache2
```

Confirmed that Apache was running.

## 4. Publishing a Webpage

Created a custom webpage:

```bash
echo '<h1>My First AWS Cloud Server</h1><p>Hosted on Ubuntu EC2 in Stockholm.</p><p>My cloud engineering journey starts here!</p>' | sudo tee /var/www/html/index.html
```

Tested the webpage:

```bash
curl http://localhost
```

Opened the EC2 public IP address in a browser and confirmed that the webpage worked.

## Skills Demonstrated
- AWS EC2 provisioning
- Ubuntu Linux administration
- SSH access
- Security Group configuration
- Apache installation and management
- Basic web server deployment
- HTTP connectivity testing

## Result
Successfully deployed an Apache web server on AWS EC2 and accessed my custom webpage through the internet.
<img width="776" height="454" alt="Screenshot 2026-11-23 at 11 35 41" src="https://github.com/user-attachments/assets/2512e350-da1f-4b7f-a081-2b70d0ac0939" />

