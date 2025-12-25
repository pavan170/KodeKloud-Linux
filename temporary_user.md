# Temporary User Setup on App Server 3

## Task Goal

Create a **temporary user** that expires on a specific date.

- **User:** `siva`  
- **Expiry:** `2024-04-15`  
- **Server:** App Server 3  
- **Username must be lowercase**

**Purpose:**

- Grant developers or service accounts **limited-time access**.  
- Automates removal after expiry for security and compliance.

---

## 🔹 Key Concept

- Temporary users are **automatically disabled** after the expiry date.  
- Useful for:  
  - Developers on short assignments  
  - Backup or service accounts  
  - Temporary project access  

---

## 🔹 Important Files

- `/etc/passwd` → user info  
- `/etc/shadow` → password & expiry info  
- `/etc/group` → group membership  

---

## 🔹 Command to Create Temporary User

```bash
sudo useradd -e 2024-04-15 siva

