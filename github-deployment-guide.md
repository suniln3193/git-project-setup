# Deploying Code from GitHub to Linux Server using SSH

## Prerequisites
- A Linux server with SSH access
- GitHub repository with your code
- Git installed on your Linux server
- SSH key pair generated on your local machine

## Step-by-Step Deployment Guide

### 1. Generate SSH Keys (if not already done)
```bash
# On your local machine
ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
```

### 2. Configure SSH Access to Server
```bash
# Copy your public key to the server
ssh-copy-id username@server_ip_address

# Test SSH connection
ssh username@server_ip_address
```

### 3. Configure GitHub SSH Access

1. Copy your SSH public key:
```bash
cat ~/.ssh/id_rsa.pub
```

2. Add this key to your GitHub account:
   - Go to GitHub → Settings → SSH and GPG keys
   - Click "New SSH key"
   - Paste your public key and save

### 4. Prepare the Linux Server

1. Create deployment directory:
```bash
mkdir -p /var/www/your_project
cd /var/www/your_project
```

2. Configure Git on the server:
```bash
git config --global user.name "Your Name"
git config --global user.email "your_email@example.com"
```

### 5. Initial Deployment

1. Clone your repository:
```bash
git clone git@github.com:username/repository.git .
```

2. Set proper permissions:
```bash
chmod -R 755 /var/www/your_project
chown -R www-data:www-data /var/www/your_project
```

### 6. Automated Deployment Setup

1. Create a deployment script (deploy.sh):
```bash
#!/bin/bash
cd /var/www/your_project
git pull origin main
# Add any additional deployment commands here:
# npm install
# composer install
# php artisan migrate
# etc.
```

2. Make the script executable:
```bash
chmod +x deploy.sh
```

### 7. Updating the Deployment

To update your deployment, either:

A. Manual update:
```bash
cd /var/www/your_project
git pull origin main
```

B. Run deployment script:
```bash
./deploy.sh
```

## Security Considerations

1. Always use SSH keys instead of passwords
2. Regularly update SSH keys and server access credentials
3. Use specific deployment users with limited permissions
4. Consider using deployment keys for GitHub repositories
5. Implement proper file permissions for your web server

## Troubleshooting

### Common Issues and Solutions:

1. Permission Denied:
```bash
sudo chown -R $USER:$USER /var/www/your_project
```

2. Git Pull Conflicts:
```bash
git reset --hard origin/main
git pull origin main
```

3. SSH Connection Issues:
```bash
ssh -vT git@github.com
```

## Maintenance

1. Regular backup implementation:
```bash
tar -czf backup.tar.gz /var/www/your_project
```

2. Log rotation setup:
```bash
sudo logrotate -f /etc/logrotate.conf
```

Remember to replace placeholder values such as `username`, `server_ip_address`, and `your_project` with your actual deployment details.
