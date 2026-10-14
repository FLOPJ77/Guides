# SSH Commands (Debian & Linux)


## 1. Installation on Debian

Debian usually includes the SSH client by default, but to accept incoming connections you must install the SSH server.

### Install the Server (The machine you want to access):

```bash
sudo apt update
sudo apt install openssh-server -y

```

### If you need to reinstall the client
```bash
sudo apt install openssh-client -y
```

### Manage SSH Service:

```bash
# Check if SSH is running
sudo systemctl status ssh

# Start and enable on boot
sudo systemctl start ssh
sudo systemctl enable ssh

# Restart SSH (e.g., after editing configs)
sudo systemctl restart ssh

```

### Commands:

```bash
# Standard connection (default port 22)
ssh username@remote_ip_or_hostname

# Connect using a custom port
ssh -p 2222 username@remote_ip_or_hostname

# Execute a single command remotely and exit
ssh username@remote_ip "uptime"

# Verbose mode (great for troubleshooting connection issues)
ssh -v username@remote_ip

```

## SSH Key Authentication (Passwordless & Secure)

Using keys is safer and faster than using passwords.
Step 1: Generate a key pair on your local machine

```bash
# Ed25519 is modern, fast, and secure (recommended)
ssh-keygen -t ed25519 -C "your_email_or_comment"

# Or standard RSA (4096-bit):
ssh-keygen -t rsa -b 4096
```

(Press Enter to accept default paths, set an optional passphrase).
Step 2: Copy your public key to the remote server

```bash
# Standard copy
ssh-copy-id username@remote_ip

# Copy if the server uses a non-standard port
ssh-copy-id -p 2222 username@remote_ip
```

Step 3: Connect using the key

```bash
# Connect normally (will automatically look for ~/.ssh/id_ed25519)
ssh username@remote_ip

# Or specify an identity file explicitly
ssh -i ~/.ssh/my_custom_key username@remote_ip
```


5. Script: SSH Config File (~/.ssh/config)

Instead of typing long commands, create a config file on your local machine:

```bash
vi ~/.ssh/config
```

Add your shortcuts like this:
code Text

```bash
Host myserver
    HostName 192.168.1.50
    User debian
    Port 22
    IdentityFile ~/.ssh/id_ed25519

```

Now you can simply connect by typing:

```bash
ssh myserver

```

### Important Files & Paths

Path	Purpose
/etc/ssh/sshd_config	Main SSH daemon configuration file (on the server).
~/.ssh/	User directory storing private/public keys and config.
~/.ssh/authorized_keys	Remote file containing trusted public keys allowed to log in.
~/.ssh/known_hosts	Local cache of verified fingerprints of remote servers.
