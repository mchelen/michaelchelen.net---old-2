[[connectbot.htc.aria.300px.png|width=300px|frame|alt=ConnectBot running on HTC Aria from ATT]]


SSH provides secure access to a remote server. Both password and public key authentication are allowed. ConnectBot is an open source SSH client for Android. A key can be created in ConnectBot for use with the server. The key can be disabled at any time. This method can be performed entirely from your Android handset if you currently have password access to an SSH server. ConnectBot supports shell login and port forwarding, and file transfer is planned. Tested with ConnectBot 1.7.0, Android 2.2, and Ubuntu 10.10 Beta.


<br style="clear:both;"/><br />


<ol>
<br style="clear:both;"/><br /><h2><li>Install Open SSH server</li></h2><br />
SSH server must be installed on the remote system. Key authentication is usually enabled by default. To install in Ubuntu:
<pre class="bash source-bash" style="font-family:monospace;">sudo apt-get install openssh-server
</pre>

<br style="clear:both;"/><br /><h2><li>Start ConnectBot</li></h2><br />
<a href="http://www.flickr.com/photos/31831582@N08/4955288167/" title="connectbot by mchelen, on Flickr"><img src="http://farm5.static.flickr.com/4149/4955288167_e94d69e69f_m.jpg" width="160" height="240" alt="connectbot" style="float:right;margin:1em;"/></a><br /><br />
There are no known hosts yet.
<br style="clear:both;"/><br /><h2><li>Manage Pubkeys</li></h2><br />
<a href="http://www.flickr.com/photos/31831582@N08/4955291277/" title="connectbot.menu by mchelen, on Flickr"><img src="http://farm5.static.flickr.com/4083/4955291277_2ce0fc56b0_m.jpg" width="160" height="240" alt="connectbot.menu" style="float:right;margin:1em;"/></a><br /><br />
Click Menu, then Manage Pubkeys to configure keys.

<br style="clear:both;"/><br /><h2><li>Manage Pubkeys Screen</li></h2><br />
<a href="http://www.flickr.com/photos/31831582@N08/4955288431/" title="connectbot.pubkeys by mchelen, on Flickr"><img src="http://farm5.static.flickr.com/4088/4955288431_3f808ff18f_m.jpg" width="160" height="240" alt="connectbot.pubkeys" style="float:right;margin:1em;"/></a><br /><br />
There are no keys set up yet.

<br style="clear:both;"/><br /><h2><li>Generate Pubkey</li></h2><br />
<a href="http://www.flickr.com/photos/31831582@N08/4955291549/" title="connectbot.pubkeys.menu by mchelen, on Flickr"><img src="http://farm5.static.flickr.com/4152/4955291549_abdb5a2316_m.jpg" width="160" height="240" alt="connectbot.pubkeys.menu" style="float:right;margin:1em;"/></a><br /><br />
Click Menu then Generate. We are going to create a new key. This allows us to specifically revoke access if the handset is lost.

<br style="clear:both;"/><br /><h2><li>Generate Pubkey Settings</li></h2><br />
<a href="http://www.flickr.com/photos/31831582@N08/4955288675/" title="connectbot.pubkeys.generate.settings by mchelen, on Flickr"><img src="http://farm5.static.flickr.com/4134/4955288675_f4b3182fd0_m.jpg" width="160" height="240" alt="connectbot.pubkeys.generate.settings" style="float:right;margin:1em;"/></a><br /><br />
Most of the defaults are fine. We will create a 1024 bit RSA key. For added security, use a password for the key. This will let you to securely use the same password on all servers where your key is authorized.

<br style="clear:both;"/><br /><h2><li>Example Settings</li></h2><br />
<a href="http://www.flickr.com/photos/31831582@N08/4955884510/" title="connectbot.pubkeys.generate.settings.example by mchelen, on Flickr"><img src="http://farm5.static.flickr.com/4154/4955884510_8e6b6765fd_m.jpg" width="160" height="240" alt="connectbot.pubkeys.generate.settings.example" style="float:right;margin:1em;"/></a><br /><br />
You can call your key anything you like. I have named mine after the device, htc_aria. Enable "Load key at start" to have the key automatically loaded.

<br style="clear:both;"/><br /><h2><li>Collect Entropy </li></h2><br />
<a href="http://www.flickr.com/photos/31831582@N08/4955881634/" title="connectbot.pubkeys.generate.entropy by mchelen, on Flickr"><img src="http://farm5.static.flickr.com/4124/4955881634_71a231d105_m.jpg" width="160" height="240" alt="connectbot.pubkeys.generate.entropy" style="float:right;margin:1em;"/></a><br /><br />
Random numbers are used to generate the key. Move your finger around the screen until enough is generated.

<br style="clear:both;"/><br /><h2><li>New Pubkey Created</li></h2><br />
<a href="http://www.flickr.com/photos/31831582@N08/4955884774/" title="connectbot.pubkeys.example by mchelen, on Flickr"><img src="http://farm5.static.flickr.com/4153/4955884774_76dd94172a_m.jpg" width="160" height="240" alt="connectbot.pubkeys.example" style="float:right;margin:1em;"/></a><br /><br />
The new key has been created. It is unlocked and will be used by ConnectBot automatically when connecting to a server.

<br style="clear:both;"/><br /><h2><li>Copy Pubkey</li></h2><br />
<a href="http://www.flickr.com/photos/31831582@N08/4955289255/" title="connectbot.pubkeys.details by mchelen, on Flickr"><img src="http://farm5.static.flickr.com/4137/4955289255_ca0d92a86f_m.jpg" width="160" height="240" alt="connectbot.pubkeys.details" style="float:right;margin:1em;"/></a><br /><br />
Do a long press on the key to bring up a menu. We want to copy the public portion on the remote server. Click "Copy public key"

<br style="clear:both;"/><br /><h2><li>Connect to Server</li></h2><br />
<a href="http://www.flickr.com/photos/31831582@N08/5024695974/" title="CAP2010092520341 by mchelen, on Flickr"><img src="http://farm5.static.flickr.com/4086/5024695974_75d625d2ed_m.jpg" width="160" height="240" alt="CAP2010092520341" style="float:right;margin:1em;"/></a><br /><br />
Go back to the ConnectBot home screen and connect to your SSH server as normal.

<br style="clear:both;"/><br /><h2><li>First Connection</li></h2><br />
<a href="http://www.flickr.com/photos/31831582@N08/4955885070/" title="connectbot.first.connect by mchelen, on Flickr"><img src="http://farm5.static.flickr.com/4147/4955885070_b549291ca9_m.jpg" width="160" height="240" alt="connectbot.first.connect" style="float:right;margin:1em;"/></a><br /><br />
Choose "Yes" to accept the server's key if this is the first time connecting to the server.

<br style="clear:both;"/><br /><h2><li>Connection Established</li></h2><br />
<a href="http://www.flickr.com/photos/31831582@N08/4955882494/" title="connectbot.connected by mchelen, on Flickr"><img src="http://farm5.static.flickr.com/4145/4955882494_ca640df7d1_m.jpg" width="160" height="240" alt="connectbot.connected" style="float:right;margin:1em;"/></a><br /><br />
Login with a username and password to complete the connection. This is now the terminal of the remote server.
<br style="clear:both;"/><br /><h2><li>SSH Directory</li></h2><br />
<a href="http://www.flickr.com/photos/31831582@N08/4955883060/" title="connectbot.cd.ssh by mchelen, on Flickr"><img src="http://farm5.static.flickr.com/4104/4955883060_989db07e28_m.jpg" width="160" height="240" alt="connectbot.cd.ssh" style="float:right;margin:1em;"/></a><br /><br />
The SSH keys and settings are stored in the <pre class="bash source-bash" style="font-family:monospace;">.ssh</pre> directory within the user's home. Go into this directory:
<pre class="bash source-bash" style="font-family:monospace;">cd .ssh
</pre>

<br style="clear:both;"/><br /><h2><li>Add Key</li></h2><br />
<a href="http://www.flickr.com/photos/31831582@N08/4955290703/" title="connectbot.authorized.keys.append by mchelen, on Flickr"><img src="http://farm5.static.flickr.com/4125/4955290703_43f2b8a9cb_m.jpg" width="160" height="240" alt="connectbot.authorized.keys.append" style="float:right;margin:1em;"/></a><br /><br />
The list of keys accepted for this user is stored in the <pre class="bash source-bash" style="font-family:monospace;">authorized_keys</pre> file. The new public key should be appended to this file. Use the <pre class="bash source-bash" style="font-family:monospace;">echo</pre> command and paste in the key, surrounded by parentheses. Use <pre class="bash source-bash" style="font-family:monospace;">>></pre> to append the output onto the <pre class="bash source-bash" style="font-family:monospace;">authorized_keys</pre> file.
<pre class="bash source-bash" style="font-family:monospace;">echo "PASTEKEYHERE" >> authorized_keys
</pre>
For example:
<pre class="bash source-bash" style="font-family:monospace;">echo "ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAAAgQDQFSzet/Qu8SLklDQyNbX5k16MwOBVKuaY9bNJhb99BkIRIVbNpr61eHUG3gP6haNC6qreTbpHscq4AQV21gLvCgVmHsTci0QAK44weFyDzVwIBFH9uUN+f/k2NTY9zV8FaBqK9CW8hS2f50EB38mGYvE7/0/S1u7/jtxnKqwAgw== htc_aria" >> authorized_keys
</pre>

<br style="clear:both;"/><br /><h2><li>Set Permissions for authorized_keys </li></h2><br />
<a href="http://www.flickr.com/photos/31831582@N08/4955883782/" title="connectbot.authorized.keys.chmod by mchelen, on Flickr"><img src="http://farm5.static.flickr.com/4086/4955883782_c6ca21e9e8_m.jpg" width="160" height="240" alt="connectbot.authorized.keys.chmod" style="float:right;margin:1em;"/></a><br /><br />
The authorized_keys file must only be writeable the owner. Set the permissions to 644 which means rw-r--r-- if it is not set this way already.
<pre class="bash source-bash" style="font-family:monospace;">chmod 644 authorized_keys
</pre>

<br style="clear:both;"/><br /><h2><li>Disconnect</li></h2><br />
<a href="http://www.flickr.com/photos/31831582@N08/5025271404/" title="CAP2010092600511 by mchelen, on Flickr"><img src="http://farm5.static.flickr.com/4104/5025271404_7acdb02738_m.jpg" width="160" height="240" alt="CAP2010092600511" style="float:right;margin:1em;"/></a>
Disconnect from the server. It will be now be listed on the screen.



<br style="clear:both;"/><br /><h2><li>Test Connection</li></h2><br />
<a href="http://www.flickr.com/photos/31831582@N08/5025263614/" title="CAP2010090616311 by mchelen, on Flickr"><img src="http://farm5.static.flickr.com/4130/5025263614_40d7d8b940_m.jpg" width="160" height="240" alt="CAP2010090616311" style="float:right;margin:1em;"/></a>
Connect to the server again. While logging in it will say that public key authentication is being attempted:
<pre class="text source-text" style="font-family:monospace;">Attempting "publickey" authentication with any in-memory public keys
</pre>
If the key is working, no username or password will be required to complete login. The SSH key authentication is now configured!
<br /><br />


<br style="clear:both;"/><br /><h2><li>Optional: Disable Key</li></h2><br />
If the device is lost or access should to be disabled at any time, remove the key from the <pre class="bash source-bash" style="font-family:monospace;">authorized_keys</pre> file. Use any text editor, or sed, to find the appropriate line. With a key named htc_aria for example:
<pre class="bash source-bash" style="font-family:monospace;">cd ~/.ssh
sed '/htc_aria$/d' authorized_keys | tee authorized_keys</pre>


<!--
<br style="clear:both;"/><br /><h2><li>test</li></h2><br />
blah<br /><br />
-->


</ol>
