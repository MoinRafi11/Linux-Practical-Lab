# Linux System-Level Commands

This section covers basic Linux commands used to inspect CPU, memory, disk storage, and network information.

---

## 1. CPU Information

### `lscpu`

Displays detailed information about the system CPU.

```bash
lscpu

Useful information

The output can include:

1.CPU architecture
2.Number of CPUs
3.CPU cores
4.Threads
5.CPU model
6.CPU frequency
7.Virtualization information.


## 2. Memory Information
free

Displays information about system memory and swap usage.

free

For human-readable output:

free -h
Useful information

The output shows:

Total memory
Used memory
Free memory
Available memory
Swap memory


## 3. Disk Space
df

Displays available and used disk space on mounted file systems.

df

For human-readable output:

df -h
Useful information

The output includes:

File system
Total size
Used space
Available space
Usage percentage
Mount point


## 4. Directory Disk Usage
du

Displays the amount of disk space used by files and directories.

du

#To display the total size of a directory in a human-readable format:

du -sh directory/
Useful options
du -h
du -sh



##5. `Block Devices`
lsblk

Lists available block devices such as disks and partitions.

lsblk


Purpose:

Useful for identifying:

Hard disks
SSDs
Virtual disks
Partitions
Mount points


## 6. `Hostname`

hostname

#Displays the system's hostname.

hostname

#To display additional hostname information:

hostnamectl


## 7. IP Address Information
ip

The ip command is used to view and manage network interfaces and addresses.

To display network interfaces and IP addresses:

ip addr

A shorter form is:

ip a


## 8. Test Network Connectivity
ping

Tests network connectivity to another host.

ping google.com

To send a specific number of packets:

ping -c 4 google.com

Press Ctrl + C to stop a continuous ping.


## 9. Network Connections
ss

Displays network sockets and active connections.

ss

To display listening TCP and UDP ports:

ss -tuln
Useful options
-t  → TCP
-u  → UDP
-l  → Listening
-n  → Display numerical addresses and ports


🧪 Basic System Inspection Workflow

A simple system inspection can be performed using:

lscpu
free -h
df -h
lsblk
ip addr
hostname

These commands provide a quick overview of the system's CPU, memory, storage, and network configuration.

