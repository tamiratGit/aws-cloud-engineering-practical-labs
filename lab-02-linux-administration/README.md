# Lab 2: Linux Administration and Networking

## Objective
Practise Linux administration, user management, service management, process monitoring, and networking on an AWS EC2 Ubuntu server.

## 1. File and Directory Management

Created a practice directory and file:

```bash
mkdir ~/lab2
cd ~/lab2
echo "AWS Cloud Engineer Training" > notes.txt
ls -l notes.txt
```

## 2. Linux File Permissions

Practised changing permissions:

```bash
chmod 600 notes.txt
chmod 644 notes.txt
```

Changed file ownership:

```bash
sudo chown ubuntu:ubuntu notes.txt
```

Verified permissions using:

```bash
ls -l notes.txt
```

## 3. Linux User Management

Created a new Linux user:

```bash
sudo adduser clouduser
id clouduser
```

## 4. Apache Service Management

Practised checking, stopping, starting, and restarting Apache:

```bash
sudo systemctl status apache2
sudo systemctl stop apache2
sudo systemctl start apache2
sudo systemctl restart apache2
sudo systemctl is-active apache2
```

Confirmed that Apache was active after restarting.

## 5. Process Management

Inspected running processes:

```bash
ps aux
ps aux | grep apache2
top
```

## 6. Networking

Checked network interfaces and IP addresses:

```bash
ip addr
hostname -I
```

Checked routing:

```bash
ip route
```

Tested DNS resolution:

```bash
getent hosts amazon.com
```

Checked listening ports:

```bash
sudo ss -tulpn
```

Tested HTTP connectivity:

```bash
curl -I http://localhost
```

## Network Observation

- EC2 private IP observed: `172.31.47.227`
- DNS resolution: successful
- Apache port 80: listening
- HTTP test: successful
- Reported errors: none

## Skills Demonstrated
- Linux file permissions
- User and ownership management
- Apache service management
- Process monitoring
- IP address and routing inspection
- DNS troubleshooting
- Listening ports and HTTP testing

## Result
Successfully completed Linux administration and networking exercises on an AWS EC2 Ubuntu server.
