# Group-Based Access Setup (Nautilus App Servers)

## Objective
Implement group-based access control on Nautilus App servers.

## Target Servers
- stapp01  
- stapp02  
- stapp03  

## Group and User Details
- **Group:** `nautilus_admin_users`  
- **User:** `mohammed`  

## Commands

```bash
# Create the group
sudo groupadd nautilus_admin_users

# Check if user exists, if not, create user
id mohammed || sudo useradd mohammed

# Add user to the group
sudo usermod -aG nautilus_admin_users mohammed

# Verify user groups
groups mohammed
