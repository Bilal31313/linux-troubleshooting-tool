# Linux Common Issues Troubleshooting Script

A lightweight, interactive Bash script for diagnosing and resolving common Linux system issues. Built as part of systems engineering interview prep, this tool helps automate real-world troubleshooting scenarios DevOps engineers often face.

## 🔧 Features

This script provides a menu with the following diagnostic options:

1. **Check High CPU Usage**
   - Displays the top CPU-consuming process
   - Option to `kill` or `renice` the offending process
   - Logs the action to `~/logs.txt`

2. **Check Open Ports**
   - Verifies if a specific port is open using `lsof`
   - Optionally checks if the port is bound only to `localhost`
   - Helps debug connectivity issues

3. **Check if a Service is Active**
   - Verifies the status of a given service using `systemctl`
   - Attempts to restart the service if inactive
   - If the restart fails, appends the last 10 log lines from `journalctl` to `~/logs.txt`

4. **Check Disk Usage**
   - Checks disk usage of a specific directory
   - If usage exceeds 60MB, offers to clean up files older than 7 days
   - Deletes files upon confirmation and logs them to `~/logs.txt`

5. **Exit**
   - Gracefully exits the tool

## 📦 Requirements

- Bash (Linux)
- `lsof`, `ss`, `systemctl`, `journalctl`, `du`, `find`, `awk`
- `sudo` permissions (for service control and file deletion)

## 🧪 Usage

```bash
bash Common_Issues
```
📝 Logging
All destructive actions and relevant details are logged to:

~/logs.txt
👨‍💻 Author
Bilal Khawaja
GitHub: Bilal31313

📄 License
MIT — use it, fork it, improve it.

