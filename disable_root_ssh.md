# Disable Direct Root SSH Login on App Servers


## 🔹 Goal


- Prevent direct SSH login as `root` on all app servers.  
- Users must log in as normal users and use `sudo` for administrative tasks.  
- Security best practice to avoid brute-force attacks on root.


---


## 🔹 Steps with Explanation


### 1️⃣ Backup SSH config


```bash
#copying the existing sshd_config to a backup file 
sudo cp /etc/ssh/sshd_config /etc/ssh/sshd_config.bak



Explanation:
Before making any changes, create a backup of the SSH configuration.
If something goes wrong, you can restore the original file.


###2️⃣ Edit SSH configuration


```bash


#open the code
sudo vi /etc/ssh/sshd_config


Explanation:
The SSH configuration file controls who can log in and how.


Locate the line:
#PermitRootLogin yes
Change it to:
PermitRootLogin no


Remove the '#' if it's commented out.


Why:
This prevents anyone from logging in directly as root, enforcing the use of normal users + sudo for administrative tasks.


###3️⃣ Restart SSH service
```bash
#resrtarting the ssh service to apply changes


sudo systemctl restart sshd
Explanation:
Changes to sshd_config do not take effect until the SSH service is restarted.
Restarting ensures the new configuration is applied immediately.