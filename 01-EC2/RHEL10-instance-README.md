# 🚀 RHEL 10 Deployment on AWS EC2 | Sydney Region

## 📌 Project Overview

This project demonstrates the deployment and basic administration of a **Red Hat Enterprise Linux 10 (RHEL 10)** instance on **Amazon EC2** in the AWS Asia Pacific (Sydney) Region.

The objective was to gain practical experience in cloud server provisioning, storage configuration, network security, SSH-based remote access, and essential Linux system administration.

After completing the configuration and command-line exercises, the EC2 instance was terminated as part of resource cleanup.

## 🏗️ Infrastructure Configuration

| Component | Configuration |
|---|---|
| Cloud Provider | Amazon Web Services (AWS) |
| Cloud Service | Amazon EC2 |
| AWS Region | Asia Pacific (Sydney) |
| Region Code | ap-southeast-2 |
| Operating System | Red Hat Enterprise Linux 10 |
| Storage Capacity | 12 GiB |
| EBS Volume Type | General Purpose SSD (`gp3`) |
| Remote Connection | SSH |
| SSH Client | Git Bash |
| Instance Lifecycle | Launched → Connected → Tested → Terminated |

## 🔐 Security Group Configuration

Configured an EC2 Security Group to control inbound network traffic.

| Inbound Rule | Protocol | Port | Source | Description |
|---|---|---|---|---|
| SSH | TCP | 22 | My IP | Secure remote access |
| ICMP | ICMP | As configured | My IP | Network connectivity testing |

**Security Best Practices**
- Restricted SSH access to my current public IP address.
- Avoided exposing SSH (port 22) to all IP addresses (`0.0.0.0/0`).
- Used SSH key-pair authentication for remote connectivity.
- Configured ICMP access only for network diagnostics.

## 🔑 Connecting to EC2 Using SSH

After launching the instance and verifying its status checks, I connected to the RHEL server remotely using Git Bash.

**SSH command:**

```bash
ssh -i "your-key.pem" ec2-user@YOUR_PUBLIC_IP
```

Replace:
- `your-key.pem` with your downloaded private key filename.
- `YOUR_PUBLIC_IP` with the EC2 instance's public IPv4 address.

**Note:** The default SSH username for the standard AWS RHEL AMI is generally `ec2-user`.

## 🐧 Linux System Administration

After establishing the SSH connection, I executed the following commands to explore the server environment.

### 1. Privilege Management

```bash
sudo -i
whoami
```

- Switched to an interactive root login shell.
- Verified the current user identity.

### 2. Hostname Configuration

```bash
hostname
hostnamectl set-hostname node1
bash
hostname
```

- Checked the existing hostname.
- Changed the hostname to `node1`.
- Started a new Bash shell and verified the updated hostname.

### 3. Operating System Information

```bash
cat /etc/redhat-release
uname -r
```

- Verified the installed RHEL version.
- Checked the running Linux kernel version.

### 4. System Monitoring

```bash
uptime
df -h
```

- Checked system uptime and load averages.
- Inspected filesystem disk usage in human-readable format.

## 📸 Project Workflow

The practical implementation followed this sequence:

1. Selected the Red Hat Enterprise Linux 10 AMI.
2. Configured the EC2 instance in the Sydney region.
3. Configured 12 GiB GP3 storage.
4. Created a Security Group with SSH and ICMP inbound rules restricted to My IP.
5. Launched the EC2 instance.
6. Connected to the server using SSH through Git Bash.
7. Executed Linux system administration commands.
8. Verified operating system details, hostname, kernel version, uptime, and disk usage.
9. Terminated the EC2 instance after completing the demonstration.

## 🎯 Key Skills Demonstrated

- **AWS:** EC2 provisioning, Region selection, EBS storage configuration.
- **Cloud Networking:** Security Groups and inbound traffic management.
- **Linux:** Root access, hostname configuration, system information and disk monitoring.
- **Remote Administration:** SSH connectivity and key-pair authentication.
- **Cloud Resource Management:** EC2 instance lifecycle and cleanup.

## 🧹 Resource Cleanup

After completing the practical exercise, I terminated the EC2 instance to avoid leaving an unused compute resource running.

**Important:** Terminating an EC2 instance does not guarantee that all associated resources are deleted. Always check EBS volumes, snapshots, Elastic IP addresses, and other associated resources to avoid unexpected AWS charges.

## 💡 Key Takeaway

This hands-on exercise strengthened my understanding of deploying and managing a Linux server in the AWS cloud environment.

It provided practical exposure to **AWS EC2, RHEL 10, SSH connectivity, Security Groups, EBS storage, and Linux system administration**.

I look forward to building more hands-on projects and expanding my Cloud and DevOps knowledge.

---

### 🛠️ Technology Stack

`AWS` · `Amazon EC2` · `Red Hat Enterprise Linux 10` · `Linux` · `EBS GP3` · `Security Groups` · `SSH` · `Git Bash`

---

**#AWS #EC2 #RHEL10 #RedHat #LinuxAdministration #CloudComputing #DevOps #Linux**
connect with me: www.linkedin.com/in/dipali-dehankar-91511a3a7
