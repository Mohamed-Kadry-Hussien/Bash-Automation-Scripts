# 🗂️ Backup and Recovery Tool

![Bash](https://img.shields.io/badge/Language-Bash-green)  ![Platform](https://img.shields.io/badge/Platform-Linux-lightgrey)

The **Backup and Recovery Tool** is a powerful Bash script designed to help you easily backup, restore, and manage your files. It supports local backups and synchronization with Google Drive using `rclone`. The tool is user-friendly and provides a menu-driven interface for seamless operation.

---

## 🚀 Features

| **Feature**            | **Description**                                                                 |
|-------------------------|---------------------------------------------------------------------------------|
| **📂 Backup Files**     | Create compressed backups of specified directories.                             |
| **🌐 Sync to Google Drive** | Automatically sync backups to Google Drive using `rclone`.                    |
| **📋 List Backups**     | View available backups in the specified backup destination.                    |
| **🔄 Restore Backups**  | Restore backups to a specified directory.                                      |
| **🔐 Secure**           | Uses a service account key for secure Google Drive access.                     |

---

## 🛠️ Files and Their Functions

### 1. **Main Script (`backup_tool.sh`)**:
   - **Function**: The core script that provides the backup, restore, and sync functionality.
   - **Usage**: Run the script and follow the menu prompts.
   - **Key Features**:
     - Backup files to a specified destination.
     - Sync backups to Google Drive.
     - List and restore backups.

### 2. **Service Account Key (`famous-vista-450706-b7-ede8cbe7aa55.json`)**:
   - **Function**: Provides secure access to Google Drive for syncing backups.
   - **Usage**: Place this file in the same directory as the script.
   - **Key Features**:
     - Authenticates with Google Drive using a service account.
     - Enables automated syncing of backups.

---

## 🛠️ Commands Used in the Script

### 1. **Backup Files**
- **`tar -czf`**: Creates a compressed archive of specified directories.
- **`mkdir -p`**: Ensures the backup destination directory exists.

### 2. **Sync to Google Drive**
- **`rclone copy`**: Uploads the backup file to Google Drive.
- **`rclone link`**: Generates a shareable link for the uploaded file.

### 3. **List Backups**
- **`ls -lh`**: Lists backup files with details (size, permissions, etc.).

### 4. **Restore Backups**
- **`tar -xzf`**: Extracts the backup archive to a specified directory.
- **`chown -R`**: Ensures the restored files have the correct ownership.

---

## 🌟 Advantages

- **✅ Easy to Use**: Menu-driven interface for seamless operation.
- **🔒 Secure**: Uses a service account key for secure Google Drive access.
- **📂 Flexible**: Supports local backups and cloud synchronization.
- **🔄 Automated**: Can be scheduled with `cron` for regular backups.
- **📄 Comprehensive**: Provides backup, restore, and sync functionality in one tool.

---
