## Redis Server Installation in Windows 10 (v1709 – 2017-09, Fall Creators Update) on top of Windows Subsystem for Linux (WSL)


### Software requirements to install Redis Server in Windows
	1. Windows 10 (v1709 – 2017-09, Fall Creators Update)
	2. Microsoft PowerShell as the default shell
	3. Any one of the followings
		a) Ubuntu 18.04 (installs Redis v4.09)
		b) Kali Linux (installs Redis v4.10)
		c) Debian GNU/Linux (installs Redis v3.2.6)

### Software requirements to install Redis Client in Windows
	1. Redis Desktop Manager
	2. Any other client such as Java, C#, and etc...


## Step by Step: Install & Setup Redis Server

### Step 1: Open Windows PowerShell and execute following command
	> Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux

### Step 2: Restart windows

### Step 3: Download Ubuntu 18.04 LTS (installs Redis v4.09) from 'Microsoft Store'

### Goto Ubuntu terminal

### Step 4: Update Ubunu
	> sudo apt-get update

### Step 5: Upgrade Ubuntu
	> sudo apt-get upgrade

	Note: Give yes for all the questions

### Step 6: Install Redis Server
	> sudo apt-get install redis-server

### Step 7: Check Redis Server version
	$ redis-cli -v

### Step 8: Restart the Redis server to make sure it is running:
	$ sudo service redis-server restart

### Step 9: Execute a simple Redis command to verify your Redis server is running and available:
	$ redis-cli

### Step 10: Set a Key & Value pairs
	127.0.0.1:6379> set my_name "Rahamath S"

### Step 11: Get a Value by Key
	127.0.0.1:6379> get my_name
	"my_name"

### Step 11: To stop Redis server:
	127.0.0.1:6379> sudo service redis-server stop


## Step by Step: Install & Setup Redis Desktop Manager

### Step 1: Download following Redis Desktop Manager from http://docs.redisdesktop.com/en/latest/install/
	- redis-desktop-manager-2019.5.176.exe

### Step 2: After installation, open Redis Desktop Manager

### Step 3: Click on 'Connect to Redis Server'

### Step 4: Enter following Redis Server connection settings
	- Connection Name
	- Redis Server IP (default: 127.0.0.1)
	- Redis Server Port (default: 6379)
	- Enter SSL, SSL Tunnel and other nessesary details

### Step 5: Test Connection and Click 'OK'

### Step 6: Left side click on the 'Connection Name' to expand and check the Keys & Values


## Refer following GitHub project for Java Client to connect with Redis Server

	https://github.com/rahamath18/Redis-Jedis-Java-Client-Example

## Note:

The MSOpenTech-Redis project is no longer being actively maintained. If you are looking for a Windows version of Redis, you may want to check out Memurai. Please note that Microsoft is not officially endorsing this product in any way. More details in https://github.com/microsoftarchive/redis

To install & setup Redis Server on Windows 10 https://redislabs.com/blog/redis-on-windows-10

To install & setup Redis Server on macOS & Linux https://redis.io/download

Also, you may install & setup Redis Server on Linux via the package manager

For quick Redis Server Installation & Setup Guide for macOS https://github.com/rahamath18/Redis-on-MacOS