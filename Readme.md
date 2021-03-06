#Description
Powershell module that leverages a custom version of the SSH.NET Library (http://sshnet.codeplex.com/) to provide basic SSH functionalyty in Powershell.
The main purpose of the module is to facilitate automating actions against one or multiple SSH enabled servers.

#Install
To install the module including all source code you can just run in a PowerShell v3 the following command:
<pre>
iex (New-Object Net.WebClient).DownloadString("https://gist.github.com/darkoperator/6152630/raw/c67de4f7cd780ba367cccbc2593f38d18ce6df89/instposhsshdev")
</pre>

#Support
* Provides functionality for automating SSH, SFTP and SCP actions.
* Supports diffie-hellman-group-exchange-sha256, diffie-hellman-group-exchange-sha1, diffie-hellman-group14-sha1 and diffie-hellman-group1-sha1 key exchange methods.
* Supports 3des-cbc, aes128-cbc, aes192-cbc, aes256-cbc, aes128-ctr, aes192-ctr, aes256-ctr, blowfish-cbc, cast128-cbc, arcfour and twofish encryptions.
* Supports hmac-md5, hmac-sha1, hmac-ripemd160, hmac-sha2-256, hmac-sha2-256-96, hmac-md5-96 and hmac-sha1-96 hashing algorithms.
* Supports publickey, password and keyboard-interactive authentication methods
* Supports RSA and DSA private key
* Supports DES-EDE3-CBC, DES-EDE3-CFB, DES-CBC, AES-128-CBC, AES-192-CBC and AES-256-CBC algorithms for private key encryption
* Supports SOCKS4, SOCKS5 and HTTP Proxy
* Remote, dynamic and local port forwarding

#ChangeLog

##Version 1.2
* Added support for zlib compression.
* Disabbled Dynamic Port Forward function, there seems to be problems with the library.

##Version 1.1
* Added functions for managing SSH Trusted Host list.
* SCP, SSH Session and SFTP Session cmdlets now verify the SSH Host Fingerprint.
* Complete refactor of the cmdlets for SSH Session, SFTP Session and SCP.
* Added Download and Upload Progress to SCP cmdlets.
* Patched the Renci SSH .Net library to correct problems when uploading using SCP.

# ToDo
* Add progress for SFTP upload and Download

# Know Issues
* No Compression support at the moment.
* Once a Download or Upload is started only way to cancel is by closing PowerShell.
* Subterminals are not supported (su, vi, vim)
