# Real Time Output of Commands I Practiced

## Hostname Commands

### 1. View Current Hostname

`hostnamectl` - Displays detailed hostname and system information.

![hostnamectl](images/1.png)

### 2. Change Hostname

`sudo hostnamectl set-hostname devops-server` - Changes the system hostname.

![hostname changed](images/2.png)

---

## Process Commands

### 3. Check System Uptime

`uptime` - Shows how long the system has been running and load averages.

![uptime](images/3.png)

### 4. Find High CPU Consuming Processes

`ps aux --sort=-%cpu | head` - Lists processes consuming the most CPU.

![cpu processes](images/4.png)

### 5. Display Process Tree

`pstree -p` - Shows parent-child relationship between running processes.

![pstree](images/5.png)

---

## Service Commands

### 6. List Running Services

`systemctl list-units --type=service --state=running`

Shows all currently running services.

![running services](images/6.png)

### 7. Check SSH Service Status

`systemctl status ssh`

Displays detailed information about the SSH service.

![ssh status](images/7.png)

### 8. View SSH Service Dependencies

`systemctl list-dependencies ssh`

Shows services and targets required by SSH.

![ssh dependencies](images/8.png)

---

## Log Commands

### 9. View SSH Logs

`journalctl -u ssh -n 20`

Displays the latest SSH service logs.

![ssh logs](images/9.png)

### 10. View Error Logs

`journalctl -p err -b`

Shows boot-time error messages.

![error logs](images/10.png)

---

## Storage Commands

### 11. Check Disk Usage

`df -h`

Displays filesystem usage in human-readable format.

![disk usage](images/11.png)

---

## What I Learned Today

- Learned how Linux manages processes and services.
- Explored process monitoring using `ps`, `uptime`, and `pstree`.
- Inspected SSH service status and dependencies.
- Viewed system and service logs using `journalctl`.
- Checked disk utilization using `df -h`.
- Changed the EC2 hostname using `hostnamectl`.
