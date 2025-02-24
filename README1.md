# 🖥️ System Health Checker Script

The **System Health Checker Script** is a powerful and user-friendly Bash script designed to monitor and report the health status of your Linux system. It provides detailed insights into CPU usage, memory consumption, disk space, network activity, pending software updates, and active users. Additionally, it can generate comprehensive reports and send them via email for remote monitoring.

---

## 🚀 Features

| Feature               | Description                                                                 |
|-----------------------|-----------------------------------------------------------------------------|
| **CPU Monitoring**    | Displays CPU model, cores, operation modes, and usage (overall and per-core).|
| **Memory Monitoring** | Shows total, used, free, and cached memory with usage percentage.           |
| **Disk Monitoring**   | Displays disk usage for all partitions and highlights root partition usage.  |
| **Network Monitoring**| Lists active interfaces, IP addresses, and provides live traffic monitoring. |
| **Software Updates**  | Checks for pending updates and lists upgradable packages.                   |
| **Active Users**      | Displays active users, sessions, and running processes.                     |
| **Report Generation** | Generates a comprehensive system health report in a text file.              |
| **Email Notifications**| Sends reports via email using `ssmtp` with Gmail support.                   |

---

## 🛠️ Commands Used in the Script

### 1. **CPU Monitoring**
- **`lscpu`**: Retrieves detailed CPU information (model, cores, operation modes).
- **`top -bn1`**: Displays CPU usage in batch mode (non-interactive).
- **`mpstat -P ALL`**: Shows CPU usage per core (requires `sysstat` package).

### 2. **Memory Monitoring**
- **`free -h`**: Displays memory usage in a human-readable format (total, used, free, cached).
- **`free | awk`**: Calculates memory usage percentage.

### 3. **Disk Monitoring**
- **`df -h`**: Shows disk usage for all partitions in a human-readable format.
- **`df -h /`**: Displays disk usage specifically for the root partition.

### 4. **Network Monitoring**
- **`ip -br a`**: Lists network interfaces and their IP addresses.
- **`vnstat -l`**: Monitors live network traffic (requires `vnstat` package).
- **`vnstat -d`**: Displays daily network usage.
- **`vnstat -m`**: Displays monthly network usage.

### 5. **Software Updates**
- **`apt list --upgradable`**: Lists upgradable packages (Debian/Ubuntu-based systems).

### 6. **Active Users**
- **`who`**: Displays currently logged-in users.
- **`who -u`**: Shows detailed user session information (start time, IP address).
- **`ps -eo user,comm`**: Lists running processes for each user.

### 7. **Report Generation**
- **`date +"%Y-%m-%d_%H-%M-%S"`**: Generates a timestamp for the report filename.
- **`mkdir -p`**: Creates the report directory if it doesn’t exist.
- **`>` and `>>`**: Redirects output to a file (overwrites or appends).

### 8. **Email Notifications**
- **`ssmtp`**: Sends emails using the `ssmtp` package.
- **`cat`**: Combines the report file with email headers for sending.

---

## 🌟 Advantages

- **Comprehensive Monitoring**: Covers all critical aspects of system health in one script.
- **User-Friendly**: Interactive prompts guide users through each feature.
- **Customizable**: Users can choose which metrics to monitor and generate reports.
- **Automation Ready**: Can be scheduled with `cron` for regular system health checks.
- **Email Alerts**: Enables remote monitoring by sending reports via email.
- **Lightweight**: Written in Bash, it has minimal dependencies and runs efficiently on any Linux system.

---
