# Linux Custom Apache User Setup

## 🔐 Why this task was given

xFusionCorp wants better security for their web applications.  
Instead of running Apache apps as a common user, each application gets its own Linux user.  
This limits damage if one app is compromised.

## 📝 Task Requirements

- **Server:** App Server 2 (stapp02)  
- **User:** yousuf  
- **UID:** 1067  
- **Home directory:** /var/www/yousuf  

## ⚙️ Commands Used

```bash
# Logged in as steve, switched to root
sudo su -

# Create user
useradd -u 1067 -d /var/www/yousuf -m yousuf

# Verify
id yousuf




##✅ Final Result

User yousuf exists ✔

UID is 1067 ✔

Home directory is /var/www/yousuf ✔

Task completed 100% ✔