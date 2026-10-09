# Linux Fundamentals for Cybersecurity

## 1. Introduction

Linux is an open-source operating system widely used in servers, cloud infrastructure, cybersecurity labs, and security tools.

Understanding Linux helps cybersecurity professionals investigate systems, analyze logs, manage permissions, and understand how processes and networks operate.

## 2. Basic Linux Commands

| Command | Purpose | Example |
|---|---|---|
| `pwd` | Displays the current directory | `pwd` |
| `ls` | Lists files and directories | `ls -la` |
| `cd` | Changes the current directory | `cd Documents` |
| `mkdir` | Creates a directory | `mkdir lab-notes` |
| `touch` | Creates an empty file | `touch notes.txt` |
| `cat` | Displays file contents | `cat notes.txt` |
| `cp` | Copies files | `cp notes.txt backup.txt` |
| `mv` | Moves or renames files | `mv notes.txt linux.txt` |
| `whoami` | Displays the current username | `whoami` |
| `man` | Opens a command's manual | `man ls` |

## 3. Files and Directories

Linux organizes files in a hierarchical structure beginning at the root directory `/`.

Important directories include:

- `/home` — User home directories.
- `/etc` — System configuration files.
- `/var/log` — Common location for system and application logs.
- `/tmp` — Temporary files.
- `/root` — The root user's home directory.

## 4. File Permissions

Linux permissions control who can read, write, or execute a file.

- `r` — Read permission.
- `w` — Write permission.
- `x` — Execute permission.

Use `ls -l` to inspect file permissions.

Use `chmod` to change permissions. For example, `chmod 600 notes.txt` gives the owner read and write access while removing permissions for group and others.

**Security lesson:** Apply the principle of least privilege. Give users and processes only the permissions they need.

## 5. Processes and Users

Useful commands include:

- `ps` — Displays information about processes.
- `top` — Shows running processes and resource usage.
- `id` — Displays user and group identifiers.
- `sudo` — Runs an authorized command with elevated privileges.

**Security lesson:** Investigate unfamiliar processes carefully and use administrative privileges only when necessary.

## 6. Networking Basics

Useful commands include:

- `ip addr` — Displays network interface addresses.
- `ip route` — Displays routing information.
- `ss -tuln` — Lists listening TCP and UDP sockets.
- `ping` — Tests network reachability, where permitted.

**Security lesson:** Unexpected listening services can increase a system's attack surface. Verify whether each service is required and properly secured.

## 7. Log Analysis

Logs help administrators investigate errors, authentication activity, and unusual system behavior.

On many Linux systems, logs are stored under `/var/log`.

Example:

```bash
ls -la /var/log
```

Some systems use `journalctl` to inspect logs collected by systemd.

**Security lesson:** Review authentication failures, unexpected privilege changes, and unusual service activity. Interpret events
