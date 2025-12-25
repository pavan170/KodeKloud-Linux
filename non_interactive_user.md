# Linux User Setup with Non-Interactive Shell

## Task

Create a user with a non-interactive shell (cannot log in) for services/tools.

- **User:** siva  
- **Shell:** /sbin/nologin  

## Commands

```bash
# Create the user with non-interactive shell
sudo useradd -s /sbin/nologin siva

# Ensure the shell is set correctly (optional if user already exists)
sudo usermod -s /sbin/nologin siva

# Verify user entry in /etc/passwd
getent passwd siva

# Check user ID and group info
id siva
groups siva
