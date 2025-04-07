# Github
## 1. SSH Key Generator
PuTTYgen is a key generator tool for creating pairs of public and private SSH keys.
### 1.1 Download PuTTYgen on Windows
To download 
To get PuTTY, go to PuTTY Installation Download page: https://www.puttygen.com/download-putty, whereby the complete installation package will be available with setup instructions.

![image](https://github.com/user-attachments/assets/413eb133-6c51-403e-9983-91a9bc415ad3)

### 1.2 Run PuTTYgen on Windows
To run PuTTYgen, Go to Windows -> Start Menu -> All Programs -> PuTTY -> PuTTYgen. You will see a window for the PuTTY Key Generator on your screen.

![image](https://github.com/user-attachments/assets/c763226d-7762-4f92-86ff-d90e1bb29978)

Voila! Now you can generate public or private key pair using PuTTYgen.

This is a text!

### 1.3 Types of Keys Supported on PuTTYgen
It is important to know the types of key PuTTYgen supports prior to using it. Below are the key types that it currently supports for SSH-2 and SSH-1 protocol:

SSH-1 protocol: For SSH-1 only supports one key i.e. Rivest–Shamir–Adleman (RSA)

SSH-2 protocol: SSH-2 supports multiple key types that include – Digital Signature Algorithm (DSA), Elliptic Curve Digital Signature Algorithm (ECDSA) and Ed25519.

### 1.4 Export OpenSSH key
Export the generated key to OpenSSH: Conversions => Export OpenSSH key

### 1.5 

# 2.Adding your SSH key to the ssh-agent
Before adding a new SSH key to the ssh-agent to manage your keys, you should have checked for existing SSH keys and generated a new SSH key. 

In a new admin elevated PowerShell window, ensure the ssh-agent is running.

# 2.1 Go to the SSH keys directory

cd "$env:USERPROFILE\.ssh"

# 2.2 Start the ssh-agent in the background
Get-Service -Name ssh-agent | Set-Service -StartupType Manual
Start-Service ssh-agent

# 2.3 Add your SSH key
ssh-add github_rsa
