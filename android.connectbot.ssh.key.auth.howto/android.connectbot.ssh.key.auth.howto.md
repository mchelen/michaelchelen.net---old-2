[[connectbot.htc.aria.300px.png|frame|alt=ConnectBot running on HTC Aria from ATT]]


SSH provides secure access to a remote server. Both password and public key authentication are allowed. ConnectBot is an open source SSH client for Android. A key can be created in ConnectBot for use with the server. The key can be disabled at any time. This method can be performed entirely from your Android handset if you currently have password access to an SSH server. ConnectBot supports shell login and port forwarding, and file transfer is planned. Tested with ConnectBot 1.7.0, Android 2.2, and Ubuntu 10.10 Beta.


# Install Open SSH server
SSH server must be installed on the remote system. Key authentication is usually enabled by default. To install in Ubuntu:
```
sudo apt-get install openssh-server
```

# Start ConnectBot
[[connectbot.home.png|frame|alt=ConnectBot home screen]]
There are no known hosts yet.

# Select Manage Pubkeys
[[connectbot.home.menu.png|frame|alt=Home screen Menu]]
Click Menu, then Manage Pubkeys to configure keys.

# Manage Pubkeys Screen
[[connectbot.pubkeys.png|frame|alt=Manage the authentication keys]]
There are no keys set up yet.

# Generate Pubkey
[[connectbot.pubkey.generate.png|frame|alt=Add a new key]]

Click Menu then Generate. We are going to create a new key. This allows us to specifically revoke access if the handset is lost.

# Generate Pubkey Settings
[[connectbot.pubkey.generate.settings.png|frame|alt=Settings for new pubkey]]

Most of the defaults are fine. We will create a 1024 bit RSA key. For added security, use a password for the key. This will let you to securely use the same password on all servers where your key is authorized.

# Example Settings
[[connectbot.pubkey.generate.settings.example.png|frame|alt=Settings for new pubkey]]
You can call your key anything you like. I have named mine after the device, htc_aria. Enable "Load key at start" to have the key automatically loaded.

# Collect Entropy 
[[connectbot.pubkey.generate.entropy.png|frame|alt=Entropy collection]]
Random numbers are used to generate the key. Move your finger around the screen until enough is generated.

# New Pubkey Created
[[connectbot.pubkey.example.png|frame|alt=New pubkey listed]]
The new key has been created. It is unlocked and will be used by ConnectBot automatically when connecting to a server.

# Copy Pubkey
[[connectbot.pubkey.details.png|frame|alt=Copy the public key]]
Do a long press on the key to bring up a menu. We want to copy the public portion on the remote server. Click "Copy public key"

# Connect to Server
[[connectbot.connect.to.server.png|frame|alt=Enter server information]]
Go back to the ConnectBot home screen and connect to your SSH server as normal.

# First Connection
[[connectbot.first.connect.png|frame|alt=On first connection the host is unknown]]
Choose "Yes" to accept the server's key if this is the first time connecting to the server.

# Connection Established
[[connectbot.connected.png|frame|alt=Successful connection]]
Login with a username and password to complete the connection. This is now the terminal of the remote server.


# SSH Directory
[[connectbot.cd.ssh.png|frame|alt=Change directory to .ssh]]
The SSH keys and settings are stored in the `.ssh` directory within the user's home. Go into this directory:
```
cd .ssh
```

# Add Key
[[connectbot.authorized.keys.append.png|frame|alt=Add your new key]]
The list of keys accepted for this user is stored in the `authorized_keys` file. The new public key should be appended to this file. Use the `echo` command and paste in the key, surrounded by parentheses. Use `>>` to append the output onto the `authorized_keys` file.
```
echo "PASTEKEYHERE" >> authorized_keys
```
For example:
```
echo "ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAAAgQDQFSzet/Qu8SLklDQyNbX5k16MwOBVKuaY9bNJhb99BkIRIVbNpr61eHUG3gP6haNC6qreTbpHscq4AQV21gLvCgVmHsTci0QAK44weFyDzVwIBFH9uUN+f/k2NTY9zV8FaBqK9CW8hS2f50EB38mGYvE7/0/S1u7/jtxnKqwAgw== htc_aria" >> authorized_keys
```

# Set Permissions for authorized_keys
[[connectbot.authorized.keys.chmod.png|frame|alt=Change permissions for authorized_keys]]
The authorized_keys file must only be writeable the owner. Set the permissions to 644 which means rw-r--r-- if it is not set this way already.
```
chmod 644 authorized_keys
```

# Disconnect
[[connectbot.disconnect.png|frame|alt=After disconnect]]
Disconnect from the server. It will be now be listed on the screen.

# Test Connection
[[connectbot.pubkey.test.png|frame|alt=Test pubkey connection]]
Connect to the server again. While logging in it will say that public key authentication is being attempted:
```
Attempting "publickey" authentication with any in-memory public keys
```
If the key is working, no username or password will be required to complete login. The SSH key authentication is now configured!



# Optional: Disable Key
If the device is lost or access should to be disabled at any time, remove the key from the `authorized_keys` file. Use any text editor, or sed, to find the appropriate line. With a key named htc_aria for example:
```
cd ~/.ssh
sed '/htc_aria$/d' authorized_keys | tee authorized_keys
```


