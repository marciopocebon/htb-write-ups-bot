ippsec: [HackTheBox - Helpline](https://youtube.com/watch?v=Vs3oSDlzxwA)

0xdf: [HTB: Helpline](https://0xdf.gitlab.io//2019/08/17/htb-helpline.html)

[00:35](https://youtube.com/watch?v=Vs3oSDlzxwA&t=35) - Begin of Recon

[01:42](https://youtube.com/watch?v=Vs3oSDlzxwA&t=102) - Checking the MangeEngine Page

[02:23](https://youtube.com/watch?v=Vs3oSDlzxwA&t=143) - Running Searchsploit to see potential exploits

[03:40](https://youtube.com/watch?v=Vs3oSDlzxwA&t=220) - Enumerating valid usernames via AjaxDomainServlet

[05:40](https://youtube.com/watch?v=Vs3oSDlzxwA&t=340) - Logging in with guest:guest

[07:10](https://youtube.com/watch?v=Vs3oSDlzxwA&t=430) - Running the privilege escalation script to get Administrator access

[08:00](https://youtube.com/watch?v=Vs3oSDlzxwA&t=480) - Searching for information on this exploit

[08:20](https://youtube.com/watch?v=Vs3oSDlzxwA&t=500) - Blog post missing... Searching Archive.org and Google Cache for a mirror

[10:00](https://youtube.com/watch?v=Vs3oSDlzxwA&t=600) - Making curl go through burp to step through the exploit in BurpSuite

[18:00](https://youtube.com/watch?v=Vs3oSDlzxwA&t=1080) - Copying the admin cookies into FireFox 

[19:25](https://youtube.com/watch?v=Vs3oSDlzxwA&t=1165) - Going to Admin then Custom Triggers to execute code on the server

[21:50](https://youtube.com/watch?v=Vs3oSDlzxwA&t=1310) - Getting a reverse shell via Nishang

[22:30](https://youtube.com/watch?v=Vs3oSDlzxwA&t=1350) - Using iconv to create UTF-16LE encoded Base64 for use with "-EncodedCommand" option

[25:45](https://youtube.com/watch?v=Vs3oSDlzxwA&t=1545) - Reverse Shell as System returned, but EFS Protects the flags

[26:45](https://youtube.com/watch?v=Vs3oSDlzxwA&t=1605) - Finding interesting files with get-childitem -recurse . | select FullName

[28:50](https://youtube.com/watch?v=Vs3oSDlzxwA&t=1730) - Copying mimikatz over to the box to steal NTLM Hashes

[31:00](https://youtube.com/watch?v=Vs3oSDlzxwA&t=1860) - Defender blocked us.  Disable defender with Set-MpPreference -DisableRealtimeMonitoring $true

[32:50](https://youtube.com/watch?v=Vs3oSDlzxwA&t=1970) - Using hashes.org to view password of Zachary, checking his groups to see he can view event logs

[33:30](https://youtube.com/watch?v=Vs3oSDlzxwA&t=2010) - Doing some powershell goodness to search event logs!

[40:50](https://youtube.com/watch?v=Vs3oSDlzxwA&t=2450) - Extracting ProcessCommandLine from the logs (Tolu Password), its a shame Nishang screws with how some commands output to stdout.  This could of been a lot cleaner.

[43:00](https://youtube.com/watch?v=Vs3oSDlzxwA&t=2580) - Using Mimikatz to decrypt the EFS Protected file with Tolu's password

[57:25](https://youtube.com/watch?v=Vs3oSDlzxwA&t=3445) - Need to read Leo's admin-pass.xml, load meterpreter and migrate into his namespace

[01:00:20](https://youtube.com/watch?v=Vs3oSDlzxwA&t=3620) - admin-pass is the output of SecureString, lets decrypt it to get the admin password

[01:02:20](https://youtube.com/watch?v=Vs3oSDlzxwA&t=3740) - Using Invoke-Command with the credential object created to execute commands as administrator

[01:03:50](https://youtube.com/watch?v=Vs3oSDlzxwA&t=3830) - Cannot read root.txt because of "Double Hop Problem" (how PowerShell Authenticates), using CredSSP Authentication to fix this.

-----------------------------------------------------------

ippsec: [HackTheBox - Arkham](https://youtube.com/watch?v=krC5j1Ab44I)

0xdf: [HTB: Arkham](https://0xdf.gitlab.io//2019/08/10/htb-arkham.html)

[00:55](https://youtube.com/watch?v=krC5j1Ab44I&t=55) - Begin of Recon 

[02:20](https://youtube.com/watch?v=krC5j1Ab44I&t=140) - Checking the WebPages

[03:50](https://youtube.com/watch?v=krC5j1Ab44I&t=230) - Examining /userSubscribe.faces, to discover potential deserialization

[05:00](https://youtube.com/watch?v=krC5j1Ab44I&t=300) - Exploring javax.faces.ViewState

[05:50](https://youtube.com/watch?v=krC5j1Ab44I&t=350) - Googling around to see what an unencrypted serialized object should look like

[07:15](https://youtube.com/watch?v=krC5j1Ab44I&t=435) - Checking out SMB to discover an openshare

[09:00](https://youtube.com/watch?v=krC5j1Ab44I&t=540) - Downloading appserver.zip from batshare via smbclient

[11:00](https://youtube.com/watch?v=krC5j1Ab44I&t=660) - Cracking a luks encrypted file with dd and hashcat

[14:00](https://youtube.com/watch?v=krC5j1Ab44I&t=840) - Luks cracked, mounting the disk with luksOpen

[16:20](https://youtube.com/watch?v=krC5j1Ab44I&t=980) - Discovery of the secret used to encrypt the java object

[18:10](https://youtube.com/watch?v=krC5j1Ab44I&t=1090) - Creating a python script to decrypt the ViewState to verify we have correct crypto settings

[23:10](https://youtube.com/watch?v=krC5j1Ab44I&t=1390) - Script completed, lets test the decryption!

[24:15](https://youtube.com/watch?v=krC5j1Ab44I&t=1455) - Downloading ysoserial to create a deserialization CommonCollections gadget

[26:00](https://youtube.com/watch?v=krC5j1Ab44I&t=1560) - Creating a python script to exploit the deserialization vuln

[31:00](https://youtube.com/watch?v=krC5j1Ab44I&t=1860) - Script complete!  We got a ping, testing the MyFaces serialization objects (did not work)

[33:00](https://youtube.com/watch?v=krC5j1Ab44I&t=1980) - Modifying the script to run commands other than what ySoSerial provided

[41:10](https://youtube.com/watch?v=krC5j1Ab44I&t=2470) - Script updates finished, trying to get a reverse shell via nishang (did not work)

[42:40](https://youtube.com/watch?v=krC5j1Ab44I&t=2560) - Trying Invoke-WebRequest, because Net.WebClient did not work.  (testing for constrained mode)

[45:00](https://youtube.com/watch?v=krC5j1Ab44I&t=2700) - Downloading netcat to upload to the box

[46:00](https://youtube.com/watch?v=krC5j1Ab44I&t=2760) - Netcat returned a powershell reverse shell 

[47:20](https://youtube.com/watch?v=krC5j1Ab44I&t=2840) - Discovering Backup.zip, downloading, using readpst to convert it to a plaintext mbox file

[50:00](https://youtube.com/watch?v=krC5j1Ab44I&t=3000) - Using evolution to view mbox file and find Batman's password

[52:45](https://youtube.com/watch?v=krC5j1Ab44I&t=3165) - Using Powershell's Invoke-Command to execute commands as Batman (like runas)

[55:40](https://youtube.com/watch?v=krC5j1Ab44I&t=3340) - Reverse shell as batman returned!  Running a few commands to find out he is localadmin but needs to break out of UAC

[58:10](https://youtube.com/watch?v=krC5j1Ab44I&t=3490) - Unintended: Using net use to mount c$ and view the flag

[59:30](https://youtube.com/watch?v=krC5j1Ab44I&t=3570) - Checking github hfiref0x/UACME to find a UAC Bypass.  Chose one by a fellow HTB Member

[01:02:10](https://youtube.com/watch?v=krC5j1Ab44I&t=3730) - Using GreatSCT/MSBuild to launch Meterpreter

[01:02:45](https://youtube.com/watch?v=krC5j1Ab44I&t=3765) - While GreatSCT installs, create a DLL to return a reverse shell

[01:06:00](https://youtube.com/watch?v=krC5j1Ab44I&t=3960) - copying the DLL into c:\users\batman\appdata\local\microsoft\windowsapps

[01:08:30](https://youtube.com/watch?v=krC5j1Ab44I&t=4110) - Using GreatSCT to generate payloads

[01:11:50](https://youtube.com/watch?v=krC5j1Ab44I&t=4310) - Getting a Meterpreter Session then migrating into an interactive process

[01:17:45](https://youtube.com/watch?v=krC5j1Ab44I&t=4665) - Running SystemPropertiesAdvanced.exe, which elevates and executes our dll

-----------------------------------------------------------

ippsec: [HackTheBox - Fortune](https://youtube.com/watch?v=_BLd046r-co)

0xdf: [HTB: Fortune](https://0xdf.gitlab.io//2019/08/03/htb-fortune.html)

[01:04](https://youtube.com/watch?v=_BLd046r-co&t=64) - Begin of recon

[04:41](https://youtube.com/watch?v=_BLd046r-co&t=281) - Exploring the web page on port 80

[06:02](https://youtube.com/watch?v=_BLd046r-co&t=362) - Using wfuzz to do a special character fuzz to identify odd behavior and discover command injection

[11:06](https://youtube.com/watch?v=_BLd046r-co&t=666) - Creating a hotkey in Burpsuite to send requests in repeater pane

[11:50](https://youtube.com/watch?v=_BLd046r-co&t=710) - Start of creating a python program to automate this

[17:30](https://youtube.com/watch?v=_BLd046r-co&t=1050) - Script finished

[18:30](https://youtube.com/watch?v=_BLd046r-co&t=1110) - Exploring /var/appsrv 

[21:15](https://youtube.com/watch?v=_BLd046r-co&t=1275) - Exploring authpf

[22:30](https://youtube.com/watch?v=_BLd046r-co&t=1350) - Hunting for the signing key for the CA to view HTTPS

[24:40](https://youtube.com/watch?v=_BLd046r-co&t=1480) - Copying the certificates to our box

[26:00](https://youtube.com/watch?v=_BLd046r-co&t=1560) - Creating and signing a Client Certificate

[28:50](https://youtube.com/watch?v=_BLd046r-co&t=1730) - Importing the certificate into FireFox

[30:49](https://youtube.com/watch?v=_BLd046r-co&t=1849) - Discovering the reason our certificate isn't working (time of server is behind)

[31:50](https://youtube.com/watch?v=_BLd046r-co&t=1910) - Accessing the HTTPS Website to get a SSH key for NFSUSER

[33:40](https://youtube.com/watch?v=_BLd046r-co&t=2020) - Discovering additional ports are open after using SSH with NFSUSER

[34:45](https://youtube.com/watch?v=_BLd046r-co&t=2085) - Installing the NFS-COMMON package to get the showmount binary

[35:10](https://youtube.com/watch?v=_BLd046r-co&t=2110) - Mounting a NFS Share with Version 2

[36:00](https://youtube.com/watch?v=_BLd046r-co&t=2160) - Editing our User ID on our box to gain access to the NFS Directories

[37:00](https://youtube.com/watch?v=_BLd046r-co&t=2220) - Reading mail to discover that the root password is set to the Postgres databases root pw

[37:30](https://youtube.com/watch?v=_BLd046r-co&t=2250) - Testing if we could setup a SetUID Binary with this NFS (Check Jail Video for this being successful)

[40:20](https://youtube.com/watch?v=_BLd046r-co&t=2420) - SSH into the box as Charlie and dumping the database

[43:40](https://youtube.com/watch?v=_BLd046r-co&t=2620) - Exploring the source code to the web application

[47:00](https://youtube.com/watch?v=_BLd046r-co&t=2820) - Copying the crypto python script to our box, which will let us decrypt it

[47:40](https://youtube.com/watch?v=_BLd046r-co&t=2860) - Copying the secrets into the crypto python script and decrypting the password

-----------------------------------------------------------

ippsec: [HackTheBox - CTF](https://youtube.com/watch?v=51JQg202csw)

0xdf: [HTB: CTF](https://0xdf.gitlab.io//2019/07/20/htb-ctf.html)

[00:52](https://youtube.com/watch?v=51JQg202csw&t=52) - Start of Recon, discovering CentOS Version via HTTPD Version

[02:15](https://youtube.com/watch?v=51JQg202csw&t=135) - Checking out the HTTP Page

[03:32](https://youtube.com/watch?v=51JQg202csw&t=212) - Checking out login.php

[05:15](https://youtube.com/watch?v=51JQg202csw&t=315) - Identifying a Secure Token is used, most likely STOKEN

[07:05](https://youtube.com/watch?v=51JQg202csw&t=425) - Failing to enumerate usernames through BruteForce

[09:45](https://youtube.com/watch?v=51JQg202csw&t=585) - Fuzzing the login form with special characters to identify a blacklist

[11:45](https://youtube.com/watch?v=51JQg202csw&t=705) - Trying Double URL Encoding to bypass the BlackList

[12:55](https://youtube.com/watch?v=51JQg202csw&t=775) - Explaining Double URL Encoding

[14:45](https://youtube.com/watch?v=51JQg202csw&t=885) - Discovering this is most likely a LDAP Injection

[16:50](https://youtube.com/watch?v=51JQg202csw&t=1010) - Explaining how a LDAP Query Works

[19:15](https://youtube.com/watch?v=51JQg202csw&t=1155) - Identifying the LDAP Query Structure with a Null Byte

[20:40](https://youtube.com/watch?v=51JQg202csw&t=1240) - Injecting the WildCard (*) to enumerate usernames

[24:00](https://youtube.com/watch?v=51JQg202csw&t=1440) - Using Wfuzz to extract the username

[26:00](https://youtube.com/watch?v=51JQg202csw&t=1560) - Enumerating LDAP Attributes that are utilized

[30:26](https://youtube.com/watch?v=51JQg202csw&t=1826) - Creating a python script to extract the Pager Attribute

[41:38](https://youtube.com/watch?v=51JQg202csw&t=2498) - Script complete, lets extract the token

[43:45](https://youtube.com/watch?v=51JQg202csw&t=2625) - Using STOKEN to generate the OTP and logging in

[46:00](https://youtube.com/watch?v=51JQg202csw&t=2760) - Disabling NTP so we can math the server time

[46:44](https://youtube.com/watch?v=51JQg202csw&t=2804) - Discovery of that second half of the original LDAP Query at 16 minutes.

[47:33](https://youtube.com/watch?v=51JQg202csw&t=2853) - Using a Null Byte to remove the GROUP Check.

[50:33](https://youtube.com/watch?v=51JQg202csw&t=3033) - Running Commands

[50:25](https://youtube.com/watch?v=51JQg202csw&t=3025) - Reverse Shell Returned

[53:17](https://youtube.com/watch?v=51JQg202csw&t=3197) - Checking for the LDAP Bind password, then SSHing into the box

[55:00](https://youtube.com/watch?v=51JQg202csw&t=3300) - Going over the /backup directory

[58:20](https://youtube.com/watch?v=51JQg202csw&t=3500) - Using ListFiles to have 7za print our the contents of root.txt

-----------------------------------------------------------

ippsec: [HackTheBox - LaCasaDePapel](https://youtube.com/watch?v=OSRCEOQQJ4E)

0xdf: [HTB: LaCasaDePapel](https://0xdf.gitlab.io//2019/07/27/htb-lacasadepapel.html)

[01:05](https://youtube.com/watch?v=OSRCEOQQJ4E&t=65) - Start of nmap

[02:50](https://youtube.com/watch?v=OSRCEOQQJ4E&t=170) - Attempting to execute an VSFTPD Backdoor via MSF

[03:40](https://youtube.com/watch?v=OSRCEOQQJ4E&t=220) - Discovering the backdoor opened 6200, discovering a weird shell

[04:50](https://youtube.com/watch?v=OSRCEOQQJ4E&t=290) - Lets figure out what just happened

[06:50](https://youtube.com/watch?v=OSRCEOQQJ4E&t=410) - Triggering the backdoor without Metasploit

[09:05](https://youtube.com/watch?v=OSRCEOQQJ4E&t=545) - Exploring the Psy PHP Shell opened up by the backdoor

[10:20](https://youtube.com/watch?v=OSRCEOQQJ4E&t=620) - Several functions for executing bash aren't working, checking disable_functions

[11:40](https://youtube.com/watch?v=OSRCEOQQJ4E&t=700) - Attempting to bypass disabled_functions (does not work)

[12:50](https://youtube.com/watch?v=OSRCEOQQJ4E&t=770) - Using ScanDir() and File_Get_Contents(), to explore the filesystem

[14:50](https://youtube.com/watch?v=OSRCEOQQJ4E&t=890) - Identifying we are probably running as the Dali User (Unintended Path)

[17:00](https://youtube.com/watch?v=OSRCEOQQJ4E&t=1020) - Downloading CA.KEY, which is a private key to a webserver

[21:40](https://youtube.com/watch?v=OSRCEOQQJ4E&t=1300) - Using the CA.KEY to generate client certificates to access the HTTPS Page

[30:25](https://youtube.com/watch?v=OSRCEOQQJ4E&t=1825) - Weird it didn't work, lets just verify all our certificates are good

[32:28](https://youtube.com/watch?v=OSRCEOQQJ4E&t=1948) - This time it worked! We connected to the server

[33:20](https://youtube.com/watch?v=OSRCEOQQJ4E&t=2000) - Failing to add the certificate to BurpSuite

[33:50](https://youtube.com/watch?v=OSRCEOQQJ4E&t=2030) - Discovering File Traversal by editing the PATH variable

[36:38](https://youtube.com/watch?v=OSRCEOQQJ4E&t=2198) - Discovering the LFI just puts the path as Base64 Encoded

[37:15](https://youtube.com/watch?v=OSRCEOQQJ4E&t=2235) - Using the LFI to download the SSH Private Key

[38:45](https://youtube.com/watch?v=OSRCEOQQJ4E&t=2325) - Testing SSH Key against users on the box to gain access!

[39:13](https://youtube.com/watch?v=OSRCEOQQJ4E&t=2353) - UNINTENDED: Skipping the HTTPS Certificate - Generating SSH Keys to upload via PHP Shell

[40:30](https://youtube.com/watch?v=OSRCEOQQJ4E&t=2430) - UNINTENDED: Using file_put_contents() to append our public key to authorized_keys

[41:30](https://youtube.com/watch?v=OSRCEOQQJ4E&t=2490) - UNINTENDED: Using SSH to tunnel through Dali (SOCKS Proxy)

[42:30](https://youtube.com/watch?v=OSRCEOQQJ4E&t=2550) - UNINTENDED: Scanning ports on Dali that are listening on LocalHost

[43:08](https://youtube.com/watch?v=OSRCEOQQJ4E&t=2588) - UNINTENDED: Port 8000 is open, and its one step after the Reverse_Proxy that performs SSL Authentication!

[45:35](https://youtube.com/watch?v=OSRCEOQQJ4E&t=2735) - Running PSPY and LinEnum

[50:20](https://youtube.com/watch?v=OSRCEOQQJ4E&t=3020) - Using PSPY to view FileSystem Events which will show the cron

[52:30](https://youtube.com/watch?v=OSRCEOQQJ4E&t=3150) - Taking control of ~/memcached.ini because we own the folder!

[54:45](https://youtube.com/watch?v=OSRCEOQQJ4E&t=3285) - Exploiting the cron that utilizes memcached.ini to get a root shell

[55:55](https://youtube.com/watch?v=OSRCEOQQJ4E&t=3355) - Exploring how the SSL Authentication is working

60:00 - Exploring how the VSFTPD Backdoor was modified.

-----------------------------------------------------------

ippsec: [HackTheBox - FriendZone](https://youtube.com/watch?v=Zf8p49IzEEA)

0xdf: [HTB: FriendZone](https://0xdf.gitlab.io//2019/07/13/htb-friendzone.html)

[00:45](https://youtube.com/watch?v=Zf8p49IzEEA&t=45) - Begin of Recon

[04:10](https://youtube.com/watch?v=Zf8p49IzEEA&t=250) - Running SMBMap to identify and crawl file shares

[05:00](https://youtube.com/watch?v=Zf8p49IzEEA&t=300) - Downloading creds.txt from an smb share and checking FTP/SMB

[06:50](https://youtube.com/watch?v=Zf8p49IzEEA&t=410) - Checking the webpage and grabbing potential DNS Names for the box

[10:40](https://youtube.com/watch?v=Zf8p49IzEEA&t=640) - Using dig to perform a DNS Zone Transfer to obtain additional host names

[12:00](https://youtube.com/watch?v=Zf8p49IzEEA&t=720) - Adding all hostnames to /etc/hosts

[12:55](https://youtube.com/watch?v=Zf8p49IzEEA&t=775) - Running Aquatone to take screenshots of all the pages for quick examination

[15:15](https://youtube.com/watch?v=Zf8p49IzEEA&t=915) - Testing Uploads.Friendzone.red

[16:30](https://youtube.com/watch?v=Zf8p49IzEEA&t=990) - Testing admin.friendzone.red

[17:00](https://youtube.com/watch?v=Zf8p49IzEEA&t=1020) - Testing administrator1.friendzone.red, logging in with creds found from SMB

[18:35](https://youtube.com/watch?v=Zf8p49IzEEA&t=1115) - Found an LFI in the Dashboard.PHP script (PageName Variable)

[20:15](https://youtube.com/watch?v=Zf8p49IzEEA&t=1215) - Using PHP Wrappers with the LFI To obtain PHP Script Source

[23:00](https://youtube.com/watch?v=Zf8p49IzEEA&t=1380) - Revisiting recon to find ways to upload files, end up using SMBClient

[25:10](https://youtube.com/watch?v=Zf8p49IzEEA&t=1510) - Gaining code execution through the LFI Exploit and SMB File Share

[27:30](https://youtube.com/watch?v=Zf8p49IzEEA&t=1650) - Reverse Shell Returned

[28:50](https://youtube.com/watch?v=Zf8p49IzEEA&t=1730) - Exploring /var/www/html to see if any troll directories had useful files in them, find creds to Friend user

[31:20](https://youtube.com/watch?v=Zf8p49IzEEA&t=1880) - Running PSPY to identify cron jobs we don't have permission to see

[33:15](https://youtube.com/watch?v=Zf8p49IzEEA&t=1995) - Running LinEnum.sh to enumerate the box and discover the Python OS Library is writeable

[38:20](https://youtube.com/watch?v=Zf8p49IzEEA&t=2300) - Fixing our reverse shell by setting ROWS and COLUMNS of our terminal so we can use Vi

[40:45](https://youtube.com/watch?v=Zf8p49IzEEA&t=2445) - Placing a reverse shell in the Python OS library

-----------------------------------------------------------

ippsec: [HackTheBox - HackBack](https://youtube.com/watch?v=B9nozi1PrhY)

0xdf: [HTB: Hackback](https://0xdf.gitlab.io//2019/07/06/htb-hackback.html)

[00:01:30](https://youtube.com/watch?v=B9nozi1PrhY&t=90) - Begin of Recon, discovery of an HTTP API that has a few commands

[00:06:00](https://youtube.com/watch?v=B9nozi1PrhY&t=360) - Using JQ to parse json output, use NetStat/Proc to find GoPhish

[00:15:00](https://youtube.com/watch?v=B9nozi1PrhY&t=900) - Logging into GoPhish with default creds admin:gophish, finding DNS Names

[00:21:15](https://youtube.com/watch?v=B9nozi1PrhY&t=1275) - Discovery of Obfuscated JavaScript Deobfuscating it to find a hidden section

[00:33:20](https://youtube.com/watch?v=B9nozi1PrhY&t=2000) - Using wfuzz to bruteforce the password for webadmin.php

[00:37:10](https://youtube.com/watch?v=B9nozi1PrhY&t=2230) - Finding Code Execution in WebAdmin.php

[00:44:00](https://youtube.com/watch?v=B9nozi1PrhY&t=2640) - Creating a Python Script to give a pseudo shell to cat, ls, and upload

[01:10:45](https://youtube.com/watch?v=B9nozi1PrhY&t=4245) - Script finished, uploading reGeorg to create a proxy onto the box to bypass FW

[01:16:20](https://youtube.com/watch?v=B9nozi1PrhY&t=4580) - Using WinRM to access low privilege shell as Simple User

[01:25:08](https://youtube.com/watch?v=B9nozi1PrhY&t=5108) - Exploring /Util/Scripts to find a way to privesc to Hacker

[01:30:29](https://youtube.com/watch?v=B9nozi1PrhY&t=5429) - Exploring GetSystem functionality of meterpreter

[01:37:20](https://youtube.com/watch?v=B9nozi1PrhY&t=5840) - Starting to create program to steal a token from NamedPipe Clients

[01:41:00](https://youtube.com/watch?v=B9nozi1PrhY&t=6060) - Creating XOR Encrypter for payloads in C (There is a bug used & instead of %)

[01:48:20](https://youtube.com/watch?v=B9nozi1PrhY&t=6500) - Using MSFVenom to generate raw payload to XOR then generate in C Format

[01:51:38](https://youtube.com/watch?v=B9nozi1PrhY&t=6698) - Creating the Stager to execute meterpreter, with some fun old AV Evasion tactics

[02:03:45](https://youtube.com/watch?v=B9nozi1PrhY&t=7425) - Found the issue, AND'd the payload instead of XOR'd in encrypt.c

[02:08:30](https://youtube.com/watch?v=B9nozi1PrhY&t=7710) - Creating the NamedPipe portion of code

[02:28:30](https://youtube.com/watch?v=B9nozi1PrhY&t=8910) - Creating the Pipe Impersonation part of the code

[02:43:16](https://youtube.com/watch?v=B9nozi1PrhY&t=9796) - Had some weird errors, adding the ability to enable token privileges

[03:01:00](https://youtube.com/watch?v=B9nozi1PrhY&t=10860) - Editing the /util/scripts/clean.ini to execute our NamedPipe Creation File

[03:06:10](https://youtube.com/watch?v=B9nozi1PrhY&t=11170) - Meterpreter Session Loaded.  Unfortunately it grab the impersonation token, more troubleshooting.

[03:08:20](https://youtube.com/watch?v=B9nozi1PrhY&t=11300) - Found the bug that caused us to not pass the token

[03:09:45](https://youtube.com/watch?v=B9nozi1PrhY&t=11385) - Re-Explaining all the code

[03:14:57](https://youtube.com/watch?v=B9nozi1PrhY&t=11697) - Meterpreter loaded, using incognito to grab our impersonation token for HACKER user

[03:30:15](https://youtube.com/watch?v=B9nozi1PrhY&t=12615) - Creating a bat file to run NetCat and upload into /util/scripts/spool which gets executed

[03:35:50](https://youtube.com/watch?v=B9nozi1PrhY&t=12950) - Start of looking at UserLogger Service, download it, un-UPX it

[03:41:30](https://youtube.com/watch?v=B9nozi1PrhY&t=13290) - Using ProcessMonitor to Dynamically Analyze the UserLogger binary (think of strace on windows)

[03:49:40](https://youtube.com/watch?v=B9nozi1PrhY&t=13780) - UserLogger lets us write binaries as SYSTEM with 777 permissions! Lets chain Diagnostic Hub Exploit

[03:52:00](https://youtube.com/watch?v=B9nozi1PrhY&t=13920) - Changing CMDLine in FakeDLL and valid_dir in Diaghub_exploit.cpp

[04:18:05](https://youtube.com/watch?v=B9nozi1PrhY&t=15485) - Changing from DEBUG mode to RELEASE mode for compiling.  Which fixes it.

[04:25:15](https://youtube.com/watch?v=B9nozi1PrhY&t=15915) - Root.txt is hidden behind alternate data streams.

[04:27:39](https://youtube.com/watch?v=B9nozi1PrhY&t=16059) - ALTERNATE PATH THAT LETS YOU SKIP NAMEDPIPE STUFF

-----------------------------------------------------------

ippsec: [HackTheBox - Netmon](https://youtube.com/watch?v=ZxvgniJXbOo)

0xdf: [HTB: Netmon](https://0xdf.gitlab.io//2019/06/29/htb-netmon.html)

[01:00](https://youtube.com/watch?v=ZxvgniJXbOo&t=60) - Begin of Recon

[03:50](https://youtube.com/watch?v=ZxvgniJXbOo&t=230) - Searching for good files to view via FTP

[09:00](https://youtube.com/watch?v=ZxvgniJXbOo&t=540) - Nothing really found, searching for where PRTG creation file is

[14:34](https://youtube.com/watch?v=ZxvgniJXbOo&t=874) - Backup configuration found!

[16:20](https://youtube.com/watch?v=ZxvgniJXbOo&t=980) - Logging in by incrementing the password from 2018 to 2019

[17:55](https://youtube.com/watch?v=ZxvgniJXbOo&t=1075) - Searching for CVE's

[19:45](https://youtube.com/watch?v=ZxvgniJXbOo&t=1185) - Searching for where to send notification emails like CVE Said

[20:30](https://youtube.com/watch?v=ZxvgniJXbOo&t=1230) - Testing for Command Injection via Cmd

[22:20](https://youtube.com/watch?v=ZxvgniJXbOo&t=1340) - Testing for Command Injection via Powershell

[23:00](https://youtube.com/watch?v=ZxvgniJXbOo&t=1380) - Getting a reverse shell

[26:55](https://youtube.com/watch?v=ZxvgniJXbOo&t=1615) - Encoding powershell in Base64 to eliminate potential bad characters

[29:10](https://youtube.com/watch?v=ZxvgniJXbOo&t=1750) - Getting a reverse shell

-----------------------------------------------------------

ippsec: [HackTheBox - Querier](https://youtube.com/watch?v=d7ACjty4m7U)

0xdf: [HTB: Querier](https://0xdf.gitlab.io//2019/06/22/htb-querier.html)

[00:50](https://youtube.com/watch?v=d7ACjty4m7U&t=50) - Begin of Reocn

[03:30](https://youtube.com/watch?v=d7ACjty4m7U&t=210) - Using SMBMap to enumerate fileshares

[05:45](https://youtube.com/watch?v=d7ACjty4m7U&t=345) - Discovering an Excel Macro File

[09:25](https://youtube.com/watch?v=d7ACjty4m7U&t=565) - Using olevba to extract macro from the document to discover credentials

[11:15](https://youtube.com/watch?v=d7ACjty4m7U&t=675) - Using MSSQLClient.py from Impacket to log into the SQL Server

[12:15](https://youtube.com/watch?v=d7ACjty4m7U&t=735) - Doing the SQL CMD:XP_DIRTREE to read a file off a UNC Share to steal the hash with Responder

[13:15](https://youtube.com/watch?v=d7ACjty4m7U&t=795) - Cracking the NetNTLMv2 Hash

[14:11](https://youtube.com/watch?v=d7ACjty4m7U&t=851) - Explaining the Responder Database file to view previously captured hashes

[16:30](https://youtube.com/watch?v=d7ACjty4m7U&t=990) - Logging into the SQL Server with the cracked account, then doing XP_CMDSHELL to run commands

[17:50](https://youtube.com/watch?v=d7ACjty4m7U&t=1070) - Getting a Nishang Reverse Shell

[22:00](https://youtube.com/watch?v=d7ACjty4m7U&t=1320) - Running PowerUp, doing Invoke-ServiceAbuse and discovering creds in an old Group Policy Object

[26:30](https://youtube.com/watch?v=d7ACjty4m7U&t=1590) - Going back to the password disclosed via Group Policy and discovering they are an administrator

[28:00](https://youtube.com/watch?v=d7ACjty4m7U&t=1680) - Explaining how the PowerUp module decrypted a password out of Group Policy

[29:10](https://youtube.com/watch?v=d7ACjty4m7U&t=1750) - Getting VIM to highlight the syntax of Powershell

[34:50](https://youtube.com/watch?v=d7ACjty4m7U&t=2090) - Rooting the box with Invoke-ServiceAbuse

-----------------------------------------------------------

ippsec: [HackTheBox - Flujab](https://youtube.com/watch?v=_f9Xygr-qHU)

0xdf: [HTB: FluJab](https://0xdf.gitlab.io//2019/06/15/htb-flujab.html)

[01:30](https://youtube.com/watch?v=_f9Xygr-qHU&t=90) - Begin of Recon

[04:15](https://youtube.com/watch?v=_f9Xygr-qHU&t=255) - Adding DNS Names to /etc/hosts

[05:20](https://youtube.com/watch?v=_f9Xygr-qHU&t=320) - Using Aquatone to take HTTP Screenshots of a bunch of pages

[11:00](https://youtube.com/watch?v=_f9Xygr-qHU&t=660) - Start of looking at FreeFlujab.htb

[15:40](https://youtube.com/watch?v=_f9Xygr-qHU&t=940) - Looking at HTTP Cookies we send

[17:40](https://youtube.com/watch?v=_f9Xygr-qHU&t=1060) - Editing Cookies in Firefox

[19:50](https://youtube.com/watch?v=_f9Xygr-qHU&t=1190) - Discovering SMTP_CONFIG, which lets us change where the mail server is

[21:50](https://youtube.com/watch?v=_f9Xygr-qHU&t=1310) - Using FireFox to remove character restrictions on a page

[24:15](https://youtube.com/watch?v=_f9Xygr-qHU&t=1455) - The WebPage kept resetting our cookie, using Burp to auto replace

[27:30](https://youtube.com/watch?v=_f9Xygr-qHU&t=1650) - Standing up a SMTP Server in python to read mail

[30:20](https://youtube.com/watch?v=_f9Xygr-qHU&t=1820) - Discovering SQL Injection

[34:50](https://youtube.com/watch?v=_f9Xygr-qHU&t=2090) - SQL Injection confirmed, testing Union Injections

[37:40](https://youtube.com/watch?v=_f9Xygr-qHU&t=2260) - Creating a Python Script to aid us in running SQL Injections

[37:40](https://youtube.com/watch?v=_f9Xygr-qHU&t=2260) - Script: Running a SMTP Server in background thread

[41:35](https://youtube.com/watch?v=_f9Xygr-qHU&t=2495) - Script: Adding ability to use arrow keys to go to previous command

[46:42](https://youtube.com/watch?v=_f9Xygr-qHU&t=2802) - Script: Making our command prompt send HTTP Requests

[52:40](https://youtube.com/watch?v=_f9Xygr-qHU&t=3160) - Dumping database structure from INFORMATION_SCHEMA

-----------------------------------------------------------

ippsec: [HackTheBox - Help](https://youtube.com/watch?v=XB8CbhfOczU)

0xdf: [HTB: Helpline](https://0xdf.gitlab.io//2019/08/17/htb-helpline.html)

0xdf: [HTB: Help](https://0xdf.gitlab.io//2019/06/08/htb-help.html)

[00:49](https://youtube.com/watch?v=XB8CbhfOczU&t=49) - Begin of recon

[01:45](https://youtube.com/watch?v=XB8CbhfOczU&t=105) - Running gobuster to find /support

[02:50](https://youtube.com/watch?v=XB8CbhfOczU&t=170) - Searching for a way to find version of HelpdeskZ

[03:35](https://youtube.com/watch?v=XB8CbhfOczU&t=215) - Reading over the File Upload exploit script to see it requires server time

[05:10](https://youtube.com/watch?v=XB8CbhfOczU&t=310) - Uploading a PHP Reverse Shell Script

[07:45](https://youtube.com/watch?v=XB8CbhfOczU&t=465) - Going back to GitHub to find where uploads are saved

[09:10](https://youtube.com/watch?v=XB8CbhfOczU&t=550) - Begin of modifying the script to pull the server time out of HTTP Headers

[10:30](https://youtube.com/watch?v=XB8CbhfOczU&t=630) - Figuring out the python to pull the "Date" HTTP Header

[14:30](https://youtube.com/watch?v=XB8CbhfOczU&t=870) - Getting the Time Format right with STRFTIME.COM

[19:40](https://youtube.com/watch?v=XB8CbhfOczU&t=1180) - Testing out the exploit and getting a shell

[23:20](https://youtube.com/watch?v=XB8CbhfOczU&t=1400) - Discovery of an old kernel, looking for an exploit

[24:30](https://youtube.com/watch?v=XB8CbhfOczU&t=1470) - Copying the exploit, compiling, and privesc!

[25:50](https://youtube.com/watch?v=XB8CbhfOczU&t=1550) - Looking into port 3000

[27:00](https://youtube.com/watch?v=XB8CbhfOczU&t=1620) - /graphql discovered

[27:42](https://youtube.com/watch?v=XB8CbhfOczU&t=1662) - Dumping the schema to discover what data is inside

[30:15](https://youtube.com/watch?v=XB8CbhfOczU&t=1815) - Dumping username, password from the database

[32:12](https://youtube.com/watch?v=XB8CbhfOczU&t=1932) - Logging into HelpdeskZ

[33:40](https://youtube.com/watch?v=XB8CbhfOczU&t=2020) - Discovering the Boolean SQL Injection

[34:50](https://youtube.com/watch?v=XB8CbhfOczU&t=2090) - Running SQLMap

[36:00](https://youtube.com/watch?v=XB8CbhfOczU&t=2160) - Explaining the Injection

[37:10](https://youtube.com/watch?v=XB8CbhfOczU&t=2230) - Begin of creating a python script to exploit this

-----------------------------------------------------------

ippsec: [HackTheBox - Sizzle](https://youtube.com/watch?v=YVhlfUvsqYc)

0xdf: [HTB: Sizzle](https://0xdf.gitlab.io//2019/06/01/htb-sizzle.html)

[01:04](https://youtube.com/watch?v=YVhlfUvsqYc&t=64) - Begin of Recon

[06:45](https://youtube.com/watch?v=YVhlfUvsqYc&t=405) - Checking the web interfaces

[07:20](https://youtube.com/watch?v=YVhlfUvsqYc&t=440) - Discovering there is a Certificate Authority

[08:50](https://youtube.com/watch?v=YVhlfUvsqYc&t=530) - Taking a look at LDAP

[10:55](https://youtube.com/watch?v=YVhlfUvsqYc&t=655) - Examining SMB to find shares

[12:00](https://youtube.com/watch?v=YVhlfUvsqYc&t=720) - Searching the Operations and Department Shares

[14:50](https://youtube.com/watch?v=YVhlfUvsqYc&t=890) - Viewing permissions of a SMB Share with SMBCACLS

[19:10](https://youtube.com/watch?v=YVhlfUvsqYc&t=1150) - Discovering a writeable share, dropping a SCF File to get a hash

[22:04](https://youtube.com/watch?v=YVhlfUvsqYc&t=1324) - Using Hashcat to crack NetNTLMv2

[24:40](https://youtube.com/watch?v=YVhlfUvsqYc&t=1480) - Using SMBMap to identify if this user has access to anything extra

[25:40](https://youtube.com/watch?v=YVhlfUvsqYc&t=1540) - Discovering the CertSRV Directory 

[28:00](https://youtube.com/watch?v=YVhlfUvsqYc&t=1680) - Discovering Powershell Remoting

[30:00](https://youtube.com/watch?v=YVhlfUvsqYc&t=1800) - Error from WinRM (Need SSL)

[31:00](https://youtube.com/watch?v=YVhlfUvsqYc&t=1860) - Using openSSL to generate a private key

[31:52](https://youtube.com/watch?v=YVhlfUvsqYc&t=1912) - Going to /CertSRV to sign our certificate as Amanda

[34:00](https://youtube.com/watch?v=YVhlfUvsqYc&t=2040) - Adding the SSL Authentication to WinrM

[35:15](https://youtube.com/watch?v=YVhlfUvsqYc&t=2115) - Playing with LDAP Again (with the Amanda Creds)

[37:50](https://youtube.com/watch?v=YVhlfUvsqYc&t=2270) - Shell on the box with WinRM as Amanda

[38:15](https://youtube.com/watch?v=YVhlfUvsqYc&t=2295) - Running SharpHound

[40:29](https://youtube.com/watch?v=YVhlfUvsqYc&t=2429) - Applocker is on the box, lets move it in the windows directory 

[42:00](https://youtube.com/watch?v=YVhlfUvsqYc&t=2520) - Trying to get the bloodhound data off the box.

[44:20](https://youtube.com/watch?v=YVhlfUvsqYc&t=2660) - Starting bloodhound 

[45:27](https://youtube.com/watch?v=YVhlfUvsqYc&t=2727) - File didn't copy lets load up Covenant

[49:30](https://youtube.com/watch?v=YVhlfUvsqYc&t=2970) - Covenant is up and running - Create a HTTP Listener

[50:30](https://youtube.com/watch?v=YVhlfUvsqYc&t=3030) - Hosting a Launcher

[52:30](https://youtube.com/watch?v=YVhlfUvsqYc&t=3150) - Getting a grunt

[54:40](https://youtube.com/watch?v=YVhlfUvsqYc&t=3280) - Running SeatBelt

[57:00](https://youtube.com/watch?v=YVhlfUvsqYc&t=3420) - Running SharpHound

60:00 - Finally uploading the bloodhound data

[01:01:18](https://youtube.com/watch?v=YVhlfUvsqYc&t=3678) - Running Bloodhound with all Collection Methods

[01:05:15](https://youtube.com/watch?v=YVhlfUvsqYc&t=3915) - Discovering the MRLKY can DCSYNC

[01:07:25](https://youtube.com/watch?v=YVhlfUvsqYc&t=4045) - Cannot kerberoast because of the Double Hop Problem, create token with MakeToken

[01:12:30](https://youtube.com/watch?v=YVhlfUvsqYc&t=4350) - Cracked the Kerberoasted Hash, doing maketoken with mrlky and running DCSYnc

[01:14:40](https://youtube.com/watch?v=YVhlfUvsqYc&t=4480) - Running WMIExec to get Administrator

[01:22:00](https://youtube.com/watch?v=YVhlfUvsqYc&t=4920) - UNINTENDED Method 1: Amanda can write to Clean.bat

[01:24:30](https://youtube.com/watch?v=YVhlfUvsqYc&t=5070) - UNINTENDED Method 2: Forensic artifacts leave MRKLY Hash in C:\windows\system32\file.txt

-----------------------------------------------------------

ippsec: [HackTheBox - Conceal](https://youtube.com/watch?v=1ae64CdwLHE)

0xdf: [HTB: Conceal](https://0xdf.gitlab.io//2019/05/18/htb-conceal.html)

[01:15](https://youtube.com/watch?v=1ae64CdwLHE&t=75) - Begin of recon

[02:54](https://youtube.com/watch?v=1ae64CdwLHE&t=174) - Checking SNMP with snmpwalk

[03:29](https://youtube.com/watch?v=1ae64CdwLHE&t=209) - Discovering a Hashed PSK (MD5) in SNMPWalk, searching the internet for a decrypted value

[04:18](https://youtube.com/watch?v=1ae64CdwLHE&t=258) - Getting more SNMP Information with snmp-check

[07:35](https://youtube.com/watch?v=1ae64CdwLHE&t=455) - Going over UDP Ports discovered by snmp-check

[10:55](https://youtube.com/watch?v=1ae64CdwLHE&t=655) - Running ike-scan

[11:55](https://youtube.com/watch?v=1ae64CdwLHE&t=715) - Examining ike-scan results to build a IPSEC Config

[13:50](https://youtube.com/watch?v=1ae64CdwLHE&t=830) - Installing Strongswan (IPSEC/VPN Program)

[14:19](https://youtube.com/watch?v=1ae64CdwLHE&t=859) - Adding the PSK Found earlier to /etc/ipsec.secrets

[15:30](https://youtube.com/watch?v=1ae64CdwLHE&t=930) - Begin configuring /etc/ipsec.conf

[20:08](https://youtube.com/watch?v=1ae64CdwLHE&t=1208) - Starting and debugging ipsec

[21:55](https://youtube.com/watch?v=1ae64CdwLHE&t=1315) - Explaining why we add TCP to strongswan config

[24:00](https://youtube.com/watch?v=1ae64CdwLHE&t=1440) - Starting IPSEC, then using NMAP through IPSEC.

[25:55](https://youtube.com/watch?v=1ae64CdwLHE&t=1555) - Enumerating SMB Quickly (SMBMap/cme)

[26:50](https://youtube.com/watch?v=1ae64CdwLHE&t=1610) - Enumerating FTP, discovering we can upload files

[27:20](https://youtube.com/watch?v=1ae64CdwLHE&t=1640) - Checking HTTP, hunting for our uploaded file.  Then uploading files that may lead to code execution

[29:44](https://youtube.com/watch?v=1ae64CdwLHE&t=1784) - Grabbing an ASP Webshell from Github/tennc/webshell

[32:08](https://youtube.com/watch?v=1ae64CdwLHE&t=1928) - Webshell has been uploaded

[32:30](https://youtube.com/watch?v=1ae64CdwLHE&t=1950) - Explaining a weird MTU Issue you *may* run into due to the nested VPN's

[35:40](https://youtube.com/watch?v=1ae64CdwLHE&t=2140) - Back to playing with the web shell, getting a reverse shell with Nishang

[38:03](https://youtube.com/watch?v=1ae64CdwLHE&t=2283) - Explaining RLWRAP

[38:40](https://youtube.com/watch?v=1ae64CdwLHE&t=2320) - whoami /all shows SEImpersonation, so we run JuicyPotato to privesc

[44:35](https://youtube.com/watch?v=1ae64CdwLHE&t=2675) - JuicyPotato fails with the default CLSID, changing it up to get it working.

[46:30](https://youtube.com/watch?v=1ae64CdwLHE&t=2790) - Doing the box again with Windows

[47:15](https://youtube.com/watch?v=1ae64CdwLHE&t=2835) - Setting up the IPSEC Connection through Windows Firewall

[50:00](https://youtube.com/watch?v=1ae64CdwLHE&t=3000) - Installing a DotNet C2 (The Covenant)

[54:20](https://youtube.com/watch?v=1ae64CdwLHE&t=3260) - Covenant/Elite open, starting a Listener then a Powershell Launcher

[01:00:10](https://youtube.com/watch?v=1ae64CdwLHE&t=3610) - Grunt activated. Running Seatbelt, then compiling Watson and reflectively running it

[01:05:00](https://youtube.com/watch?v=1ae64CdwLHE&t=3900) - Grabbing the Sandbox Escaper ALPC Privesc

[01:08:03](https://youtube.com/watch?v=1ae64CdwLHE&t=4083) - Being lazy and compiling a CPP Rev Shell in Linux because it wasn't installed on Windows

[01:25:35](https://youtube.com/watch?v=1ae64CdwLHE&t=5135) - Box is reverted, trying the ALPC Exploit again

-----------------------------------------------------------

ippsec: [HackTheBox - LightWeight](https://youtube.com/watch?v=yQgtDoCDAYk)

0xdf: [HTB: Lightweight](https://0xdf.gitlab.io//2019/05/11/htb-lightweight.html)

[00:45](https://youtube.com/watch?v=yQgtDoCDAYk&t=45) - Begin of recon, Nmap

[01:30](https://youtube.com/watch?v=yQgtDoCDAYk&t=90) - Taking the CentOS Apache Version to find major version

[03:20](https://youtube.com/watch?v=yQgtDoCDAYk&t=200) - Running GoBuster with a Common-PHP-Files wordlist.

[06:00](https://youtube.com/watch?v=yQgtDoCDAYk&t=360) - Enumerating Ldap with ldapsearch

[07:30](https://youtube.com/watch?v=yQgtDoCDAYk&t=450) - Discovery of Password Hashes within ldap information

[10:55](https://youtube.com/watch?v=yQgtDoCDAYk&t=655) - Attempting to crack the hashes. (does not crack)

[12:30](https://youtube.com/watch?v=yQgtDoCDAYk&t=750) - Back to the web page

[13:15](https://youtube.com/watch?v=yQgtDoCDAYk&t=795) - Page says to login with ip@Lightweight with the password of your ip

[15:35](https://youtube.com/watch?v=yQgtDoCDAYk&t=935) - Running LinEnum

[20:15](https://youtube.com/watch?v=yQgtDoCDAYk&t=1215) - Discovery of Extended Capabilities set on tcpdump

[20:50](https://youtube.com/watch?v=yQgtDoCDAYk&t=1250) - Performing a packet capture over SSH without touching disk

[23:45](https://youtube.com/watch?v=yQgtDoCDAYk&t=1425) - Examining the pcap created, don't see anything on ens33

[24:20](https://youtube.com/watch?v=yQgtDoCDAYk&t=1460) - Performing a packet capture through SSH and piping live results to WireShark

[26:00](https://youtube.com/watch?v=yQgtDoCDAYk&t=1560) - Discovery of LDAP Traffic, ldapuser2 password passed in clear-text

[28:15](https://youtube.com/watch?v=yQgtDoCDAYk&t=1695) - Using bash to exfil a file over the network (backup.7z)

[29:25](https://youtube.com/watch?v=yQgtDoCDAYk&t=1765) - Using 7z2john and hashcat to crack a 7zip file

[32:05](https://youtube.com/watch?v=yQgtDoCDAYk&t=1925) - Examining extracted files to discover a new credential (ldapuser1)

[33:30](https://youtube.com/watch?v=yQgtDoCDAYk&t=2010) - The openssl binary in ldapuser1 has an empty capability (which is all)

[35:00](https://youtube.com/watch?v=yQgtDoCDAYk&t=2100) - Using GTFOBins to see what we can do with openssl

[37:11](https://youtube.com/watch?v=yQgtDoCDAYk&t=2231) - Reading /etc/shadow with openssl

[37:35](https://youtube.com/watch?v=yQgtDoCDAYk&t=2255) - Adding an entry into /etc/sudoers to allow us to escalate to root

-----------------------------------------------------------

ippsec: [HackTheBox - Chaos](https://youtube.com/watch?v=no9UnySBQrU)

0xdf: [HTB: Chaos](https://0xdf.gitlab.io//2019/05/25/htb-chaos.html)

[01:05](https://youtube.com/watch?v=no9UnySBQrU&t=65) - Begin of recon

[02:20](https://youtube.com/watch?v=no9UnySBQrU&t=140) - Starting up GoBuster then editing /etc/hosts to add the hosts in nmap

[03:20](https://youtube.com/watch?v=no9UnySBQrU&t=200) - Going over the website

[06:00](https://youtube.com/watch?v=no9UnySBQrU&t=360) - Discovering a wordpress instance (/wp/ form goBuster)

[09:50](https://youtube.com/watch?v=no9UnySBQrU&t=590) - Finding webmail credentials from a wordpress Protected Post

[10:30](https://youtube.com/watch?v=no9UnySBQrU&t=630) - Discovering webmail.chaos.htb (Method 1)

[12:50](https://youtube.com/watch?v=no9UnySBQrU&t=770) - Testing IMAP, then configuring Evolution to login to the mail server (Method 2)

[16:40](https://youtube.com/watch?v=no9UnySBQrU&t=1000) - Decrypting the message that was in the draft.

[22:55](https://youtube.com/watch?v=no9UnySBQrU&t=1375) - Message decrypted, new page discovered

[23:11](https://youtube.com/watch?v=no9UnySBQrU&t=1391) - Discovering a webpage for creating pdfs

[24:10](https://youtube.com/watch?v=no9UnySBQrU&t=1450) - Searching for a code injection path for LaTex

[24:45](https://youtube.com/watch?v=no9UnySBQrU&t=1485) - Discovering the blacklist is on "input"

[25:30](https://youtube.com/watch?v=no9UnySBQrU&t=1530) - Testing for blind command execution via ping

[27:43](https://youtube.com/watch?v=no9UnySBQrU&t=1663) - Reverse Shell Returned

[28:10](https://youtube.com/watch?v=no9UnySBQrU&t=1690) - Enumerating the web directory to find passwords

[29:11](https://youtube.com/watch?v=no9UnySBQrU&t=1751) - Switching to the "Ayush" user with mail password, discover we are in rBash

[29:45](https://youtube.com/watch?v=no9UnySBQrU&t=1785) - Escaping rBash by via tar (Method 1: GTFOBins)

[31:00](https://youtube.com/watch?v=no9UnySBQrU&t=1860) - Escaping rBash by editing path (Method 2)

[32:55](https://youtube.com/watch?v=no9UnySBQrU&t=1975) - Discovering a mozilla user configuration directory, copying it off to export passwords

[36:30](https://youtube.com/watch?v=no9UnySBQrU&t=2190) - Using firefox_decrypt to export root password

[37:30](https://youtube.com/watch?v=no9UnySBQrU&t=2250) - Logging into webmin with credentials from firefox

[37:50](https://youtube.com/watch?v=no9UnySBQrU&t=2270) - Privesc via switching to root user with known password (Method 1)

[38:10](https://youtube.com/watch?v=no9UnySBQrU&t=2290) - Using webmin to execute commands as root (Method 2)

-----------------------------------------------------------

ippsec: [HackTheBox - Bighead](https://youtube.com/watch?v=VBt-CmjMYiM)

0xdf: [HTB: BigHead](https://0xdf.gitlab.io//2019/05/04/htb-bighead.html)

[00:01:10](https://youtube.com/watch?v=VBt-CmjMYiM&t=70) - Begin of Nmap

[00:04:45](https://youtube.com/watch?v=VBt-CmjMYiM&t=285) - Pulling important information from the website

[00:06:00](https://youtube.com/watch?v=VBt-CmjMYiM&t=360) - Discovering DNS Names, adding stuff to /etc/hosts

[00:18:30](https://youtube.com/watch?v=VBt-CmjMYiM&t=1110) - Odd behavior with code.bighead.htb, redirects us to 127.0.0.1; change that with Burp

[00:23:50](https://youtube.com/watch?v=VBt-CmjMYiM&t=1430) - Using wfuzz to dirbust, with the ability to see HTTP Codes (hunting for 418)

[00:27:00](https://youtube.com/watch?v=VBt-CmjMYiM&t=1620) - Found BigHead Web Server on Github, pulling Zips and cracking

[00:36:40](https://youtube.com/watch?v=VBt-CmjMYiM&t=2200) - Before reversing the binary, keep hunting for information about the OS

[00:43:40](https://youtube.com/watch?v=VBt-CmjMYiM&t=2620) - Discovering PHPInfo within the PhpMyAdmin directory, has OS.

[00:46:00](https://youtube.com/watch?v=VBt-CmjMYiM&t=2760) - Installing Immunity and Mona

[00:47:30](https://youtube.com/watch?v=VBt-CmjMYiM&t=2850) - Grabbing MinGW so we can run the Bighead Webserver

[00:55:40](https://youtube.com/watch?v=VBt-CmjMYiM&t=3340) - Crashing the webserver, seeing we have

[01:00:00](https://youtube.com/watch?v=VBt-CmjMYiM&t=3600) - Sending a pattern to the box and examining the stack to see where our overwrites are

[01:06:15](https://youtube.com/watch?v=VBt-CmjMYiM&t=3975) - Validating we know where all our overwrites are (EAX,EBX,EIP,ESP)

[01:10:06](https://youtube.com/watch?v=VBt-CmjMYiM&t=4206) - Explanation of EggHunters

[01:16:05](https://youtube.com/watch?v=VBt-CmjMYiM&t=4565) - Grabbing the shellcode we want, then adding it to our exploit script

[01:24:50](https://youtube.com/watch?v=VBt-CmjMYiM&t=5090) - Validating our exploit is working as we intended by setting a break point on JMP ESP

[01:27:00](https://youtube.com/watch?v=VBt-CmjMYiM&t=5220) - Our box complains about DEP, lets disable that on our OS and hope its disabled on target

[01:30:00](https://youtube.com/watch?v=VBt-CmjMYiM&t=5400) - Running the exploit against the target and getting a shell back!

[01:35:00](https://youtube.com/watch?v=VBt-CmjMYiM&t=5700) - Searching the registry (HKLM) for "password"

[01:37:00](https://youtube.com/watch?v=VBt-CmjMYiM&t=5820) - Dumping information about services on the box (HKLM\System\CurrentControlSet\Services)

[01:38:15](https://youtube.com/watch?v=VBt-CmjMYiM&t=5895) - Discovery of NGINX password, then looking at ports listening on localhost

[01:41:08](https://youtube.com/watch?v=VBt-CmjMYiM&t=6068) - Found SSH Listening on 127.0.0.1:2020, Setting up a reverse tunnel with Chisel

[01:45:10](https://youtube.com/watch?v=VBt-CmjMYiM&t=6310) - SSH into nginx@Bighead over port 2020, land in an extremely restricted shell

[01:50:30](https://youtube.com/watch?v=VBt-CmjMYiM&t=6630) - Searching for vulnerable PHP Code, discovering testlink

[02:02:55](https://youtube.com/watch?v=VBt-CmjMYiM&t=7375) - Exploiting an LFI Vulnerability

[02:07:00](https://youtube.com/watch?v=VBt-CmjMYiM&t=7620) - Using Netcat to get a reverse shell

[02:16:10](https://youtube.com/watch?v=VBt-CmjMYiM&t=8170) - Looking at the KeePass Configuration File to see where the KDBX and Key is

[02:18:55](https://youtube.com/watch?v=VBt-CmjMYiM&t=8335) - A bunch of pain trying to get data off the Alternate Data Stream.

[02:31:30](https://youtube.com/watch?v=VBt-CmjMYiM&t=9090) - Finally got the KDBX back to my box, then crack the KeePass file

-----------------------------------------------------------

ippsec: [HackTheBox - Irked](https://youtube.com/watch?v=OGFTM_qvtVI)

0xdf: [HTB: Irked](https://0xdf.gitlab.io//2019/04/27/htb-irked.html)

[00:39](https://youtube.com/watch?v=OGFTM_qvtVI&t=39) - Begin on Recon

[01:39](https://youtube.com/watch?v=OGFTM_qvtVI&t=99) - Starting a full nmap scan 

[04:15](https://youtube.com/watch?v=OGFTM_qvtVI&t=255) - Discovery of IRC

[04:35](https://youtube.com/watch?v=OGFTM_qvtVI&t=275) - Manually looking at IRC

[06:00](https://youtube.com/watch?v=OGFTM_qvtVI&t=360) - Looking at the IRC to understand how to connect to an IRC Server

[07:00](https://youtube.com/watch?v=OGFTM_qvtVI&t=420) - Pulling the IRC Version and discovering the exploit

[08:50](https://youtube.com/watch?v=OGFTM_qvtVI&t=530) - Going into the history of the IRC Backdoor

[09:45](https://youtube.com/watch?v=OGFTM_qvtVI&t=585) - Manually exploiting the IRC Server

[13:10](https://youtube.com/watch?v=OGFTM_qvtVI&t=790) - Shell returned on the server

[14:30](https://youtube.com/watch?v=OGFTM_qvtVI&t=870) - Discovery of .backup which gives a steg password

[16:45](https://youtube.com/watch?v=OGFTM_qvtVI&t=1005) - Logging in with djmardov

[21:20](https://youtube.com/watch?v=OGFTM_qvtVI&t=1280) - Discovery of SetUID enabled custom binary, viewuser

[23:25](https://youtube.com/watch?v=OGFTM_qvtVI&t=1405) - Using ltrace to see what the binary does, executes the file /tmp/listusers

[23:50](https://youtube.com/watch?v=OGFTM_qvtVI&t=1430) - Getting a root shell

[25:50](https://youtube.com/watch?v=OGFTM_qvtVI&t=1550) - Testing exploiting the binary with "who", fails due to no setuid

[27:50](https://youtube.com/watch?v=OGFTM_qvtVI&t=1670) - Looking at the binary within Ghidra

-----------------------------------------------------------

ippsec: [HackTheBox - Teacher](https://youtube.com/watch?v=u2-te8n2WbY)

0xdf: [HTB: Teacher](https://0xdf.gitlab.io//2019/04/20/htb-teacher.html)

[00:40](https://youtube.com/watch?v=u2-te8n2WbY&t=40) - Begin of recon

[02:00](https://youtube.com/watch?v=u2-te8n2WbY&t=120) - Poking around at the website to identify what techologies it utilizes

[02:30](https://youtube.com/watch?v=u2-te8n2WbY&t=150) - Discovering something odd about images/5.png

[03:25](https://youtube.com/watch?v=u2-te8n2WbY&t=205) - Downloading 5.png to discover it is a text file with a portion of a password

[06:00](https://youtube.com/watch?v=u2-te8n2WbY&t=360) - Finding a place to login (/moodle), attempt to enumerate valid usernames

[08:00](https://youtube.com/watch?v=u2-te8n2WbY&t=480) - Using wfuzz to bruteforce the password

[11:20](https://youtube.com/watch?v=u2-te8n2WbY&t=680) - Looking for a way to enumerate Moodle Versions

[13:20](https://youtube.com/watch?v=u2-te8n2WbY&t=800) - Searching for exploits for this version and finding "Bad Teacher"

[14:40](https://youtube.com/watch?v=u2-te8n2WbY&t=880) - Start of manually exploiting this vulnerability

[16:00](https://youtube.com/watch?v=u2-te8n2WbY&t=960) - Adding a "Calculated Question" which has the formula (vulnerable) parameter

[20:16](https://youtube.com/watch?v=u2-te8n2WbY&t=1216) - Finding artifacts of creating/testing the machine which spoils what we are supposed to do

[24:21](https://youtube.com/watch?v=u2-te8n2WbY&t=1461) - Fixing our forumla to allow for code execution

[28:30](https://youtube.com/watch?v=u2-te8n2WbY&t=1710) - Getting a reverse shell

[30:00](https://youtube.com/watch?v=u2-te8n2WbY&t=1800) - Looking around the MySQL Database to discover hashes of other users

[31:52](https://youtube.com/watch?v=u2-te8n2WbY&t=1912) - The account Giovannibak stands out due to the hash being just MD5

[32:30](https://youtube.com/watch?v=u2-te8n2WbY&t=1950) - Attempting the password (expelled) of the MD5 hash above to login to "Su" to Giovannibak

[36:20](https://youtube.com/watch?v=u2-te8n2WbY&t=2180) - Grabbing and compiling pspy to find a cronjob

[38:30](https://youtube.com/watch?v=u2-te8n2WbY&t=2310) - Running PSPY to discover /usr/bin/backup.sh

[40:00](https://youtube.com/watch?v=u2-te8n2WbY&t=2400) - Abusing the backup cron to have it chmod 777 /etc/shadow (could do anything, sudoers is a bit less noisy)

-----------------------------------------------------------

ippsec: [HackTheBox - Redcross](https://youtube.com/watch?v=-GNyDEQ9UDU)

0xdf: [HTB: RedCross](https://0xdf.gitlab.io//2019/04/13/htb-redcross.html)

[00:20](https://youtube.com/watch?v=-GNyDEQ9UDU&t=20) - Flow chart of potential paths through this box

[02:25](https://youtube.com/watch?v=-GNyDEQ9UDU&t=145) - Begin of recon, SSL Enumeration, examining PHP Behavior

[06:23](https://youtube.com/watch?v=-GNyDEQ9UDU&t=383) - Using GoBuster to dicover directories, pdf's, and php scripts

[08:10](https://youtube.com/watch?v=-GNyDEQ9UDU&t=490) - Using wfuzz to discover subdomains (virtual host routing)

[12:15](https://youtube.com/watch?v=-GNyDEQ9UDU&t=735) - Guessing credential, logging in with guest:guest disover SQL Injection

[16:45](https://youtube.com/watch?v=-GNyDEQ9UDU&t=1005) - Manually doing an error-based SQL Injection with extractquery()

[31:50](https://youtube.com/watch?v=-GNyDEQ9UDU&t=1910) - A good screenshot showing the SQL Inject Queries used, then cracking

[35:00](https://youtube.com/watch?v=-GNyDEQ9UDU&t=2100) - Doing the SQLInjection with SQLMap, needed the delay flag!

[37:50](https://youtube.com/watch?v=-GNyDEQ9UDU&t=2270) - Examining the account-signup.pdf to create a user

[39:50](https://youtube.com/watch?v=-GNyDEQ9UDU&t=2390) - Doing XSS (cross site scripting) to steal a cookie of  the admin

[43:15](https://youtube.com/watch?v=-GNyDEQ9UDU&t=2595) - Going to admin.redcross.htb and showing that any way you got the PHPSESSID cookie would work

[46:15](https://youtube.com/watch?v=-GNyDEQ9UDU&t=2775) - Poking at admin.redcross.htb, creating a user that lands us in an SSH Jail

[48:38](https://youtube.com/watch?v=-GNyDEQ9UDU&t=2918) - Playing with the Firewall portion of the site, discover command injection in deleting rules!

[52:28](https://youtube.com/watch?v=-GNyDEQ9UDU&t=3148) - Reverse shell as www-data

[54:40](https://youtube.com/watch?v=-GNyDEQ9UDU&t=3280) - Discover postgresql credentials in actions.php, this database lets you create users!

-----------------------------------------------------------

ippsec: [HackTheBox - Vault](https://youtube.com/watch?v=LfbwlPxToBc)

0xdf: [HTB: Vault](https://0xdf.gitlab.io//2019/04/06/htb-vault.html)

[01:08](https://youtube.com/watch?v=LfbwlPxToBc&t=68) - Begin of Recon

[03:08](https://youtube.com/watch?v=LfbwlPxToBc&t=188) - Begin of GoBustering

[07:15](https://youtube.com/watch?v=LfbwlPxToBc&t=435) - Discovery of an image upload script

[08:39](https://youtube.com/watch?v=LfbwlPxToBc&t=519) - Attempting to bypass the upload filter

[12:46](https://youtube.com/watch?v=LfbwlPxToBc&t=766) - Reverse Shell to ubuntu Returned.  Examining Web Source

[15:28](https://youtube.com/watch?v=LfbwlPxToBc&t=928) - ALTERNATIVE: Checking out the host name pollution, setting host header to localhost

[19:27](https://youtube.com/watch?v=LfbwlPxToBc&t=1167) - Resume of poking around the host, discover passwords and other hosts in /home

[23:14](https://youtube.com/watch?v=LfbwlPxToBc&t=1394) - Uploading a static-compiled nmap to the box (static-binaries is a github repo)

[24:57](https://youtube.com/watch?v=LfbwlPxToBc&t=1497) - SSH Local Port Forward and Dynamic, to let our Kali box communicate with the next hop.

[27:27](https://youtube.com/watch?v=LfbwlPxToBc&t=1647) - Discovery of a page that lets us create ovpn (openvpn) configs and test the VPN

[28:45](https://youtube.com/watch?v=LfbwlPxToBc&t=1725) - Think i broke the box here, sent unicode to the box.... It stops responding on web.

[32:55](https://youtube.com/watch?v=LfbwlPxToBc&t=1975) - Machine reverted, getting back to where I started.

[34:50](https://youtube.com/watch?v=LfbwlPxToBc&t=2090) - Trying this again, and get a shell on ubuntu -- Lets do a Reverse Port Forward to get a shell on our kali box.

[36:12](https://youtube.com/watch?v=LfbwlPxToBc&t=2172) - Shell returned to Kali Box, explaining how to use socat if SSH Forward cannot listen on all ports.

[38:58](https://youtube.com/watch?v=LfbwlPxToBc&t=2338) - Exploring the DNS Server box.

[39:26](https://youtube.com/watch?v=LfbwlPxToBc&t=2366) - Finding a password in /home/dave/ssh

[40:15](https://youtube.com/watch?v=LfbwlPxToBc&t=2415) - Discovering Vault's IP Address in /etc/hosts

[41:20](https://youtube.com/watch?v=LfbwlPxToBc&t=2480) - Perfoming a NMAP on the vault box, discover two ports closed

[41:50](https://youtube.com/watch?v=LfbwlPxToBc&t=2510) - Doing a NMAP with the source port of one of the above ports to test for a lazy firewall, discover SSH on port 987

[43:20](https://youtube.com/watch?v=LfbwlPxToBc&t=2600) - ALTERNATIVE: Bypassing the firewall by using IPv6

[49:47](https://youtube.com/watch?v=LfbwlPxToBc&t=2987) - How to set the source port with SSH via ncat

[50:45](https://youtube.com/watch?v=LfbwlPxToBc&t=3045) - Discovering root.txt.gpg on Vault, it is encrypted with RSA Key D1EB1F03

[51:35](https://youtube.com/watch?v=LfbwlPxToBc&t=3095) - Dave has the above RSA Key, use SCP to send the file back to Ubuntu

[54:45](https://youtube.com/watch?v=LfbwlPxToBc&t=3285) - The file has been copied, using gpg to decrypt the file.

[55:39](https://youtube.com/watch?v=LfbwlPxToBc&t=3339) - MAJOR UNINTENDED WAY: Discovering SPICE ports are listening on localhost:5900-5903, this is like VNC

[57:05](https://youtube.com/watch?v=LfbwlPxToBc&t=3425) - Using Remote-Viewer to connect to the SPICE Port and getting physical access to the machine.

[57:42](https://youtube.com/watch?v=LfbwlPxToBc&t=3462) - Rebooting Vault by sending the Ctrl+Alt+delete key

[58:00](https://youtube.com/watch?v=LfbwlPxToBc&t=3480) - Editing grub to get a root shell without a password

[58:56](https://youtube.com/watch?v=LfbwlPxToBc&t=3536) - Changing the password to root, then rebooting again

[59:30](https://youtube.com/watch?v=LfbwlPxToBc&t=3570) - Logging in with the new password.

-----------------------------------------------------------

ippsec: [HackTheBox - Curling](https://youtube.com/watch?v=Paajc2Dupms)

0xdf: [HTB: Curling](https://0xdf.gitlab.io//2019/03/30/htb-curling.html)

[01:12](https://youtube.com/watch?v=Paajc2Dupms&t=72) - Begin of Recon

[01:55](https://youtube.com/watch?v=Paajc2Dupms&t=115) - Running Cewl to generate a wordlist

[02:50](https://youtube.com/watch?v=Paajc2Dupms&t=170) - Finding secret.txt in the HTML Source, which happens to be the password

[03:28](https://youtube.com/watch?v=Paajc2Dupms&t=208) - Runninh JoomScan so we have something running in the background

[04:20](https://youtube.com/watch?v=Paajc2Dupms&t=260) - Checking the manifest to get the Joomla Version

[06:20](https://youtube.com/watch?v=Paajc2Dupms&t=380) - Explaining what equals mean in base64

[07:50](https://youtube.com/watch?v=Paajc2Dupms&t=470) - Begin of hunting for Joomla Username

[08:30](https://youtube.com/watch?v=Paajc2Dupms&t=510) - BruteForcing Joomla Login with WFUZZ

[10:35](https://youtube.com/watch?v=Paajc2Dupms&t=635) - Troubleshooting by sending wfuzz through burp

[12:25](https://youtube.com/watch?v=Paajc2Dupms&t=745) - Turns out the CSRF Token is tied to cookie, adding that to the wfuzz command

[17:10](https://youtube.com/watch?v=Paajc2Dupms&t=1030) - Success! Logged into Joomla

[17:58](https://youtube.com/watch?v=Paajc2Dupms&t=1078) - Gaining code execution by modifying a template

[20:20](https://youtube.com/watch?v=Paajc2Dupms&t=1220) - Getting a reverse shell

[23:20](https://youtube.com/watch?v=Paajc2Dupms&t=1400) - Finding the file: password_backup which is encoded

[23:55](https://youtube.com/watch?v=Paajc2Dupms&t=1435) - Extracting password_backup manually with xxd, zcat, bzcat, tar

[25:43](https://youtube.com/watch?v=Paajc2Dupms&t=1543) - Extracting Password_Backup with CyberChef

[27:35](https://youtube.com/watch?v=Paajc2Dupms&t=1655) - Logging in with Floris

[28:17](https://youtube.com/watch?v=Paajc2Dupms&t=1697) - Looking at /home/floris/AdminArea

[28:50](https://youtube.com/watch?v=Paajc2Dupms&t=1730) - Testing the input file by changing the url to us

[29:30](https://youtube.com/watch?v=Paajc2Dupms&t=1770) - Getting LFI by using file:// within curl

[30:38](https://youtube.com/watch?v=Paajc2Dupms&t=1838) - Pulling the cron, to see what is going on

[31:25](https://youtube.com/watch?v=Paajc2Dupms&t=1885) - Cron shows curl -K to use curl with a config file, checking man page.

[32:05](https://youtube.com/watch?v=Paajc2Dupms&t=1925) - Changing where curl saves to, in order to gain a root shell

[33:45](https://youtube.com/watch?v=Paajc2Dupms&t=2025) - Showing another good file to read with the LFI (logs)

[34:18](https://youtube.com/watch?v=Paajc2Dupms&t=2058) - Using pspy to show when processes start/end, which shows the curl command with no exploits

-----------------------------------------------------------

ippsec: [HackTheBox - Frolic](https://youtube.com/watch?v=b6WGQSJu_zQ)

0xdf: [HTB: Frolic](https://0xdf.gitlab.io//2019/03/23/htb-frolic.html)

[01:16](https://youtube.com/watch?v=b6WGQSJu_zQ&t=76) - Begin of Recon, until around 13 minutes gathering information to avoid rabbit holes

[04:04](https://youtube.com/watch?v=b6WGQSJu_zQ&t=244) - Using nc/ncat to verify a port is open (-zv)

[11:17](https://youtube.com/watch?v=b6WGQSJu_zQ&t=677) - Doing gobuster across man of the sub directories

[13:03](https://youtube.com/watch?v=b6WGQSJu_zQ&t=783) - Examining /admin/ - Examine the HTML Source because login is not sending any data

[14:09](https://youtube.com/watch?v=b6WGQSJu_zQ&t=849) - Discover some weird text encoding (Ook), how I went about decoding it

[15:44](https://youtube.com/watch?v=b6WGQSJu_zQ&t=944) - Decoded to base64 with some spaces, clean up the base64 and are left with a zip file

[19:19](https://youtube.com/watch?v=b6WGQSJu_zQ&t=1159) - After cracking the zip, there is another text encoding challenge (BrainF*)

[25:11](https://youtube.com/watch?v=b6WGQSJu_zQ&t=1511) - With potential information, return to our long running recon for more information

[28:49](https://youtube.com/watch?v=b6WGQSJu_zQ&t=1729) - Discovering /playsms

[32:00](https://youtube.com/watch?v=b6WGQSJu_zQ&t=1920) - Reading ExploitDB Articles and then attempting to manuall exploit PlaySMS via uploading a CSV

[34:34](https://youtube.com/watch?v=b6WGQSJu_zQ&t=2074) - Getting a reverse shell

[39:00](https://youtube.com/watch?v=b6WGQSJu_zQ&t=2340) - Running LinEnum.sh

[40:00](https://youtube.com/watch?v=b6WGQSJu_zQ&t=2400) - Finding the SetUID file: rop

[42:00](https://youtube.com/watch?v=b6WGQSJu_zQ&t=2520) - Exploiting ROP Program with ret2libc

[45:30](https://youtube.com/watch?v=b6WGQSJu_zQ&t=2730) - Getting offsets of system, exit, /bin/sh from libc using ldd, readelf, and strings

[50:34](https://youtube.com/watch?v=b6WGQSJu_zQ&t=3034) - Running our exploit to get root shell

[54:00](https://youtube.com/watch?v=b6WGQSJu_zQ&t=3240) - Begin of recovering rop.c source code

[56:41](https://youtube.com/watch?v=b6WGQSJu_zQ&t=3401) - Recreating rop.c then compiling

[59:44](https://youtube.com/watch?v=b6WGQSJu_zQ&t=3584) - Copying the physical disk to our local box via SSH and DD

[01:01:44](https://youtube.com/watch?v=b6WGQSJu_zQ&t=3704) - Using PhotoRec to restore files and finding rop.c

-----------------------------------------------------------

ippsec: [HackTheBox - Carrier](https://youtube.com/watch?v=2ZxRA8BgmnA)

0xdf: [HTB: Carrier](https://0xdf.gitlab.io//2019/03/16/htb-carrier.html)

[00:53](https://youtube.com/watch?v=2ZxRA8BgmnA&t=53) - Begin of Recon

[03:30](https://youtube.com/watch?v=2ZxRA8BgmnA&t=210) - Checking out the Web Page

[04:20](https://youtube.com/watch?v=2ZxRA8BgmnA&t=260) - Doing UDP/GoBuster Scans

[08:20](https://youtube.com/watch?v=2ZxRA8BgmnA&t=500) - Running SNMPWalk and then logging into web interface

[10:20](https://youtube.com/watch?v=2ZxRA8BgmnA&t=620) - Reading the tickets on the web page

[12:00](https://youtube.com/watch?v=2ZxRA8BgmnA&t=720) - Discovering code execution

[16:00](https://youtube.com/watch?v=2ZxRA8BgmnA&t=960) - Reverse Shell Returned

[23:15](https://youtube.com/watch?v=2ZxRA8BgmnA&t=1395) - Discovering FTP Server 10.120.15.10

[26:00](https://youtube.com/watch?v=2ZxRA8BgmnA&t=1560) - Gaining access to a Router Interface

[27:30](https://youtube.com/watch?v=2ZxRA8BgmnA&t=1650) - Using Draw.io to draw out the network

[32:40](https://youtube.com/watch?v=2ZxRA8BgmnA&t=1960) - Examining routing information

[35:45](https://youtube.com/watch?v=2ZxRA8BgmnA&t=2145) - Looking at BGP Information

[39:00](https://youtube.com/watch?v=2ZxRA8BgmnA&t=2340) - First attempt at BGP Hijack, advertising a route

[43:30](https://youtube.com/watch?v=2ZxRA8BgmnA&t=2610) - Did not work, examining routing loop.

[50:50](https://youtube.com/watch?v=2ZxRA8BgmnA&t=3050) - Blocking the routing advertisement to AS300

[56:50](https://youtube.com/watch?v=2ZxRA8BgmnA&t=3410) - Showing the new routing loop (AS300 sends to AS200)

[01:00:00](https://youtube.com/watch?v=2ZxRA8BgmnA&t=3600) - Telling AS200 not to advertise the route to AS300

[01:04:00](https://youtube.com/watch?v=2ZxRA8BgmnA&t=3840) - Grabbing FTP Traffic to get root password

[01:07:00](https://youtube.com/watch?v=2ZxRA8BgmnA&t=4020) - Logging into all 3 routers for some fun

[01:08:50](https://youtube.com/watch?v=2ZxRA8BgmnA&t=4130) - Hiding from TraceRoute by mucking with TTL's

[01:13:20](https://youtube.com/watch?v=2ZxRA8BgmnA&t=4400) - Redoing the attack, but showing routing tables on all routers

[01:17:30](https://youtube.com/watch?v=2ZxRA8BgmnA&t=4650) - Unintended route, Just adding an IP to eth2

-----------------------------------------------------------

ippsec: [HackTheBox - Ethereal](https://youtube.com/watch?v=Bhh5yPHjwUY)

0xdf: [HTB: Ethereal](https://0xdf.gitlab.io//2019/03/09/htb-ethereal.html)

0xdf: [HTB: Ethereal Attacking Password Box](https://0xdf.gitlab.io//2019/03/09/htb-ethereal-pbox.html)

0xdf: [HTB: Ethereal Shell Development](https://0xdf.gitlab.io//2019/03/09/htb-ethereal-shell.html)

[00:50](https://youtube.com/watch?v=Bhh5yPHjwUY&t=50) - Begin of Recon, Downloading FTP and inspecting websites

[10:23](https://youtube.com/watch?v=Bhh5yPHjwUY&t=623) - Recap of what we saw on the recon. Limited pages that provide paths for exploitation, Server Hostname, and FTP

[11:30](https://youtube.com/watch?v=Bhh5yPHjwUY&t=690) - Sending MD5Hashes to VirusTotal to get file age

[15:45](https://youtube.com/watch?v=Bhh5yPHjwUY&t=945) - Downloading PasswordBox sourcecode to examine pbox.dat and discover a password manager.

[21:00](https://youtube.com/watch?v=Bhh5yPHjwUY&t=1260) - Use Hydra to try to bruteforce ethereal.htb:8080, find blind command injection in page by running various ping commands but no way to view output.

[25:45](https://youtube.com/watch?v=Bhh5yPHjwUY&t=1545) - Using nslookup to exfil the results of commands executed.

[33:15](https://youtube.com/watch?v=Bhh5yPHjwUY&t=1995) - Creating Python Script to automate exploitaiton of this program.  Using Scapy, BeutifulSoup, and Requests.

[55:23](https://youtube.com/watch?v=Bhh5yPHjwUY&t=3323) - Script working! Now to make the output a bit more pretty using tokens to sepereate spaces

[01:02:00](https://youtube.com/watch?v=Bhh5yPHjwUY&t=3720) - Running commands to get interesting information about the page

[01:05:20](https://youtube.com/watch?v=Bhh5yPHjwUY&t=3920) - Enumerating the Firewall via netsh

[01:09:10](https://youtube.com/watch?v=Bhh5yPHjwUY&t=4150) - Using OpenSSL to get a reverse shell on windows

[01:17:25](https://youtube.com/watch?v=Bhh5yPHjwUY&t=4645) - Reverse shell returned. 

[01:19:40](https://youtube.com/watch?v=Bhh5yPHjwUY&t=4780) - Creating a malicious shortcut via powershell

[01:22:40](https://youtube.com/watch?v=Bhh5yPHjwUY&t=4960) - Using OpenSSL To transfer files

[01:28:00](https://youtube.com/watch?v=Bhh5yPHjwUY&t=5280) - Getting reverse shell as Alan, then using OpenSSL to convert files to base64 to make exfil easier

[01:32:30](https://youtube.com/watch?v=Bhh5yPHjwUY&t=5550) - Creating and signing a malicious MSI with WiX.

[01:48:15](https://youtube.com/watch?v=Bhh5yPHjwUY&t=6495) - First attempt failed, creating a less complicated MSI File by just having it execute our shortcut

[01:53:00](https://youtube.com/watch?v=Bhh5yPHjwUY&t=6780) - Getting reverse shell as SYSTEM - Cannot read EFS Files

[01:55:20](https://youtube.com/watch?v=Bhh5yPHjwUY&t=6920) - Having our MSI not run as SYSTEM by changing impersonation in WiX

[01:58:30](https://youtube.com/watch?v=Bhh5yPHjwUY&t=7110) - Shell as Rupal returned.

-----------------------------------------------------------

ippsec: [HackTheBox - Access](https://youtube.com/watch?v=Rr6Oxrj2IjU)

0xdf: [HTB: Access](https://0xdf.gitlab.io//2019/03/02/htb-access.html)

[00:58](https://youtube.com/watch?v=Rr6Oxrj2IjU&t=58) - Begin of recon: ftp, telnet, IIS 7.5

[03:00](https://youtube.com/watch?v=Rr6Oxrj2IjU&t=180) - Downloading all files off an FTP Server with WGET

[05:30](https://youtube.com/watch?v=Rr6Oxrj2IjU&t=330) - Examining the "Access Control.zip" file.

[06:30](https://youtube.com/watch?v=Rr6Oxrj2IjU&t=390) - Cracking a zip file with John

[07:45](https://youtube.com/watch?v=Rr6Oxrj2IjU&t=465) - Creating a wordlist for cracking the zip (strings of the mdb file)

[10:00](https://youtube.com/watch?v=Rr6Oxrj2IjU&t=600) - Exploring the MDB Files (Access Database) with MDBTools (mdb-sql and mdb-tables)

[12:30](https://youtube.com/watch?v=Rr6Oxrj2IjU&t=750) - Grabbing the same password we cracked by checking the auth_user table

[13:35](https://youtube.com/watch?v=Rr6Oxrj2IjU&t=815) - Converting the PST File (Outlook Email) to PlainText via readpst

[15:00](https://youtube.com/watch?v=Rr6Oxrj2IjU&t=900) - Logging into telnet with the credentials from the email

[15:45](https://youtube.com/watch?v=Rr6Oxrj2IjU&t=945) - Switching to a Nishang Shell to execute powershell

[18:15](https://youtube.com/watch?v=Rr6Oxrj2IjU&t=1095) - Running JAWS (Just Another Windows Scanner)

[23:34](https://youtube.com/watch?v=Rr6Oxrj2IjU&t=1414) - Discovering Stored Credentials on the box for ACCESS\Administrator 

[25:11](https://youtube.com/watch?v=Rr6Oxrj2IjU&t=1511) - Examining the Shortcut on PUBLIC\DESKTOP which shows us how the "Stored Credential" is used.

[25:58](https://youtube.com/watch?v=Rr6Oxrj2IjU&t=1558) - Using powershell to view information of a Shortcut

[27:25](https://youtube.com/watch?v=Rr6Oxrj2IjU&t=1645) - Using the Stored Credential via runas /savecred

[30:31](https://youtube.com/watch?v=Rr6Oxrj2IjU&t=1831) - Creating Base64 (UTF-16LE) on linux to use in as a Powershell EncodedCommand

[31:54](https://youtube.com/watch?v=Rr6Oxrj2IjU&t=1914) - Box done, Administrator returned.

[32:38](https://youtube.com/watch?v=Rr6Oxrj2IjU&t=1958) - Begin of decrypting the Stored Credential, uploading Mimikatz

[33:40](https://youtube.com/watch?v=Rr6Oxrj2IjU&t=2020) - Using powershell to download files

[36:36](https://youtube.com/watch?v=Rr6Oxrj2IjU&t=2196) - Discovering that I was trying to save mimikatz to a directory i cannot write to :(

[37:15](https://youtube.com/watch?v=Rr6Oxrj2IjU&t=2235) - Testing Applocker methods to bypass the Software Restriction Policy (Give up on this one)

[38:50](https://youtube.com/watch?v=Rr6Oxrj2IjU&t=2330) - Trying to get Meterpreter shell via Unicorn (Fails, unknown reason)

[41:28](https://youtube.com/watch?v=Rr6Oxrj2IjU&t=2488) - Getting a Empire Agent running

[43:35](https://youtube.com/watch?v=Rr6Oxrj2IjU&t=2615) - Empire Agent Returned, Injecting meterpreter shellcode.

[45:46](https://youtube.com/watch?v=Rr6Oxrj2IjU&t=2746) - Attempting to use Mimikatz from within Meterpreter to decrypt dpapi::creds

[46:52](https://youtube.com/watch?v=Rr6Oxrj2IjU&t=2812) - Explaining Mimikatz Arguments when in "non-interactive" mode

[54:20](https://youtube.com/watch?v=Rr6Oxrj2IjU&t=3260) - Grabbing needed files to decrypt DPAPI::CREDS offline

[56:09](https://youtube.com/watch?v=Rr6Oxrj2IjU&t=3369) - Switing to Windows to run Mimikatz

[01:02:32](https://youtube.com/watch?v=Rr6Oxrj2IjU&t=3752) - Decrypting the Creds stored in DPAPI

-----------------------------------------------------------

ippsec: [HackTheBox - Zipper](https://youtube.com/watch?v=RLvFwiDK_F8)

0xdf: [HTB: Zipper](https://0xdf.gitlab.io//2019/02/23/htb-zipper.html)

[01:15](https://youtube.com/watch?v=RLvFwiDK_F8&t=75) - Start of NMAP

[04:10](https://youtube.com/watch?v=RLvFwiDK_F8&t=250) - Signing into Zabbix as Guest

[05:30](https://youtube.com/watch?v=RLvFwiDK_F8&t=330) - Getting potential usernames from inside Zabbix and guessing creds

[06:30](https://youtube.com/watch?v=RLvFwiDK_F8&t=390) - Running Searchsploit and looking for vulnerabilties

[07:20](https://youtube.com/watch?v=RLvFwiDK_F8&t=440) - Analyzing the "API" Script from SearchSploit as we have API Creds

[10:15](https://youtube.com/watch?v=RLvFwiDK_F8&t=615) - Modifying the "API" Script 

[11:15](https://youtube.com/watch?v=RLvFwiDK_F8&t=675) - Showing a shortcut to skip the Container to Host Lateral Movement.

[15:35](https://youtube.com/watch?v=RLvFwiDK_F8&t=935) - Shell on the Container.

[17:25](https://youtube.com/watch?v=RLvFwiDK_F8&t=1045) - Searching for Zabbix MySQL Password 

[18:35](https://youtube.com/watch?v=RLvFwiDK_F8&t=1115) - Dumping the Zabbix User Database

[20:00](https://youtube.com/watch?v=RLvFwiDK_F8&t=1200) - Logging into Zabbix as Admin, discover ZBX Agent on Host.  Testing if port is accessible

[23:30](https://youtube.com/watch?v=RLvFwiDK_F8&t=1410) - Running commands on the Zabbix Agent (Host OS) from Zabbix Server (Guest OS)

[29:53](https://youtube.com/watch?v=RLvFwiDK_F8&t=1793) - Getting a Reverse Shell on Zabbix (use nohup to fork)

[32:40](https://youtube.com/watch?v=RLvFwiDK_F8&t=1960) - Running LinEnum on Zabbix Host

[35:15](https://youtube.com/watch?v=RLvFwiDK_F8&t=2115) - Examining home directories to find Zapper Creds

[36:42](https://youtube.com/watch?v=RLvFwiDK_F8&t=2202) - Examining the "Zabbix-Service" SetUID 

[39:00](https://youtube.com/watch?v=RLvFwiDK_F8&t=2340) - PRIVESC #1: Running ltrace to discover it is vulnerable to $PATH Manipulation

[42:00](https://youtube.com/watch?v=RLvFwiDK_F8&t=2520) - PRIVESC #2: Weak permissions on Purge-Backups Service

[48:30](https://youtube.com/watch?v=RLvFwiDK_F8&t=2910) - Extra Content: Building a Zabbix API Client from Scratch!

[48:55](https://youtube.com/watch?v=RLvFwiDK_F8&t=2935) - "Pseudo Terminal" Skeleton Script via Cmd module

[50:00](https://youtube.com/watch?v=RLvFwiDK_F8&t=3000) - Adding Login Functionality

[56:08](https://youtube.com/watch?v=RLvFwiDK_F8&t=3368) - Making the script login upon starting

[57:50](https://youtube.com/watch?v=RLvFwiDK_F8&t=3470) - Adding functionality to dump users

[01:04:00](https://youtube.com/watch?v=RLvFwiDK_F8&t=3840) - Adding functionality to dump groups

[01:05:25](https://youtube.com/watch?v=RLvFwiDK_F8&t=3925) - Adding functionality to add users

[01:10:45](https://youtube.com/watch?v=RLvFwiDK_F8&t=4245) - Adding functionality to modify users

-----------------------------------------------------------

ippsec: [HackTheBox - Giddy](https://youtube.com/watch?v=J2unwbMQvUo)

0xdf: [HTB: Giddy](https://0xdf.gitlab.io//2019/02/16/htb-giddy.html)

[01:00](https://youtube.com/watch?v=J2unwbMQvUo&t=60) - Begin of intro

[02:17](https://youtube.com/watch?v=J2unwbMQvUo&t=137) - Examining port 80 and 443

[03:15](https://youtube.com/watch?v=J2unwbMQvUo&t=195) - Using gobuster to discover directories

[04:20](https://youtube.com/watch?v=J2unwbMQvUo&t=260) - /remote discovered, nothing to do here

[05:25](https://youtube.com/watch?v=J2unwbMQvUo&t=325) - /mvc discovered

[06:15](https://youtube.com/watch?v=J2unwbMQvUo&t=375) - SQL Injection everywhere

[09:15](https://youtube.com/watch?v=J2unwbMQvUo&t=555) - Attempt to perform union injection on search

[10:15](https://youtube.com/watch?v=J2unwbMQvUo&t=615) - Having trouble, send to SQLMap look at other places in the applicaiton

[12:20](https://youtube.com/watch?v=J2unwbMQvUo&t=740) - SQLMap having trouble with search SQL, change to ITEM

[16:50](https://youtube.com/watch?v=J2unwbMQvUo&t=1010) - Attempting XP_CMDSHELL (Fails)

[19:50](https://youtube.com/watch?v=J2unwbMQvUo&t=1190) - Using XP_DIRTREE to read files off SMBShare

[23:30](https://youtube.com/watch?v=J2unwbMQvUo&t=1410) - Use Responder to steal the authentication attempt of XP_DIRTREE

[25:00](https://youtube.com/watch?v=J2unwbMQvUo&t=1500) - Cracking the NetNTLMv2 Hash

[26:00](https://youtube.com/watch?v=J2unwbMQvUo&t=1560) - Logging into /remote with cracked credentials

[26:40](https://youtube.com/watch?v=J2unwbMQvUo&t=1600) - Discovering unifi video is installed, this has a known privesc

[29:30](https://youtube.com/watch?v=J2unwbMQvUo&t=1770) - Attempting to use Meterpreter. (Fail: AV)

[32:15](https://youtube.com/watch?v=J2unwbMQvUo&t=1935) - Grabbing and compiling a DotNet Reverse Shell

[35:15](https://youtube.com/watch?v=J2unwbMQvUo&t=2115) - Actually compiling the reverse shell

[38:58](https://youtube.com/watch?v=J2unwbMQvUo&t=2338) - Using xcopy to copy our reverse shell to the victim

[39:00](https://youtube.com/watch?v=J2unwbMQvUo&t=2340) - Attempting to find Unifi Service name so we can restart it. End up searching registry due to permission issues.

[42:10](https://youtube.com/watch?v=J2unwbMQvUo&t=2530) - Restarting Unifi Service so it executes TaskKill.exe

[44:25](https://youtube.com/watch?v=J2unwbMQvUo&t=2665) - Start of Bypassing AppLocker Bypass by copying executable into a directory under Windows

[45:50](https://youtube.com/watch?v=J2unwbMQvUo&t=2750) - Escaping powershell constrained mode with PSBypassCLM

60:25 - Showing the Powershell History file which contained a hint at Unifi

-----------------------------------------------------------

ippsec: [HackTheBox - Ypuffy](https://youtube.com/watch?v=UoB-J-eDvrg)

0xdf: [HTB: Ypuffy](https://0xdf.gitlab.io//2019/02/09/htb-ypuffy.html)

[01:30](https://youtube.com/watch?v=UoB-J-eDvrg&t=90) - Begin of Recon

[02:25](https://youtube.com/watch?v=UoB-J-eDvrg&t=145) - Enumerating OpenBSD Patch Date via SSH Version

[04:00](https://youtube.com/watch?v=UoB-J-eDvrg&t=240) - Examining port 80... Use Wireshark to see why NMAP gets a response but firefox does not

[06:30](https://youtube.com/watch?v=UoB-J-eDvrg&t=390) - Invalid Requests, will cause HTTP Service to send error message

[07:00](https://youtube.com/watch?v=UoB-J-eDvrg&t=420) - Using ldapsearch to enumerate ldap, use wireshark to see how the nmap script works

[21:30](https://youtube.com/watch?v=UoB-J-eDvrg&t=1290) - Using SMBMap to PassTheHash and enumerate fileshares and download Putty Key

[23:20](https://youtube.com/watch?v=UoB-J-eDvrg&t=1400) - Using PuttyGen to convert Putty Key to an RSA Key

[24:55](https://youtube.com/watch?v=UoB-J-eDvrg&t=1495) - Testing out ssh_enumusers to see if that would have worked to get valid usernames

[26:30](https://youtube.com/watch?v=UoB-J-eDvrg&t=1590) - Logged in as Alice, use LinEnum

[28:40](https://youtube.com/watch?v=UoB-J-eDvrg&t=1720) - Examining doas configuration (like Sudo -l)

[30:00](https://youtube.com/watch?v=UoB-J-eDvrg&t=1800) - Examining HTTPD Configuration to see why we couldn't hit the webserver earlier

[32:30](https://youtube.com/watch?v=UoB-J-eDvrg&t=1950) - Examining SSHD Configuration to see SSH is configured to allow CA Signed Keys

[34:40](https://youtube.com/watch?v=UoB-J-eDvrg&t=2080) - Getting hashes from SSH Keys to know what publics go to which privates

[37:00](https://youtube.com/watch?v=UoB-J-eDvrg&t=2220) - Playing with the SSHAUTH webservice to enumerate what principals go to which users

[41:45](https://youtube.com/watch?v=UoB-J-eDvrg&t=2505) - Signing a SSH Key using DoAs to sign a key with the root Principal

[45:30](https://youtube.com/watch?v=UoB-J-eDvrg&t=2730) - Testing the key, explaining how this all works

[47:30](https://youtube.com/watch?v=UoB-J-eDvrg&t=2850) - Unintended privesc, Xorg exploit

-----------------------------------------------------------

ippsec: [HackTheBox - Dab](https://youtube.com/watch?v=JvqBaZ0WnV4)

0xdf: [HTB: Dab](https://0xdf.gitlab.io//2019/02/02/htb-dab.html)

[00:40](https://youtube.com/watch?v=JvqBaZ0WnV4&t=40) - Begin of the box

[03:20](https://youtube.com/watch?v=JvqBaZ0WnV4&t=200) - Checking the HTTP Ports out

[04:38](https://youtube.com/watch?v=JvqBaZ0WnV4&t=278) - Using wfuzz to bruteforce a login on port 80

[08:15](https://youtube.com/watch?v=JvqBaZ0WnV4&t=495) - Begin examining port 8080, use wfuzz to bruteforce a cookie

[11:30](https://youtube.com/watch?v=JvqBaZ0WnV4&t=690) - Using wfuzz to enumerate the WAF and determine bad characters

[14:40](https://youtube.com/watch?v=JvqBaZ0WnV4&t=880) - Doing a SSRF Like attack with wfuzz and enumerating open ports on localhost.

[16:50](https://youtube.com/watch?v=JvqBaZ0WnV4&t=1010) - Begin examining port 11211 (MemCache)

[18:00](https://youtube.com/watch?v=JvqBaZ0WnV4&t=1080) - Dumping data from Memcache

[23:50](https://youtube.com/watch?v=JvqBaZ0WnV4&t=1430) - Using CVE-2018-15473 to enumerate valid users over SSH

[27:35](https://youtube.com/watch?v=JvqBaZ0WnV4&t=1655) - Cracking the users hash and logging into the box

[29:00](https://youtube.com/watch?v=JvqBaZ0WnV4&t=1740) - Using R2 to analyzing rabbit hole application "try_harder"

[33:30](https://youtube.com/watch?v=JvqBaZ0WnV4&t=2010) - Going through LinEnum

[38:30](https://youtube.com/watch?v=JvqBaZ0WnV4&t=2310) - Using r2 to examine myexec to find password

[40:13](https://youtube.com/watch?v=JvqBaZ0WnV4&t=2413) - Using r2 to examine libseclogin.so

[41:30](https://youtube.com/watch?v=JvqBaZ0WnV4&t=2490) - Examining ld.so.conf.d to identify if we can use ldconfig to hijack a library

[42:10](https://youtube.com/watch?v=JvqBaZ0WnV4&t=2530) - Creating a malicious library to hijack seclogin()

[45:10](https://youtube.com/watch?v=JvqBaZ0WnV4&t=2710) - Lets bypass the login by hijacking printf()

-----------------------------------------------------------

ippsec: [HackTheBox - Reddish](https://youtube.com/watch?v=Yp4oxoQIBAM)

0xdf: [HTB: Reddish](https://0xdf.gitlab.io//2019/01/26/htb-reddish.html)

[00:55](https://youtube.com/watch?v=Yp4oxoQIBAM&t=55) - Begin of Recon (Port Scans)

[04:09](https://youtube.com/watch?v=Yp4oxoQIBAM&t=249) - Reverse Image Searching an favicon to get application used

[08:20](https://youtube.com/watch?v=Yp4oxoQIBAM&t=500) - NODE-RED: Reverse Shell Returned

[15:30](https://youtube.com/watch?v=Yp4oxoQIBAM&t=930) - NODE-RED: Running IP and Port Scans to identify lateral movement targets

[24:29](https://youtube.com/watch?v=Yp4oxoQIBAM&t=1469) - Downloading Chisel (Go Program for Tunnels).

[25:00](https://youtube.com/watch?v=Yp4oxoQIBAM&t=1500) - Shrinking Go Programs by using ldflags and upx packing from 10Mb to 3Mb!

[27:00](https://youtube.com/watch?v=Yp4oxoQIBAM&t=1620) - PowerPoint: Explaining Reverse Pivot Tunnel using Chisel

[31:25](https://youtube.com/watch?v=Yp4oxoQIBAM&t=1885) - WWW: Tunnel online, examining the website

[34:23](https://youtube.com/watch?v=Yp4oxoQIBAM&t=2063) - Full Port Scan to 172.19.0.2, discover REDIS

[36:30](https://youtube.com/watch?v=Yp4oxoQIBAM&t=2190) - Searching for ways to execute code against REDIS

[38:07](https://youtube.com/watch?v=Yp4oxoQIBAM&t=2287) - Using REDIS to create a PHP Shell

[41:06](https://youtube.com/watch?v=Yp4oxoQIBAM&t=2466) - PowerPoint: Explaining Local Pivot Tunnel using Chisel

[44:30](https://youtube.com/watch?v=Yp4oxoQIBAM&t=2670) - WWW: Reverse Shell Returned

[45:45](https://youtube.com/watch?v=Yp4oxoQIBAM&t=2745) - Notice wildcard used with RSYNC, go search GTFOBins

[51:32](https://youtube.com/watch?v=Yp4oxoQIBAM&t=3092) - Abusing the wildcard within RSYNC

[57:23](https://youtube.com/watch?v=Yp4oxoQIBAM&t=3443) - WWW: Got Root, but no flag... Lets go look at RSYNC again.

[01:00:15](https://youtube.com/watch?v=Yp4oxoQIBAM&t=3615) - Explaining how to tunnel from Backup - WWW - NODE-RED - Kali

[01:17:50](https://youtube.com/watch?v=Yp4oxoQIBAM&t=4670) - Getting reverse shell on BACKUP via uploading CronJob through rsync

[01:20:30](https://youtube.com/watch?v=Yp4oxoQIBAM&t=4830) - BACKUP: Reverse Shell Returned... No root.txt here either!?

[01:26:30](https://youtube.com/watch?v=Yp4oxoQIBAM&t=5190) - BACKUP: Noticing this is has /dev/sda*, where other dockers do not

[01:28:15](https://youtube.com/watch?v=Yp4oxoQIBAM&t=5295) - BACKUP: Dropping a cronjob on root disk to get shell on the host

[01:30:45](https://youtube.com/watch?v=Yp4oxoQIBAM&t=5445) - ExtraContent: PowerPoint Reverse SOCKS5 Proxy with Chisel

-----------------------------------------------------------

ippsec: [HackTheBox - SecNotes](https://youtube.com/watch?v=PJXb2pK8K84)

0xdf: [HTB: SecNotes](https://0xdf.gitlab.io//2019/01/19/htb-secnotes.html)

[01:05](https://youtube.com/watch?v=PJXb2pK8K84&t=65) - Begin of recon

[02:45](https://youtube.com/watch?v=PJXb2pK8K84&t=165) - Checking out the website

[03:50](https://youtube.com/watch?v=PJXb2pK8K84&t=230) - Using wfuzz to enumerate usernames

[05:45](https://youtube.com/watch?v=PJXb2pK8K84&t=345) - Logging in with an account we created

[07:23](https://youtube.com/watch?v=PJXb2pK8K84&t=443) - Checking out Change Password and noticing it does this poorly

[09:25](https://youtube.com/watch?v=PJXb2pK8K84&t=565) - Using the contact form, to see if tyler will follow links

[14:14](https://youtube.com/watch?v=PJXb2pK8K84&t=854) - Changing Tyler's password by sending him to the ChangePassword Page

[15:00](https://youtube.com/watch?v=PJXb2pK8K84&t=900) - Logged in and find SMB Share with credentials.

[16:15](https://youtube.com/watch?v=PJXb2pK8K84&t=975) - Found a webshare but not sure the directory it executes from. Begin hunting for a different webserver.

[17:48](https://youtube.com/watch?v=PJXb2pK8K84&t=1068) - Port 8808 found via nmap'ing all ports.  Creating a php script to gain code execution

[19:15](https://youtube.com/watch?v=PJXb2pK8K84&t=1155) - Downloading netcat for windows to use as a Reverse Shell

[21:14](https://youtube.com/watch?v=PJXb2pK8K84&t=1274) - Playing with Bash on Windows

[22:35](https://youtube.com/watch?v=PJXb2pK8K84&t=1355) - Finding the administrator password in ~/.bash_history

[23:45](https://youtube.com/watch?v=PJXb2pK8K84&t=1425) - Alternate way to find the .bash_history file

[25:36](https://youtube.com/watch?v=PJXb2pK8K84&t=1536) - Unintended way to bypass the CSRF. SQL Injection + bad Static Code analysis

-----------------------------------------------------------

ippsec: [HackTheBox - Oz](https://youtube.com/watch?v=yX00n1UmalE)

0xdf: [HTB: Oz](https://0xdf.gitlab.io//2019/01/12/htb-oz.html)

[00:50](https://youtube.com/watch?v=yX00n1UmalE&t=50) - Start of the box

[05:30](https://youtube.com/watch?v=yX00n1UmalE&t=330) - Attempting GoBuster but wildcard response gives issue

[07:40](https://youtube.com/watch?v=yX00n1UmalE&t=460) - Start of doing wfuzz to find content

[10:38](https://youtube.com/watch?v=yX00n1UmalE&t=638) - Manually testing SQLInjection

[13:07](https://youtube.com/watch?v=yX00n1UmalE&t=787) - Running SQLMap and telling it exactly where the injection is

[16:04](https://youtube.com/watch?v=yX00n1UmalE&t=964) - Manually extracting files with the SQL Injection

[19:50](https://youtube.com/watch?v=yX00n1UmalE&t=1190) - Cracking the hash with hashcat

[25:00](https://youtube.com/watch?v=yX00n1UmalE&t=1500) - Start of examining the custom webapp, playing with Template Injection

[27:00](https://youtube.com/watch?v=yX00n1UmalE&t=1620) - Explaining a way to enumerate language behind a webapp

[35:17](https://youtube.com/watch?v=yX00n1UmalE&t=2117) - Reverse Shell returned on first Docker Container

[38:00](https://youtube.com/watch?v=yX00n1UmalE&t=2280) - Examining SQL Database

[39:40](https://youtube.com/watch?v=yX00n1UmalE&t=2380) - Doing the Port Knock to open up SSH

[43:50](https://youtube.com/watch?v=yX00n1UmalE&t=2630) - Gain a foothold on the host of the docker container via ssh

[46:00](https://youtube.com/watch?v=yX00n1UmalE&t=2760) - Identifying containers running

[50:10](https://youtube.com/watch?v=yX00n1UmalE&t=3010) - Creating SSH Port Forwards without exiting SSH Session then NMAP through

[55:11](https://youtube.com/watch?v=yX00n1UmalE&t=3311) - Begin looking into Portainer, finding a weak API Endpoint

[59:00](https://youtube.com/watch?v=yX00n1UmalE&t=3540) - Start of creating a container in portainer that can access the root file

[01:08:25](https://youtube.com/watch?v=yX00n1UmalE&t=4105) - Changing sudoers so dorthy can privesc to root

[01:09:50](https://youtube.com/watch?v=yX00n1UmalE&t=4190) - Lets go back and create a python script to play with SQL Injection

-----------------------------------------------------------

ippsec: [HackTheBox - Mischief](https://youtube.com/watch?v=GKo6xoB1g4Q)

0xdf: [HTB: Mischief Additional Roots](https://0xdf.gitlab.io//2019/01/08/htb-mischief-more-root.html)

0xdf: [HTB: Mischief](https://0xdf.gitlab.io//2019/01/05/htb-mischief.html)

[01:20](https://youtube.com/watch?v=GKo6xoB1g4Q&t=80) - Begin of NMAP

[02:30](https://youtube.com/watch?v=GKo6xoB1g4Q&t=150) - Extra nmaps, SNMP and AllPorts

[04:00](https://youtube.com/watch?v=GKo6xoB1g4Q&t=240) - Playing with OneSixtyOne (SNMP BruteForce)

[07:00](https://youtube.com/watch?v=GKo6xoB1g4Q&t=420) - Looking at SNMPWalk Output

[08:40](https://youtube.com/watch?v=GKo6xoB1g4Q&t=520) - Installing SNMP Mibs so SMPWalk is readable

[10:05](https://youtube.com/watch?v=GKo6xoB1g4Q&t=605) - Accessing the box over Link Local IPv6 Address

[14:00](https://youtube.com/watch?v=GKo6xoB1g4Q&t=840) - Looking at Por 3366 (Website), getting PW from SNMP Info

[17:50](https://youtube.com/watch?v=GKo6xoB1g4Q&t=1070) - Getting IPv6 Routable Address via SNMP

[19:20](https://youtube.com/watch?v=GKo6xoB1g4Q&t=1160) - NMAP the IPv6 Address

[21:00](https://youtube.com/watch?v=GKo6xoB1g4Q&t=1260) - Accessing the page over IPv6

[23:00](https://youtube.com/watch?v=GKo6xoB1g4Q&t=1380) - Getting output from the command execution page

[24:55](https://youtube.com/watch?v=GKo6xoB1g4Q&t=1495) - Viewing Credentials Files and accessing the box via SSH

[29:00](https://youtube.com/watch?v=GKo6xoB1g4Q&t=1740) - Examining why loki cannot use /bin/su (getfacl)

[31:00](https://youtube.com/watch?v=GKo6xoB1g4Q&t=1860) - Getting a shell as www-data

[40:30](https://youtube.com/watch?v=GKo6xoB1g4Q&t=2430) - Extra content, reading files via ICMP

-----------------------------------------------------------

ippsec: [HackTheBox - Waldo](https://youtube.com/watch?v=1klneIHECqY)

0xdf: [HTB: Waldo](https://0xdf.gitlab.io//2018/12/15/htb-waldo.html)

[01:15](https://youtube.com/watch?v=1klneIHECqY&t=75) - Begin of Recon

[02:00](https://youtube.com/watch?v=1klneIHECqY&t=120) - Looking at what Filtered means in Nmap

[05:00](https://youtube.com/watch?v=1klneIHECqY&t=300) - Start of looking at webpage (GoBuster)

[06:30](https://youtube.com/watch?v=1klneIHECqY&t=390) - Manual HTTP Enumeration

[09:50](https://youtube.com/watch?v=1klneIHECqY&t=590) - Start of exploiting with BurpSuite

[17:00](https://youtube.com/watch?v=1klneIHECqY&t=1020) - SSH Key Found, logging in with nobody

[19:12](https://youtube.com/watch?v=1klneIHECqY&t=1152) - Discovering a second SSH Server

[23:36](https://youtube.com/watch?v=1klneIHECqY&t=1416) - Using the same SSH Key to login to the second SSH Server as monitor

[24:38](https://youtube.com/watch?v=1klneIHECqY&t=1478) - Escaping rBash by modifying an executable file in our current $PATH

[28:13](https://youtube.com/watch?v=1klneIHECqY&t=1693) - Running LinEnum.sh to search for PrivEscs

[30:50](https://youtube.com/watch?v=1klneIHECqY&t=1850) - Enabling ThoroughTests in LinEnum to see what else it will check

[36:30](https://youtube.com/watch?v=1klneIHECqY&t=2190) - Looking into capabilities permission sin linux

[39:00](https://youtube.com/watch?v=1klneIHECqY&t=2340) - Begin of second way to escape rBash and setup a SSH Tunnel for fun

-----------------------------------------------------------

ippsec: [HackTheBox - Active](https://youtube.com/watch?v=jUc1J31DNdw)

0xdf: [HTB: Active](https://0xdf.gitlab.io//2018/12/08/htb-active.html)

[01:10](https://youtube.com/watch?v=jUc1J31DNdw&t=70) - Begin of recon 

[03:00](https://youtube.com/watch?v=jUc1J31DNdw&t=180) - Poking at DNS - Nothing really important.

[04:00](https://youtube.com/watch?v=jUc1J31DNdw&t=240) - Examining what NMAP Scripts are ran. 

[06:35](https://youtube.com/watch?v=jUc1J31DNdw&t=395) - Lets just try out smbclient to list shares available

[07:25](https://youtube.com/watch?v=jUc1J31DNdw&t=445) - Using SMBMap to show the same thing, a great recon tool!

[08:30](https://youtube.com/watch?v=jUc1J31DNdw&t=510) - Pillaging the Replication Share with SMBMap

[09:20](https://youtube.com/watch?v=jUc1J31DNdw&t=560) - Discovering Groups.xml and then decrypting passwords from it

[13:10](https://youtube.com/watch?v=jUc1J31DNdw&t=790) - Dumping Active Directory users from linux with Impacket GetADUsers

[16:28](https://youtube.com/watch?v=jUc1J31DNdw&t=988) - Using SMBMap with our user credentials to look for more shares

[18:25](https://youtube.com/watch?v=jUc1J31DNdw&t=1105) - Switching to Windows to run BloodHound against the domain 

[26:00](https://youtube.com/watch?v=jUc1J31DNdw&t=1560) - Analyzing BloodHound Output to discover Kerberostable user

[27:25](https://youtube.com/watch?v=jUc1J31DNdw&t=1645) - Performing Kerberoast attack from linux with Impacket GetUsersSPNs

[29:00](https://youtube.com/watch?v=jUc1J31DNdw&t=1740) - Cracking tgs 23 with Hashcat

[30:00](https://youtube.com/watch?v=jUc1J31DNdw&t=1800) - Getting root on the box via PSEXEC

-----------------------------------------------------------

ippsec: [HackTheBox - Hawk](https://youtube.com/watch?v=UGd9JE1ZXUI)

0xdf: [HTB: Hawk](https://0xdf.gitlab.io//2018/11/30/htb-hawk.html)

[01:00](https://youtube.com/watch?v=UGd9JE1ZXUI&t=60) - Begin nmap, discover FTP, Drupal, H2, and its Ubuntu Beaver

[03:50](https://youtube.com/watch?v=UGd9JE1ZXUI&t=230) - Checking FTP Server for hidden files

[04:30](https://youtube.com/watch?v=UGd9JE1ZXUI&t=270) - Examining encrypted file, discovering encrypted with OpenSSL and likely a block cipher

[08:20](https://youtube.com/watch?v=UGd9JE1ZXUI&t=500) - Creating a bunch of files varying in length to narrow likely ciphers down.

[14:35](https://youtube.com/watch?v=UGd9JE1ZXUI&t=875) - Encrypting all of the above files and checking their file sizes

[22:45](https://youtube.com/watch?v=UGd9JE1ZXUI&t=1365) - Decrypting file, obtaining a password

[24:25](https://youtube.com/watch?v=UGd9JE1ZXUI&t=1465) - Begin looking at Drupal, running Droopescan

[25:12](https://youtube.com/watch?v=UGd9JE1ZXUI&t=1512) - Manually examining Drupal, finding a way to enumerate usernames

[25:50](https://youtube.com/watch?v=UGd9JE1ZXUI&t=1550) - Placing invalid emails in create account, is a semi-silent way to enumerate usernames

[28:15](https://youtube.com/watch?v=UGd9JE1ZXUI&t=1695) - Logging into Drupal with Admin.  

[29:25](https://youtube.com/watch?v=UGd9JE1ZXUI&t=1765) - Gaining code execution by enabling PHP Plugin, then previewing a page with php code

[32:30](https://youtube.com/watch?v=UGd9JE1ZXUI&t=1950) - Reverse Shell Returned

[33:25](https://youtube.com/watch?v=UGd9JE1ZXUI&t=2005) - Running LinEnum.sh - Discover H2 (Database) runs as root

[37:00](https://youtube.com/watch?v=UGd9JE1ZXUI&t=2220) - Hunting for passwords in Drupal Configuration

[39:25](https://youtube.com/watch?v=UGd9JE1ZXUI&t=2365) - Finding database connection settings.  SSHing with daniel and the database password (not needed)

[40:10](https://youtube.com/watch?v=UGd9JE1ZXUI&t=2410) - Doing Local (Daniel) and Reverse (www) SSH Tunnels.  To access services on Hawk’s Loopback.  Only need to do one of those, just showing its possible without daniel

[44:30](https://youtube.com/watch?v=UGd9JE1ZXUI&t=2670) - Accessing Hawk’s H2 Service (8082) via the loopback address

[50:00](https://youtube.com/watch?v=UGd9JE1ZXUI&t=3000) - Finding the H2 Database Code Execution through Alias Commands, then hunting for a way to login to H2 Console.

[51:45](https://youtube.com/watch?v=UGd9JE1ZXUI&t=3105) - Logging into H2 by using a non-existent database, then testing code execution

[52:50](https://youtube.com/watch?v=UGd9JE1ZXUI&t=3170) - Playing with an awesome Reverse Shell Generator (RSG), then accidentally breaking the service.

[59:50](https://youtube.com/watch?v=UGd9JE1ZXUI&t=3590) - Reverted box, cleaning up environment then getting reverse shell

[01:02:45](https://youtube.com/watch?v=UGd9JE1ZXUI&t=3765) - Discovering could have logged into the database with Drupal Database Creds.

-----------------------------------------------------------

ippsec: [HackTheBox - Jerry](https://youtube.com/watch?v=PJeBIey8gc4)

0xdf: [HTB: Jerry](https://0xdf.gitlab.io//2018/11/17/htb-jerry.html)

[00:45](https://youtube.com/watch?v=PJeBIey8gc4&t=45) - Introduction, nmap

[01:30](https://youtube.com/watch?v=PJeBIey8gc4&t=90) - Clicking around in Tomcat

[02:20](https://youtube.com/watch?v=PJeBIey8gc4&t=140) - Playing around with HTTP Authentication

[05:45](https://youtube.com/watch?v=PJeBIey8gc4&t=345) - Bruteforcing tomcat default creds with Hydra and seclists

[08:20](https://youtube.com/watch?v=PJeBIey8gc4&t=500) - Sending hydra through a proxy to examine what is happening

[12:50](https://youtube.com/watch?v=PJeBIey8gc4&t=770) - Logging into tomcat and using msfvenom + metasploit to upload a malicious war file

[22:42](https://youtube.com/watch?v=PJeBIey8gc4&t=1362) - Begin of doing this box without MSF

[23:45](https://youtube.com/watch?v=PJeBIey8gc4&t=1425) - Downloading a cmd jsp shell and making a malicious war file

[26:25](https://youtube.com/watch?v=PJeBIey8gc4&t=1585) - WebShell returned

[28:00](https://youtube.com/watch?v=PJeBIey8gc4&t=1680) - Begin of installing SilentTrinity

[30:55](https://youtube.com/watch?v=PJeBIey8gc4&t=1855) - SilentyTrinity Started, starting listener and generating a payload

[33:00](https://youtube.com/watch?v=PJeBIey8gc4&t=1980) - Pasting the payload into the webshell

[34:00](https://youtube.com/watch?v=PJeBIey8gc4&t=2040) - Debugging SSL Handshake errors

[37:00](https://youtube.com/watch?v=PJeBIey8gc4&t=2220) - Starting SilentTrinity back up, how to use modules

[39:10](https://youtube.com/watch?v=PJeBIey8gc4&t=2350) - Start of Execute-Assembly, compiling Watson

[43:10](https://youtube.com/watch?v=PJeBIey8gc4&t=2590) - Running Watson

[43:30](https://youtube.com/watch?v=PJeBIey8gc4&t=2610) - Start of Seatbelt and debugging why some dotNet code may not run (versioning issues)

-----------------------------------------------------------

ippsec: [HackTheBox - Reel](https://youtube.com/watch?v=ob9SgtFm6_g)

0xdf: [HTB: Reel](https://0xdf.gitlab.io//2018/11/10/htb-reel.html)

[00:42](https://youtube.com/watch?v=ob9SgtFm6_g&t=42) - Begin of Nmap

[04:23](https://youtube.com/watch?v=ob9SgtFm6_g&t=263) - Examining the anonymous FTP Directory and discovering email addresses in Meta Data

[06:50](https://youtube.com/watch?v=ob9SgtFm6_g&t=410) - Manually enumerating valid email addresses via SMTP

[10:50](https://youtube.com/watch?v=ob9SgtFm6_g&t=650) - Creating a "Canary Document" in Word to ping back to our server when a word document is opened

[13:14](https://youtube.com/watch?v=ob9SgtFm6_g&t=794) - Generating a malicious RTF Document (CVE-2017-0199)

[26:28](https://youtube.com/watch?v=ob9SgtFm6_g&t=1588) - Shell Returned.  Enumerating the AppLocker Policy

[32:53](https://youtube.com/watch?v=ob9SgtFm6_g&t=1973) - Decrypting a PowerShell Secure String to reveal Tom's Password, Testing access with SSH

[35:22](https://youtube.com/watch?v=ob9SgtFm6_g&t=2122) - Lets forget we had Tom and run Bloodhound from Nico!

[40:30](https://youtube.com/watch?v=ob9SgtFm6_g&t=2430) - First time opening BloodHound on this box.

[49:45](https://youtube.com/watch?v=ob9SgtFm6_g&t=2985) - Lets update Bloodhound, looks like some data is missing and there were errors when running it

[53:25](https://youtube.com/watch?v=ob9SgtFm6_g&t=3205) - Finding a path from Nico to BACKUP_ADMINS and explaining AD Security Objects (GenericWrite, WriteOwner,etc)

[58:23](https://youtube.com/watch?v=ob9SgtFm6_g&t=3503) - Taking Ownership over Herman then allowing Nico to change his password and examining bloodhound

[01:01:40](https://youtube.com/watch?v=ob9SgtFm6_g&t=3700) - Adding Herman to the Backup_Admins group

[01:04:30](https://youtube.com/watch?v=ob9SgtFm6_g&t=3870) - Finding the Administrator Password within backup scripts.

[01:07:00](https://youtube.com/watch?v=ob9SgtFm6_g&t=4020) - Attempting to run Watson (ends up not working)

[01:23:22](https://youtube.com/watch?v=ob9SgtFm6_g&t=5002) - Using Metasploit to do the box

[01:25:42](https://youtube.com/watch?v=ob9SgtFm6_g&t=5142) - Since Watson failed, lets just look at last patch times on the box to get an idea whats vulnerable.

[01:27:19](https://youtube.com/watch?v=ob9SgtFm6_g&t=5239) - Attempting to do the ALPC Exploit within Metasploit

[01:31:00](https://youtube.com/watch?v=ob9SgtFm6_g&t=5460) - That failed - Lets just prove the box is vulnerable, by overwriting a DLL

-----------------------------------------------------------

ippsec: [HackTheBox - DropZone](https://youtube.com/watch?v=QzP5nUEhZeg)

0xdf: [HTB: Dropzone](https://0xdf.gitlab.io//2018/11/03/htb-dropzone.html)

[01:00](https://youtube.com/watch?v=QzP5nUEhZeg&t=60) - Start of Recon

[02:15](https://youtube.com/watch?v=QzP5nUEhZeg&t=135) - TFTP Enumeration - Identifying configuration and OS information

[06:32](https://youtube.com/watch?v=QzP5nUEhZeg&t=392) - Finding a path to code execution

[07:17](https://youtube.com/watch?v=QzP5nUEhZeg&t=437) - Examining PSExec Metasploit Module

[08:55](https://youtube.com/watch?v=QzP5nUEhZeg&t=535) - Using irb within metasploit to print a powershell payload

[12:30](https://youtube.com/watch?v=QzP5nUEhZeg&t=750) - Examining PsExec()

[15:40](https://youtube.com/watch?v=QzP5nUEhZeg&t=940) - Examining native_upload

[18:10](https://youtube.com/watch?v=QzP5nUEhZeg&t=1090) - Examining mof_upload

[20:34](https://youtube.com/watch?v=QzP5nUEhZeg&t=1234) - Using irb within metasploit to print the MOF File

[22:35](https://youtube.com/watch?v=QzP5nUEhZeg&t=1355) - Quick explanation of MOF Files

[25:05](https://youtube.com/watch?v=QzP5nUEhZeg&t=1505) - Modifying the MOF to run NetCat

[27:30](https://youtube.com/watch?v=QzP5nUEhZeg&t=1650) - Uploading nc to the target

[28:50](https://youtube.com/watch?v=QzP5nUEhZeg&t=1730) - Uploading the malicious MOF File and getting a shell!

[29:50](https://youtube.com/watch?v=QzP5nUEhZeg&t=1790) - Using Streams to view Hidden text within ADS

[33:08](https://youtube.com/watch?v=QzP5nUEhZeg&t=1988) - Start of Bonus Content, finging a TFTP Exploit that uses MOF

[35:05](https://youtube.com/watch?v=QzP5nUEhZeg&t=2105) - Attempting to use distrinct_ftp_traversal against DropZone

[36:30](https://youtube.com/watch?v=QzP5nUEhZeg&t=2190) - Installing pry.byebug in order to allow us to drop to a debug console and step through metasploit modules

[40:50](https://youtube.com/watch?v=QzP5nUEhZeg&t=2450) - Testing out pry.byebug

[42:30](https://youtube.com/watch?v=QzP5nUEhZeg&t=2550) - Finding why the exploit module didn't work

[44:50](https://youtube.com/watch?v=QzP5nUEhZeg&t=2690) - Module still doesn't work, TFTP Stopping mid transfer

[49:30](https://youtube.com/watch?v=QzP5nUEhZeg&t=2970) - Whoops, changed the delay on the wrong timeout 

[51:00](https://youtube.com/watch?v=QzP5nUEhZeg&t=3060) - Meterpreter Shell returned, showing off the extended API and some WMI Commands.

-----------------------------------------------------------

ippsec: [HackTheBox - Bounty](https://youtube.com/watch?v=7ur4om1K98Y)

0xdf: [HTB: Bounty](https://0xdf.gitlab.io//2018/10/27/htb-bounty.html)

[00:38](https://youtube.com/watch?v=7ur4om1K98Y&t=38) - Begin of recon

[01:48](https://youtube.com/watch?v=7ur4om1K98Y&t=108) - Gobuster, using -x aspx to find aspx pages

[03:16](https://youtube.com/watch?v=7ur4om1K98Y&t=196) - Playing with a file upload form, seeing what can be uploaded

[05:15](https://youtube.com/watch?v=7ur4om1K98Y&t=315) - Using Burp Intruder to automate checking file extensions

[07:00](https://youtube.com/watch?v=7ur4om1K98Y&t=420) - Finding a way to execute code from file upload in ASPX (web.config)

[10:55](https://youtube.com/watch?v=7ur4om1K98Y&t=655) - Executing code via web.config file upload

[13:08](https://youtube.com/watch?v=7ur4om1K98Y&t=788) - Installing Merlin to be our C2

[15:25](https://youtube.com/watch?v=7ur4om1K98Y&t=925) - Compiling the Merlin Windows Agent

[18:37](https://youtube.com/watch?v=7ur4om1K98Y&t=1117) - Modifying web.config to upload and execute merlin

[21:14](https://youtube.com/watch?v=7ur4om1K98Y&t=1274) - Merlin Shell returned!

[24:18](https://youtube.com/watch?v=7ur4om1K98Y&t=1458) - Checking for SEImpersonatePrivilege Token then doing Juicy Potato

[27:44](https://youtube.com/watch?v=7ur4om1K98Y&t=1664) - Getting Admin via Juicy Potato

[29:44](https://youtube.com/watch?v=7ur4om1K98Y&t=1784) - Box completed

[30:00](https://youtube.com/watch?v=7ur4om1K98Y&t=1800) - Start of doing this box again, with Metasploit! Creating a payload with Unicorn

[33:00](https://youtube.com/watch?v=7ur4om1K98Y&t=1980) - Having troubles getting the server call back to us, trying Ping to see if the exploit is still working

[34:17](https://youtube.com/watch?v=7ur4om1K98Y&t=2057) - Reverted box.  Have to update our payload with some updated VIEWSTATE parameters

[36:45](https://youtube.com/watch?v=7ur4om1K98Y&t=2205) - Metasploit Session Returned!  Checking local_exploit_suggester

[40:01](https://youtube.com/watch?v=7ur4om1K98Y&t=2401) - Comparing local_exploit_suggester on x32 and x64 meterpreter sessions

[40:30](https://youtube.com/watch?v=7ur4om1K98Y&t=2430) - Getting Admin via MS10-092

[42:05](https://youtube.com/watch?v=7ur4om1K98Y&t=2525) - Attempting to pivot through the Firewall using Meterpreter and doing Eternal Blue! (Fails, think I screwed up listening host #PivotProblems)

[47:20](https://youtube.com/watch?v=7ur4om1K98Y&t=2840) - Creating a Python Script to find valid extensions that handles CSRF Checks if they had existed

-----------------------------------------------------------

ippsec: [HackTheBox - Tartarsauce](https://youtube.com/watch?v=9MeBiP637ZA)

0xdf: [HTB: TartarSauce](https://0xdf.gitlab.io//2018/10/20/htb-tartarsauce.html)

[01:10](https://youtube.com/watch?v=9MeBiP637ZA&t=70) - Begin of recon

[03:00](https://youtube.com/watch?v=9MeBiP637ZA&t=180) - Discovery of Wordpress and fixing broken links with burp

[06:50](https://youtube.com/watch?v=9MeBiP637ZA&t=410) - Start of WPScan

[07:14](https://youtube.com/watch?v=9MeBiP637ZA&t=434) - Start of poking at Monstra, (Rabbit Hole)

[13:05](https://youtube.com/watch?v=9MeBiP637ZA&t=785) - Back to looking at WPScan, Find Gwolle Plugin is vulnerable to RFI Exploits

[16:30](https://youtube.com/watch?v=9MeBiP637ZA&t=990) - Reverse shell returned as www-data

[18:08](https://youtube.com/watch?v=9MeBiP637ZA&t=1088) - Confirming monstra was read-only

[18:50](https://youtube.com/watch?v=9MeBiP637ZA&t=1130) - Running LinEnum.sh to see www-data can run tar via sudo

[20:30](https://youtube.com/watch?v=9MeBiP637ZA&t=1230) - Use GTFOBins to find a way to execute code with Tar

[22:00](https://youtube.com/watch?v=9MeBiP637ZA&t=1320) - Begin of Onuma user, use LinEnum again to see SystemD Timer of a custom script

[24:10](https://youtube.com/watch?v=9MeBiP637ZA&t=1450) - Examining backuperer script

[26:00](https://youtube.com/watch?v=9MeBiP637ZA&t=1560) - Hunting for vulnerabilities in Backuperer

[32:15](https://youtube.com/watch?v=9MeBiP637ZA&t=1935) - Playing with If/Then exit codes in Bash.  Tuns out exit(0/1) evaluate as True, 2 is false

[34:20](https://youtube.com/watch?v=9MeBiP637ZA&t=2060) - Begin of exploiting the backuperer service by exploiting intregrity check

[36:40](https://youtube.com/watch?v=9MeBiP637ZA&t=2200) - Creating our 32-bit setuid binary

[39:16](https://youtube.com/watch?v=9MeBiP637ZA&t=2356) - Replacing backup tar, with our malicious one.  (File Owner of Shell is wrong)

[40:54](https://youtube.com/watch?v=9MeBiP637ZA&t=2454) - Explaning file owners are embedded within Tar, creating tar on our local box so we can have the SetUID File owned by root

[42:30](https://youtube.com/watch?v=9MeBiP637ZA&t=2550) - Exploiting the Backuperer Service via SetUID!

[45:00](https://youtube.com/watch?v=9MeBiP637ZA&t=2700) - Unintended Exploit: Using SymLinks to read files via backuperer service

-----------------------------------------------------------

ippsec: [HackTheBox - DevOops](https://youtube.com/watch?v=tQ34Ntkr7H4)

0xdf: [HTB: DevOops](https://0xdf.gitlab.io//2018/10/13/htb-devoops.html)

[00:54](https://youtube.com/watch?v=tQ34Ntkr7H4&t=54) - Start of Recon

[03:10](https://youtube.com/watch?v=tQ34Ntkr7H4&t=190) - Start of GoBuster

[04:00](https://youtube.com/watch?v=tQ34Ntkr7H4&t=240) - Looking at /upload, testing with a normal XML File

[06:15](https://youtube.com/watch?v=tQ34Ntkr7H4&t=375) - Valid XML File created, begin of looking for XML Entity Injection XXE

[08:20](https://youtube.com/watch?v=tQ34Ntkr7H4&t=500) - XXE Returns a a local file off the server

[09:30](https://youtube.com/watch?v=tQ34Ntkr7H4&t=570) - Grabbing the source code to the webserver to find newpost function.

[11:35](https://youtube.com/watch?v=tQ34Ntkr7H4&t=695) - Discovery of vulnerability due to user data being passed to pickle

[12:44](https://youtube.com/watch?v=tQ34Ntkr7H4&t=764) - Creating the script to exploit pickle

[16:38](https://youtube.com/watch?v=tQ34Ntkr7H4&t=998) - Reverse shell returns!

[19:55](https://youtube.com/watch?v=tQ34Ntkr7H4&t=1195) - Poking around at Source Code

[20:15](https://youtube.com/watch?v=tQ34Ntkr7H4&t=1215) - Discover of an SSH Key within deployment stuff.

[21:15](https://youtube.com/watch?v=tQ34Ntkr7H4&t=1275) - Trying SSH Key for other users on the box to see if it is valid

[22:57](https://youtube.com/watch?v=tQ34Ntkr7H4&t=1377) - Hunting for git filers, the boxes name is "Gitter" and we have an SSH Key that goes nowhere.  

[23:00](https://youtube.com/watch?v=tQ34Ntkr7H4&t=1380) - Discovery ~roosa/work is the same as ~roosa/deploy but there's a .git repo in this one!

[23:45](https://youtube.com/watch?v=tQ34Ntkr7H4&t=1425) - Examining Git Log to see the SSH Key has changed!

[25:20](https://youtube.com/watch?v=tQ34Ntkr7H4&t=1520) - SSH'ing with the old key, to see it's root's key.

[25:58](https://youtube.com/watch?v=tQ34Ntkr7H4&t=1558) - The webserver could read Roosa's SSH Key.  Could bypass the entire pickle portion

[26:20](https://youtube.com/watch?v=tQ34Ntkr7H4&t=1580) - Start of "Extra Practice"

[27:40](https://youtube.com/watch?v=tQ34Ntkr7H4&t=1660) - Creating a Python Script to automate the LFI With XXE

[35:50](https://youtube.com/watch?v=tQ34Ntkr7H4&t=2150) - Script completed, lets improve it to try to download an exposed git repo

-----------------------------------------------------------

ippsec: [HackTheBox - Fighter](https://youtube.com/watch?v=CW4mI5BkP9E)



[00:00:55](https://youtube.com/watch?v=CW4mI5BkP9E&t=55) - Begin of Recon Nmap, Identify OS Version, Check out Page to find hostname is streetfighterclub.htb.

[00:02:53](https://youtube.com/watch?v=CW4mI5BkP9E&t=173) - Using GoBuster and WFUZZ to identify: members.streetfighterclub.htb and members.streetfighterclub.htb/old/login.asp

[00:08:45](https://youtube.com/watch?v=CW4mI5BkP9E&t=525) - Begin poking around the members.streetfighterclub.htb page - Find SQL Injection

[00:12:00](https://youtube.com/watch?v=CW4mI5BkP9E&t=720) - Boolean injection to force the query to return "valid login".  Play with logins to find it always returns to "Service not available"

[00:14:25](https://youtube.com/watch?v=CW4mI5BkP9E&t=865) - Testing Union Injections for easy exfil of data

[00:15:50](https://youtube.com/watch?v=CW4mI5BkP9E&t=950) - Examining Stacked Queries to make running our own SQL Statements easy.  Then bunch of injections to run Xp_CMDShell and get output.

[00:19:30](https://youtube.com/watch?v=CW4mI5BkP9E&t=1170) - Some valuable recon/information in debugging our SQL queries. Noticing small things really helps.

[00:34:40](https://youtube.com/watch?v=CW4mI5BkP9E&t=2080) - Start of making a program to give us a command shell.

[01:09:40](https://youtube.com/watch?v=CW4mI5BkP9E&t=4180) - Explaining the program we just created.  Then fix a small bug.

[01:12:45](https://youtube.com/watch?v=CW4mI5BkP9E&t=4365) - Begin of popping the box the intended way.  Finding powershell is blocked but specifying the 32-bit version is not

[01:17:10](https://youtube.com/watch?v=CW4mI5BkP9E&t=4630) - Return of 32-bit PowerShell... Identifying we can append data to c:\users\decoder\clean.bat -- That's odd lets try to place a shell in it to see if it is being ran.

[01:32:40](https://youtube.com/watch?v=CW4mI5BkP9E&t=5560) - Found the issue! Powershell is encoding in UTF-16 which is confusing cmd prompt.  64-bit Shell as Decoder returned!

[01:35:30](https://youtube.com/watch?v=CW4mI5BkP9E&t=5730) - Exploiting Capcom Driver to gain root shell, this post is super helpful: http://www.fuzzysecurity.com/tutorials/28.html

[01:42:18](https://youtube.com/watch?v=CW4mI5BkP9E&t=6138) - Escalating to System via Capcom Exploit, then copying root.exe and checkdll.dll to our box so we can reverse it.

[01:47:25](https://youtube.com/watch?v=CW4mI5BkP9E&t=6445) - Looking at the binaries in Ida64 Free

[01:51:14](https://youtube.com/watch?v=CW4mI5BkP9E&t=6674) - Explaining what's happening and then writing a script to bypass the password check.

[01:55:35](https://youtube.com/watch?v=CW4mI5BkP9E&t=6935) - Start of unintended way (Juicy Potato)

[01:58:10](https://youtube.com/watch?v=CW4mI5BkP9E&t=7090) - Finding a world write-able spot under System32 for AppLocker Bypass, thanks @Bufferov3rride -- Then uploading JuicyPotato

[02:06:10](https://youtube.com/watch?v=CW4mI5BkP9E&t=7570) - Start of modifying JuicyPotato to accept uppercase arguments.

[02:10:14](https://youtube.com/watch?v=CW4mI5BkP9E&t=7814) - Finding a vulnerable CLSID to get JuicyPotato working

[02:28:25](https://youtube.com/watch?v=CW4mI5BkP9E&t=8905) - Running JuicyPotato with a vulnerable CLSID to gain a SYSTEM Shell, then create our own DLL to bypass the check.

-----------------------------------------------------------

ippsec: [HackTheBox - Sunday](https://youtube.com/watch?v=xUrq29OTSuM)

0xdf: [HTB: Sunday](https://0xdf.gitlab.io//2018/09/29/htb-sunday.html)

[00:48](https://youtube.com/watch?v=xUrq29OTSuM&t=48) - Begin of NMAP Discovery of Finger

[03:36](https://youtube.com/watch?v=xUrq29OTSuM&t=216) - Enumerating Finger with Finger-User-Enum

[05:00](https://youtube.com/watch?v=xUrq29OTSuM&t=300) - Nmap'ing all port quickly by lowering max-retries

[08:40](https://youtube.com/watch?v=xUrq29OTSuM&t=520) - Adding an old Key Exchange Alogorithm to SSH

[09:30](https://youtube.com/watch?v=xUrq29OTSuM&t=570) - Showing Hydra doesn't work, then using Patator

[11:19](https://youtube.com/watch?v=xUrq29OTSuM&t=679) - Using find to count lines in all wordlist files

[14:07](https://youtube.com/watch?v=xUrq29OTSuM&t=847) - Logged in with sunny:sunday

[14:45](https://youtube.com/watch?v=xUrq29OTSuM&t=885) - Grabbing /backup/shadow.backup and cracking sha256crypt with Hashcat

[16:46](https://youtube.com/watch?v=xUrq29OTSuM&t=1006) - Just noticed this box is oooooold, try to privesc with sudo and ShellShock (Fail)

[18:53](https://youtube.com/watch?v=xUrq29OTSuM&t=1133) - Privesc by overwriting the /root/troll binary

[23:30](https://youtube.com/watch?v=xUrq29OTSuM&t=1410) - Using wget to exfil files quickly

[24:50](https://youtube.com/watch?v=xUrq29OTSuM&t=1490) - Viewing what wget --post-file looks like

[25:50](https://youtube.com/watch?v=xUrq29OTSuM&t=1550) - Creating a PHP Script to accept uploaded files

[27:30](https://youtube.com/watch?v=xUrq29OTSuM&t=1650) - Hardening our upload location to prevent executing PHP Files and/or reading what was uploaded

[29:10](https://youtube.com/watch?v=xUrq29OTSuM&t=1750) - Starting a php webserver with php -S (ip):(port) -t .

[31:10](https://youtube.com/watch?v=xUrq29OTSuM&t=1870) - Replacing the root password by changing the shadow file

[33:30](https://youtube.com/watch?v=xUrq29OTSuM&t=2010) - Demoing a way to create directories and upload files!

-----------------------------------------------------------

ippsec: [HackTheBox - Olympus](https://youtube.com/watch?v=7ifJOon5-G8)

0xdf: [HTB: Olympus](https://0xdf.gitlab.io//2018/09/22/htb-olympus.html)

[01:30](https://youtube.com/watch?v=7ifJOon5-G8&t=90) - Begin of Recon, nmap filtered explanation

[03:30](https://youtube.com/watch?v=7ifJOon5-G8&t=210) - Begin of initial DNSRecon, hunting for a domain name

[06:04](https://youtube.com/watch?v=7ifJOon5-G8&t=364) - Web page enumeration, finding xdebug in header

[09:47](https://youtube.com/watch?v=7ifJOon5-G8&t=587) - Installing xdebug plugin in Chrome to show its use

[12:50](https://youtube.com/watch?v=7ifJOon5-G8&t=770) - Getting a reverse shell on the first docker (Icarus)

[15:00](https://youtube.com/watch?v=7ifJOon5-G8&t=900) - Setting up nginx to accept files uploaded over HTTP / WebDav

[20:30](https://youtube.com/watch?v=7ifJOon5-G8&t=1230) - Examining the Wireless Capture from Icarus

[21:30](https://youtube.com/watch?v=7ifJOon5-G8&t=1290) - Cracking WPA with aircrack / hashcat

[25:00](https://youtube.com/watch?v=7ifJOon5-G8&t=1500) - Decrypting WPA traffic in Wireshark

[27:50](https://youtube.com/watch?v=7ifJOon5-G8&t=1670) - Enumerating valid usernames via SSH (CVE-2018-15473)

[33:15](https://youtube.com/watch?v=7ifJOon5-G8&t=1995) - SSH into port 2222 with information from Wireless Capture

[34:40](https://youtube.com/watch?v=7ifJOon5-G8&t=2080) - Domain Name found!  Time to do a DNS Zone Transfer

[36:15](https://youtube.com/watch?v=7ifJOon5-G8&t=2175) - Port Knocking to open up port 22

[40:05](https://youtube.com/watch?v=7ifJOon5-G8&t=2405) - PrivEsc to root via being a member of the Docker Group

-----------------------------------------------------------

ippsec: [HackTheBox - Canape](https://youtube.com/watch?v=rs75y2qPonc)

0xdf: [HTB: Canape](https://0xdf.gitlab.io//2018/09/15/htb-canape.html)

[00:43](https://youtube.com/watch?v=rs75y2qPonc&t=43) - Start of Recon, nmap and poking around the website

[04:00](https://youtube.com/watch?v=rs75y2qPonc&t=240) - Dirbusting a site that always respond 200

[09:43](https://youtube.com/watch?v=rs75y2qPonc&t=583) - Switching to a different Wordlist (SecLists/Discovery/Web/Common)

[10:48](https://youtube.com/watch?v=rs75y2qPonc&t=648) - Discovery of .git - Poking around to clone it and download

[15:10](https://youtube.com/watch?v=rs75y2qPonc&t=910) - Downloaded .git, examining commit history

[19:50](https://youtube.com/watch?v=rs75y2qPonc&t=1190) - Start of Pickle Talk

[21:25](https://youtube.com/watch?v=rs75y2qPonc&t=1285) - Begin writing of the pickle exploit

[28:45](https://youtube.com/watch?v=rs75y2qPonc&t=1725) - Return of Reverse Shell as www-data

[32:30](https://youtube.com/watch?v=rs75y2qPonc&t=1950) - Begin looking into CouchDB

[34:00](https://youtube.com/watch?v=rs75y2qPonc&t=2040) - Poking around at documents within CouchDB

[36:15](https://youtube.com/watch?v=rs75y2qPonc&t=2175) - Examining first exploit with creating a CouchDB User

[39:50](https://youtube.com/watch?v=rs75y2qPonc&t=2390) - Exploring the passwords database with our newly created admin user and finding Homers Password.

[42:00](https://youtube.com/watch?v=rs75y2qPonc&t=2520) - Getting root with sudo pip install

[45:55](https://youtube.com/watch?v=rs75y2qPonc&t=2755) - Box Done.  Begin second unintended way to get to Homer User

[47:03](https://youtube.com/watch?v=rs75y2qPonc&t=2823) - Playing with the public RCE Exploit for CouchDB 

[48:20](https://youtube.com/watch?v=rs75y2qPonc&t=2900) - Running the exploit

[49:36](https://youtube.com/watch?v=rs75y2qPonc&t=2976) - Examining the exploit, doing each step manually to see where it fails

[54:30](https://youtube.com/watch?v=rs75y2qPonc&t=3270) - Searching on how to create a new CouchDB Cluster, maybe it will allow this work?

[55:55](https://youtube.com/watch?v=rs75y2qPonc&t=3355) - Digging into how erlang works

[57:30](https://youtube.com/watch?v=rs75y2qPonc&t=3450) - Finding default CouchDB Cookie

[59:10](https://youtube.com/watch?v=rs75y2qPonc&t=3550) - Connecting to the Erlang pool then searching for how to run commands.

[01:01:54](https://youtube.com/watch?v=rs75y2qPonc&t=3714) - Exploring how to send long commands as distributed task

[01:04:30](https://youtube.com/watch?v=rs75y2qPonc&t=3870) - Getting reverse shell

-----------------------------------------------------------

ippsec: [HackTheBox - Poison](https://youtube.com/watch?v=rs4zEwONzzk)

0xdf: [HTB: Poison](https://0xdf.gitlab.io//2018/09/08/htb-poison.html)

[00:56](https://youtube.com/watch?v=rs4zEwONzzk&t=56) - Start of recon, use Bootstrap XSL Script to make nmap pretty

[03:10](https://youtube.com/watch?v=rs4zEwONzzk&t=190) - Looking at nmap in web browser 

[03:52](https://youtube.com/watch?v=rs4zEwONzzk&t=232) - Navigating to the web page, and testing all the pages.

[06:25](https://youtube.com/watch?v=rs4zEwONzzk&t=385) - Testing for LFI

[07:00](https://youtube.com/watch?v=rs4zEwONzzk&t=420) - Using PHP  Filters to view the contents of php file through LFI (Local File Inclusion)

[08:40](https://youtube.com/watch?v=rs4zEwONzzk&t=520) - Testing for RFI (Remote File Inclusion) [not vuln]

[10:00](https://youtube.com/watch?v=rs4zEwONzzk&t=600) - Code Execution via LFI + phpinfo()

[14:45](https://youtube.com/watch?v=rs4zEwONzzk&t=885) - Modifying the PHP-LFI Script code to get it working

[17:10](https://youtube.com/watch?v=rs4zEwONzzk&t=1030) - Debugging the script to see why tmp_name couldn't be found

[20:12](https://youtube.com/watch?v=rs4zEwONzzk&t=1212) - Shell returned!

[21:25](https://youtube.com/watch?v=rs4zEwONzzk&t=1285) - Looking at pwdbackup.txt and decoding 13 times to get password.

[23:37](https://youtube.com/watch?v=rs4zEwONzzk&t=1417) - SSH into the box (Do not privesc right away!)

[24:29](https://youtube.com/watch?v=rs4zEwONzzk&t=1469) - Getting shell via Log Poisoning

[26:39](https://youtube.com/watch?v=rs4zEwONzzk&t=1599) - Whoops.  Broke the exploit, because of bad PHP Code... We'll come back to this! (42:50)

[28:47](https://youtube.com/watch?v=rs4zEwONzzk&t=1727) - Begin of PrivEsc, grabbing secret.zip off

[32:38](https://youtube.com/watch?v=rs4zEwONzzk&t=1958) - Searching for processes running as root, find VNC

[33:49](https://youtube.com/watch?v=rs4zEwONzzk&t=2029) - Setting up SSH Tunnels without exiting SSH Session.

[37:43](https://youtube.com/watch?v=rs4zEwONzzk&t=2263) - Something weird happend... Setting up SSH Tunnels manually.

[40:10](https://youtube.com/watch?v=rs4zEwONzzk&t=2410) - PrivEsc: VNC through the SSH Tunnel, passing the encrypted VNC Password

[41:40](https://youtube.com/watch?v=rs4zEwONzzk&t=2500) - Decrypting the VNC Password because we can.

[42:50](https://youtube.com/watch?v=rs4zEwONzzk&t=2570) - Examining the log file to see why our Log Poison Failed, then doing the Log Poison

-----------------------------------------------------------

ippsec: [HackTheBox - Stratosphere](https://youtube.com/watch?v=uMwcJQcUnmY)

0xdf: [HTB: Stratosphere](https://0xdf.gitlab.io//2018/09/01/htb-stratosphere.html)

[01:11](https://youtube.com/watch?v=uMwcJQcUnmY&t=71) - Begin of recon

[03:48](https://youtube.com/watch?v=uMwcJQcUnmY&t=228) - Manually checking the page out

[04:30](https://youtube.com/watch?v=uMwcJQcUnmY&t=270) - Discovering the webserver is java/tomcact

[05:35](https://youtube.com/watch?v=uMwcJQcUnmY&t=335) - Starting up GoBuster / Hydra

[09:40](https://youtube.com/watch?v=uMwcJQcUnmY&t=580) - The Directory /Monitoring was found - Discovering its Struts because of .action

[11:00](https://youtube.com/watch?v=uMwcJQcUnmY&t=660) - Stumbling upon an exploit trying to find out how to enumerate Struts Versions

[14:10](https://youtube.com/watch?v=uMwcJQcUnmY&t=850) - Searching Github for CVE-2017-5638 exploit script, exploiting the box to find out its firewalled off

[21:10](https://youtube.com/watch?v=uMwcJQcUnmY&t=1270) - Using a HTTP Forward Shell to get around the strict firewall

[22:40](https://youtube.com/watch?v=uMwcJQcUnmY&t=1360) - Go here if you want to start copying the Forward Shell Script

[23:34](https://youtube.com/watch?v=uMwcJQcUnmY&t=1414) - Explaining how it works

[25:10](https://youtube.com/watch?v=uMwcJQcUnmY&t=1510) - Explaining the code

[31:06](https://youtube.com/watch?v=uMwcJQcUnmY&t=1866) - Forward Shell Returned - Enumerating Database to find creds

[37:29](https://youtube.com/watch?v=uMwcJQcUnmY&t=2249) - Examining User.py

[40:15](https://youtube.com/watch?v=uMwcJQcUnmY&t=2415) - Privesc: Abusing Python's Path to load a malicious library and sudo user.py

-----------------------------------------------------------

ippsec: [HackTheBox - Celestial](https://youtube.com/watch?v=aS6z4NgRysU)

0xdf: [HTB: Celestial](https://0xdf.gitlab.io//2018/08/25/htb-celestial.html)

[00:58](https://youtube.com/watch?v=aS6z4NgRysU&t=58) - Begin of Recon

[03:00](https://youtube.com/watch?v=aS6z4NgRysU&t=180) - Looking at the web application and finding the Serialized Cookie

[04:38](https://youtube.com/watch?v=aS6z4NgRysU&t=278) - Googling for Node JS Deserialization Exploits

[06:30](https://youtube.com/watch?v=aS6z4NgRysU&t=390) - Start of building our payload

[07:10](https://youtube.com/watch?v=aS6z4NgRysU&t=430) - Examining Node-Serialize to see what the heck _$$ND_FUNC$$_ is

[09:10](https://youtube.com/watch?v=aS6z4NgRysU&t=550) - Moving our serialized object to "Name", hoping to get to read stdout

[11:30](https://youtube.com/watch?v=aS6z4NgRysU&t=690) - Really busing the deserialize function by removing the Immediately Invokked Expression (IIFE)

[13:25](https://youtube.com/watch?v=aS6z4NgRysU&t=805) - Failing to convert an object (stdout) to string.

[14:02](https://youtube.com/watch?v=aS6z4NgRysU&t=842) - Verifying code execution via ping

[15:32](https://youtube.com/watch?v=aS6z4NgRysU&t=932) - Code execution verified, gaining a shell

[18:49](https://youtube.com/watch?v=aS6z4NgRysU&t=1129) - Reverse shell returned, running LinEnum.sh

[21:26](https://youtube.com/watch?v=aS6z4NgRysU&t=1286) - Examining logs to find the Cron Job running as root

[22:09](https://youtube.com/watch?v=aS6z4NgRysU&t=1329) - Privesc by placing a python root shell in script.py

[24:15](https://youtube.com/watch?v=aS6z4NgRysU&t=1455) - Going back and getting a shell with NodeJSShell

-----------------------------------------------------------

ippsec: [HackTheBox - Rabbit](https://youtube.com/watch?v=5nnJq_IWJog)



[01:40](https://youtube.com/watch?v=5nnJq_IWJog&t=100) - Begin of Recon (nmap, setting hostname, dns, nmap, ipv6)

[05:45](https://youtube.com/watch?v=5nnJq_IWJog&t=345) - Checking websites (80,443,8080)

[08:10](https://youtube.com/watch?v=5nnJq_IWJog&t=490) - Attempting to enumerate users of OWA-2010 (Fails)

[14:10](https://youtube.com/watch?v=5nnJq_IWJog&t=850) - Checking out Joomla Version (/administrator/manifets/files/joomla.xml)

[15:50](https://youtube.com/watch?v=5nnJq_IWJog&t=950) - Using SearchSploit with (Complain Management System)

[19:38](https://youtube.com/watch?v=5nnJq_IWJog&t=1178) - Register Account, Login, Verify/Play with SQL Union Injection

[23:30](https://youtube.com/watch?v=5nnJq_IWJog&t=1410) - Enumerating SQL Injection with SQLMap

[29:18](https://youtube.com/watch?v=5nnJq_IWJog&t=1758) - Going back to MSF/OWA_LOGIN and testing credentials.

[32:15](https://youtube.com/watch?v=5nnJq_IWJog&t=1935) - Logging into OWA and reading email to find out OpenOFfice, Defender, and Powershell Constain Mode is installed

[36:20](https://youtube.com/watch?v=5nnJq_IWJog&t=2180) - Creating a malicious OpenOffice macro with LibreOffice + Downloading an Executing a file without Powershell (certutil ftw)

[40:18](https://youtube.com/watch?v=5nnJq_IWJog&t=2418) - Compiling Merlin (like MSF/Empire)

[48:40](https://youtube.com/watch?v=5nnJq_IWJog&t=2920) - Sending the email and waiting.

[50:20](https://youtube.com/watch?v=5nnJq_IWJog&t=3020) - Merlin call back, Switch to Powershell Nishang to get a interactive shell

[54:30](https://youtube.com/watch?v=5nnJq_IWJog&t=3270) - Running PowerUp to find we are an Administrator

[56:56](https://youtube.com/watch?v=5nnJq_IWJog&t=3416) - Running JAWS to do some more Windows Enumeration

[01:03:04](https://youtube.com/watch?v=5nnJq_IWJog&t=3784) - Found an odd scheduled task "System Maintenance"

[01:06:03](https://youtube.com/watch?v=5nnJq_IWJog&t=3963) - Attempting to write a php shell to HTTPD

[01:12:30](https://youtube.com/watch?v=5nnJq_IWJog&t=4350) - Frusterated creating a PHP Script... Switch to the SCHTask Privesc

[01:18:20](https://youtube.com/watch?v=5nnJq_IWJog&t=4700) - Uhh. Testing if echo is somehow breaking .bat/.php files

[01:21:50](https://youtube.com/watch?v=5nnJq_IWJog&t=4910) - Going back to test PHP to verify it just didn't like echo.

-----------------------------------------------------------

ippsec: [HackTheBox - Silo](https://youtube.com/watch?v=2c7SzNo9uoA)

0xdf: [HTB: Silo](https://0xdf.gitlab.io//2018/08/04/htb-silo.html)

[01:30](https://youtube.com/watch?v=2c7SzNo9uoA&t=90) - Begin of recon

[03:15](https://youtube.com/watch?v=2c7SzNo9uoA&t=195) - Begin of installing SQLPlus and ODAT (Oracle Database Attack Tool)

[08:45](https://youtube.com/watch?v=2c7SzNo9uoA&t=525) - Bruteforcing the SID with ODAT

[10:15](https://youtube.com/watch?v=2c7SzNo9uoA&t=615) - Holy crap, this is slow lets also do it with Metasploit

[13:00](https://youtube.com/watch?v=2c7SzNo9uoA&t=780) - Bruteforcing valid logins with ODAT

[16:00](https://youtube.com/watch?v=2c7SzNo9uoA&t=960) - Credentials returned, logging into Oracle with SQLPlus as SysDBA

[19:00](https://youtube.com/watch?v=2c7SzNo9uoA&t=1140) - Reading files from disk via Oracle

[23:20](https://youtube.com/watch?v=2c7SzNo9uoA&t=1400) - Writing files to disk from Oracle.  Testing it in WebRoot Directory

[25:52](https://youtube.com/watch?v=2c7SzNo9uoA&t=1552) - File Written, lets write an ASPX WebShell to the Server

[29:10](https://youtube.com/watch?v=2c7SzNo9uoA&t=1750) - WebShell Working!  Lets get a Reverse Shell

[31:28](https://youtube.com/watch?v=2c7SzNo9uoA&t=1888) - Reverse Shell Returned

[32:24](https://youtube.com/watch?v=2c7SzNo9uoA&t=1944) - Finding a DropBox link, but password doesn't display well.

[33:55](https://youtube.com/watch?v=2c7SzNo9uoA&t=2035) - Attempting to copy file via SMB to view UTF8 Text

[35:18](https://youtube.com/watch?v=2c7SzNo9uoA&t=2118) - That didn't work, lets transfer the file by encoding it in Base64.

[36:55](https://youtube.com/watch?v=2c7SzNo9uoA&t=2215) - Got the password lets download the dump!

[39:10](https://youtube.com/watch?v=2c7SzNo9uoA&t=2350) - Begin of Volatility

[45:20](https://youtube.com/watch?v=2c7SzNo9uoA&t=2720) - Running the HashDump plugin from volatilty then PassTheHash with Administrator's NTLM!

[47:35](https://youtube.com/watch?v=2c7SzNo9uoA&t=2855) - Begin of unintended way, examining odat and uploading an meterpreter exe

[50:30](https://youtube.com/watch?v=2c7SzNo9uoA&t=3030) - Using odat externaltable to execute meterpreter and get a system shell!

[52:20](https://youtube.com/watch?v=2c7SzNo9uoA&t=3140) - Examining odat verbosity flag to see what commands it runs and try to learn.

-----------------------------------------------------------

ippsec: [HackTheBox - Valentine](https://youtube.com/watch?v=XYXNvemgJUo)

0xdf: [HTB: Valentine](https://0xdf.gitlab.io//2018/07/28/htb-valentine.html)

[00:25](https://youtube.com/watch?v=XYXNvemgJUo&t=25) - Start of Recon, identifying end of life OS from nmap

[03:20](https://youtube.com/watch?v=XYXNvemgJUo&t=200) - Running vulnerability scripts in nmap to discover heartbleed

[04:16](https://youtube.com/watch?v=XYXNvemgJUo&t=256) - Going to the HTTP Page to see what it looks like

[06:30](https://youtube.com/watch?v=XYXNvemgJUo&t=390) - Begin of Heartbleed - Grabbing Python Module

[07:13](https://youtube.com/watch?v=XYXNvemgJUo&t=433) - Explaining Heartbleed -- XKCD ftw

[10:15](https://youtube.com/watch?v=XYXNvemgJUo&t=615) - Explaining and running the exploit

[13:40](https://youtube.com/watch?v=XYXNvemgJUo&t=820) - Exporting large chunks of memory by running in a loop

[14:10](https://youtube.com/watch?v=XYXNvemgJUo&t=850) - Finding an encrypted SSH Key on the server

[15:35](https://youtube.com/watch?v=XYXNvemgJUo&t=935) - Examining heartbleed output to discover SSH Key Password

[17:45](https://youtube.com/watch?v=XYXNvemgJUo&t=1065) - SSH as low priv user returned

[21:55](https://youtube.com/watch?v=XYXNvemgJUo&t=1315) - Finding a writable tmux socket to hijack session and find a root shell

[23:50](https://youtube.com/watch?v=XYXNvemgJUo&t=1430) - Alternative Privesc, DirtyC0w

-----------------------------------------------------------

ippsec: [HackTheBox -  Aragog](https://youtube.com/watch?v=NFdi-2tgvxY)



[01:26](https://youtube.com/watch?v=NFdi-2tgvxY&t=86) - Start of Recon

[03:25](https://youtube.com/watch?v=NFdi-2tgvxY&t=205) - Notice SSH configured for Pub Key Only.  Hint at what to grab later!

[03:50](https://youtube.com/watch?v=NFdi-2tgvxY&t=230) - Grabbing test.txt off ftp server via anonymous auth

[04:07](https://youtube.com/watch?v=NFdi-2tgvxY&t=247) - Determining if I want to go down the "Exploit VSFTPD" rabbit hole

[05:54](https://youtube.com/watch?v=NFdi-2tgvxY&t=354) - Viewing test.txt and hosts.php

[06:48](https://youtube.com/watch?v=NFdi-2tgvxY&t=408) - Figuring out how hosts.php works and discovering XXE

[08:58](https://youtube.com/watch?v=NFdi-2tgvxY&t=538) - Start of XXE Discovery

[10:16](https://youtube.com/watch?v=NFdi-2tgvxY&t=616) - Making the XXE Output /etc/passwd

[11:33](https://youtube.com/watch?v=NFdi-2tgvxY&t=693) - Encoding output in Base64 in order to view PHP Files

[12:58](https://youtube.com/watch?v=NFdi-2tgvxY&t=778) - Using Burp Intruder to BruteForce Files

[16:20](https://youtube.com/watch?v=NFdi-2tgvxY&t=980) - Creating a program to bruteforce home directories

[26:41](https://youtube.com/watch?v=NFdi-2tgvxY&t=1601) - Program Finished.  Finding SSH ID_RSA Key

[28:15](https://youtube.com/watch?v=NFdi-2tgvxY&t=1695) - Low Priv Access Granted

[30:24](https://youtube.com/watch?v=NFdi-2tgvxY&t=1824) - LinEnum.sh shows Wordpress CHMOD'd to 777

[31:05](https://youtube.com/watch?v=NFdi-2tgvxY&t=1865) - Examining Wordpress Site (big hint left by author)

[32:10](https://youtube.com/watch?v=NFdi-2tgvxY&t=1930) - Enumerating MySQL Database

[35:15](https://youtube.com/watch?v=NFdi-2tgvxY&t=2115) - Giving up on MySQL, lets edit PHP Files to dump passwords!

[36:50](https://youtube.com/watch?v=NFdi-2tgvxY&t=2210) - Identifying the file we want to backdoor

[37:51](https://youtube.com/watch?v=NFdi-2tgvxY&t=2271) - Placing our PHP Code

[42:06](https://youtube.com/watch?v=NFdi-2tgvxY&t=2526) - Got the password!

-----------------------------------------------------------

ippsec: [HackTheBox - Nightmarev2  - Speed Run/Unintended Solutions](https://youtube.com/watch?v=TVhtjiSedjU)



[01:10](https://youtube.com/watch?v=TVhtjiSedjU&t=70) - End of intro, Start of nmap

[02:47](https://youtube.com/watch?v=TVhtjiSedjU&t=167) - Playing with Second-Order Union Injection

[05:44](https://youtube.com/watch?v=TVhtjiSedjU&t=344) - Dumping all users

[07:15](https://youtube.com/watch?v=TVhtjiSedjU&t=435) - Converting SFTP Exploit from 64bit to 32bit

[13:27](https://youtube.com/watch?v=TVhtjiSedjU&t=807) - Reversing SLS Binary

[15:19](https://youtube.com/watch?v=TVhtjiSedjU&t=919) - Kernel Exploit

[22:31](https://youtube.com/watch?v=TVhtjiSedjU&t=1351) - First Method - Executing ELF Binaries from memory (Reflective loading elf)

[35:57](https://youtube.com/watch?v=TVhtjiSedjU&t=2157) - Second Method - Crashing a program to create a write-able file.

-----------------------------------------------------------

ippsec: [HackTheBox - Bart](https://youtube.com/watch?v=Cz6vQvGGiuc)

0xdf: [HTB: Bart](https://0xdf.gitlab.io//2018/07/15/htb-bart.html)

[01:54](https://youtube.com/watch?v=Cz6vQvGGiuc&t=114) - Begin Recon, Windows IIS/OS Mapping and GoBuster

[05:20](https://youtube.com/watch?v=Cz6vQvGGiuc&t=320) - Explanation of Virtual Host Routing

[09:50](https://youtube.com/watch?v=Cz6vQvGGiuc&t=590) - Developers name exposed in HTML Source, also discover /monitor

[11:10](https://youtube.com/watch?v=Cz6vQvGGiuc&t=670) - Enumerating Username in PHP Server Monitor: Challenge Watch Sense to und

[16:33](https://youtube.com/watch?v=Cz6vQvGGiuc&t=993) - Discover of Internal-01.bart.htb

[19:17](https://youtube.com/watch?v=Cz6vQvGGiuc&t=1157) - Harveys Password with Hydra (Note: This is bypassable if you DIRBUST to find /Log/log.php)

[29:34](https://youtube.com/watch?v=Cz6vQvGGiuc&t=1774) - Finally got Hydra to return the password!

[32:20](https://youtube.com/watch?v=Cz6vQvGGiuc&t=1940) - Log Poisoning + LFI = Remote Code Execution

[37:30](https://youtube.com/watch?v=Cz6vQvGGiuc&t=2250) - Return of Reverse Shell

[41:30](https://youtube.com/watch?v=Cz6vQvGGiuc&t=2490) - Why you should check if you're a 32-bit process on a 64-bit machine

[48:35](https://youtube.com/watch?v=Cz6vQvGGiuc&t=2915) - Attempting to use b33f/FuzzySecurity Invoke-RunAs

[56:00](https://youtube.com/watch?v=Cz6vQvGGiuc&t=3360) - Mistake with Invoke-RunAs is probably pointing it to the wrong port. D:

[01:03:40](https://youtube.com/watch?v=Cz6vQvGGiuc&t=3820) - ARGH!  Lets try to use this account via Empire

[01:11:00](https://youtube.com/watch?v=Cz6vQvGGiuc&t=4260) - Bring out the big guns, it's Metasploit Time!

[01:18:10](https://youtube.com/watch?v=Cz6vQvGGiuc&t=4690) - Alright, lets poke a hole in the firewall and connect over SMB!

[01:21:17](https://youtube.com/watch?v=Cz6vQvGGiuc&t=4877) - Failed to PSExec in MSF

[01:21:40](https://youtube.com/watch?v=Cz6vQvGGiuc&t=4900) - Found Impacket-PSExec!  And it works!

[01:23:45](https://youtube.com/watch?v=Cz6vQvGGiuc&t=5025) - Lets go hunt for creds!

[01:35:23](https://youtube.com/watch?v=Cz6vQvGGiuc&t=5723) - Cracking Salted Hashes with Hashcat (Sha265.Salt)

-----------------------------------------------------------

ippsec: [HackTheBox - Nightmare](https://youtube.com/watch?v=frh-jYaUvrU)



[01:50](https://youtube.com/watch?v=frh-jYaUvrU&t=110) - Start of Recon

[04:58](https://youtube.com/watch?v=frh-jYaUvrU&t=298) - /documents and /secret rabbit hole enumeration

[08:13](https://youtube.com/watch?v=frh-jYaUvrU&t=493) - Using wfuzz on the /secret rabbit hole to find argument for download.php

[13:40](https://youtube.com/watch?v=frh-jYaUvrU&t=820) - Begin of Web Application Enumeration, some XSS Found

[18:23](https://youtube.com/watch?v=frh-jYaUvrU&t=1103) - Throwing bad characters in username and finding Second-Order SQL Injection.

[23:50](https://youtube.com/watch?v=frh-jYaUvrU&t=1430) - Begin of Union Injection to dump the database via second order sql injection

[39:36](https://youtube.com/watch?v=frh-jYaUvrU&t=2376) - Dumping users and passwords from SysAdmin table and using Hydra to bruteforce SSH

[43:54](https://youtube.com/watch?v=frh-jYaUvrU&t=2634) - Enumerating SFTP (Using SSHFS to Dump a File Listing)

[53:00](https://youtube.com/watch?v=frh-jYaUvrU&t=3180) - Converting 64-Bit SFTP Exploit to 32-Bit

[01:11:46](https://youtube.com/watch?v=frh-jYaUvrU&t=4306) - Reverse Shell Returned, some stuff and finding Set-GID Binary

[01:22:55](https://youtube.com/watch?v=frh-jYaUvrU&t=4975) - Reversing SLS binary with Radare2 (r2)

[01:47:53](https://youtube.com/watch?v=frh-jYaUvrU&t=6473) - Exploiting SLS Binary with new line character (Get to Decoder User)

[01:51:47](https://youtube.com/watch?v=frh-jYaUvrU&t=6707) - Begin of Kernel Exploitation (CVE-2017-1000112)

[01:56:00](https://youtube.com/watch?v=frh-jYaUvrU&t=6960) - Kernel Exploit Compiled (silly mistake before)

[01:59:52](https://youtube.com/watch?v=frh-jYaUvrU&t=7192) - Creating a new lsb-release file so exploit can identify kernel

[02:07:03](https://youtube.com/watch?v=frh-jYaUvrU&t=7623) - Recap of Box

[02:09:56](https://youtube.com/watch?v=frh-jYaUvrU&t=7796) - Creating a Tamper Script to do Second-Order SQL Injection

-----------------------------------------------------------

ippsec: [HackTheBox - Nibbles](https://youtube.com/watch?v=s_0GcRGv6Ds)

0xdf: [HTB: Nibbles](https://0xdf.gitlab.io//2018/06/30/htb-nibbles.html)

[00:18](https://youtube.com/watch?v=s_0GcRGv6Ds&t=18) - Start of Recon

[01:15](https://youtube.com/watch?v=s_0GcRGv6Ds&t=75) - Finding hidden directory via Source

[02:15](https://youtube.com/watch?v=s_0GcRGv6Ds&t=135) - Downloading NibbleBlog to help us with finding version information

[03:59](https://youtube.com/watch?v=s_0GcRGv6Ds&t=239) - Identifying what vresion of NibblesBlog is running

[04:42](https://youtube.com/watch?v=s_0GcRGv6Ds&t=282) - Using SearchSploit to find vulnerabilities

[05:36](https://youtube.com/watch?v=s_0GcRGv6Ds&t=336) - Examining the Exploit

[06:08](https://youtube.com/watch?v=s_0GcRGv6Ds&t=368) - Explanation of exploit

[07:25](https://youtube.com/watch?v=s_0GcRGv6Ds&t=445) - Attempting to find valid usernames for NibblesBlog

[09:13](https://youtube.com/watch?v=s_0GcRGv6Ds&t=553) - Finding usernames in /content/private

[10:15](https://youtube.com/watch?v=s_0GcRGv6Ds&t=615) - Using Hydra to attempt to bruteforce

[14:08](https://youtube.com/watch?v=s_0GcRGv6Ds&t=848) - Oh crap. Hydra not good idea we're blocked...

[15:40](https://youtube.com/watch?v=s_0GcRGv6Ds&t=940) - Using SSH Proxies to hit nibbles from another box (Falafel)

[18:20](https://youtube.com/watch?v=s_0GcRGv6Ds&t=1100) - Guessing the password

[20:10](https://youtube.com/watch?v=s_0GcRGv6Ds&t=1210) - Logged in, lets attempt our exploit!

[22:46](https://youtube.com/watch?v=s_0GcRGv6Ds&t=1366) - Code Execution achieved.  Lets get a reverse shell

[24:53](https://youtube.com/watch?v=s_0GcRGv6Ds&t=1493) - Reverse shell returned.

[26:00](https://youtube.com/watch?v=s_0GcRGv6Ds&t=1560) - Running sudo -l examine sudoer, then finding out why sudo took forever to return

[26:50](https://youtube.com/watch?v=s_0GcRGv6Ds&t=1610) - Privesc via bad sudo rules

[32:10](https://youtube.com/watch?v=s_0GcRGv6Ds&t=1930) - Alternative PrivEsc via RationalLove

-----------------------------------------------------------

ippsec: [HackTheBox - Falafel](https://youtube.com/watch?v=CUbWpteTfio)

0xdf: [HTB: Falafel](https://0xdf.gitlab.io//2018/06/23/htb-falafel.html)

[01:15](https://youtube.com/watch?v=CUbWpteTfio&t=75) - Begin of Recon

[04:25](https://youtube.com/watch?v=CUbWpteTfio&t=265) - Bruteforcing valid users

[11:15](https://youtube.com/watch?v=CUbWpteTfio&t=675) - Manually finding SQL Injection

[13:13](https://youtube.com/watch?v=CUbWpteTfio&t=793) - Using --string with SQLMap to aid Boolean Detection

[15:41](https://youtube.com/watch?v=CUbWpteTfio&t=941) - PHP Type Confusion ( == vs === with 0e12345) [Type Juggling]

[18:35](https://youtube.com/watch?v=CUbWpteTfio&t=1115) - Attempting Wget Exploit with FTP Redirection (failed)

[26:39](https://youtube.com/watch?v=CUbWpteTfio&t=1599) - Exploiting wget's maximum file length

[33:30](https://youtube.com/watch?v=CUbWpteTfio&t=2010) - Reverse Shell Returned

[36:19](https://youtube.com/watch?v=CUbWpteTfio&t=2179) - Linux Priv Checking Enum

[41:00](https://youtube.com/watch?v=CUbWpteTfio&t=2460) - Checking web crap for passwords

[44:00](https://youtube.com/watch?v=CUbWpteTfio&t=2640) - Grabbing the screenshot of tty

[49:00](https://youtube.com/watch?v=CUbWpteTfio&t=2940) - Privesc via Yossi being in Disk Group (debugfs)

[50:15](https://youtube.com/watch?v=CUbWpteTfio&t=3015) - Grabbing ssh root key off /dev/sda1

[52:15](https://youtube.com/watch?v=CUbWpteTfio&t=3135) - Attempting RationLove (Fails, apparently machine got patched so notes were wrong /troll)

[01:07:42](https://youtube.com/watch?v=CUbWpteTfio&t=4062) - Manually exploiting the SQL Injection! with Python

-----------------------------------------------------------

ippsec: [HackTheBox - Chatterbox](https://youtube.com/watch?v=_dRrvJNdP-s)

0xdf: [HTB: Chatterbox](https://0xdf.gitlab.io//2018/06/18/htb-chatterbox.html)

[01:18](https://youtube.com/watch?v=_dRrvJNdP-s&t=78) - Begin of Recon

[04:55](https://youtube.com/watch?v=_dRrvJNdP-s&t=295) - Start of aChat buffer Overflow: Finding the exploit script with Searchsploit

[07:24](https://youtube.com/watch?v=_dRrvJNdP-s&t=444) - Begin of replacing POC's Calc Shellcode with what is generated from MSFVenom

[09:42](https://youtube.com/watch?v=_dRrvJNdP-s&t=582) - Correction: Payload Size wrong, should be 3,xxx -- look at "Payload Size" I accidentally highlighted the size of the python file.

[14:30](https://youtube.com/watch?v=_dRrvJNdP-s&t=870) - Whoops, erased too much out of POC.  Lets correctly replace the shellcode this time and get a shell.

[17:50](https://youtube.com/watch?v=_dRrvJNdP-s&t=1070) - Running PowerUp to find AutoLogon Credentials

[20:05](https://youtube.com/watch?v=_dRrvJNdP-s&t=1205) - Running Code as Administrator

[24:18](https://youtube.com/watch?v=_dRrvJNdP-s&t=1458) - First Privesc Method: Using Start-Process to execute commands as a different user because Invoke-Command did not work.  

[27:30](https://youtube.com/watch?v=_dRrvJNdP-s&t=1650) - Alternate way to read root.txt -- Alfred owns root.txt, so he can edit the files access list. Get-ACL to view access list and cacls to modify

[33:12](https://youtube.com/watch?v=_dRrvJNdP-s&t=1992) - Summary of the box

[34:37](https://youtube.com/watch?v=_dRrvJNdP-s&t=2077) - Doing the box with Metasaploit, Warning: Lots of fails.

[43:10](https://youtube.com/watch?v=_dRrvJNdP-s&t=2590) - Using meterpreters PortFwd to bypass ChatterBox's firewall and access port 445

[51:25](https://youtube.com/watch?v=_dRrvJNdP-s&t=3085) - Doing the box with Empire !

[58:20](https://youtube.com/watch?v=_dRrvJNdP-s&t=3500) - Using Empire's Run_As module to execute commands as Administrator

-----------------------------------------------------------

ippsec: [HackTheBox - Fulcrum](https://youtube.com/watch?v=46RJxJ-Fm0Y)



[02:08](https://youtube.com/watch?v=46RJxJ-Fm0Y&t=128) - Begin of Recon

[14:00](https://youtube.com/watch?v=46RJxJ-Fm0Y&t=840) - XXE Detection on Fulcrum API

[17:40](https://youtube.com/watch?v=46RJxJ-Fm0Y&t=1060) - XXE Get Files

[23:40](https://youtube.com/watch?v=46RJxJ-Fm0Y&t=1420) - XXE File Retrieval Working

[24:30](https://youtube.com/watch?v=46RJxJ-Fm0Y&t=1470) - Lets Code a Python WebServer to Aid in XXE Exploitation

[39:45](https://youtube.com/watch?v=46RJxJ-Fm0Y&t=2385) - Combining XXE + SSRF (Server Side Request Forgery) to gain Code Execution

[47:28](https://youtube.com/watch?v=46RJxJ-Fm0Y&t=2848) - Shell Returned + Go Over LinEnum

[56:49](https://youtube.com/watch?v=46RJxJ-Fm0Y&t=3409) - Finding WebUser's Password and using WinRM to pivot

[01:06:00](https://youtube.com/watch?v=46RJxJ-Fm0Y&t=3960) - Getting Shell via WinRM, finding LDAP Credentials

[01:14:00](https://youtube.com/watch?v=46RJxJ-Fm0Y&t=4440) - Using PowerView to Enumerate AD Users

[01:27:06](https://youtube.com/watch?v=46RJxJ-Fm0Y&t=5226) - Start of getting a Shell on FILE (TroubleShooting FW)

[01:35:35](https://youtube.com/watch?v=46RJxJ-Fm0Y&t=5735) - Getting shell over TCP/53 on FILE

[01:37:58](https://youtube.com/watch?v=46RJxJ-Fm0Y&t=5878) - Finding credentials on scripts in Active Directories NetLogon Share, then finding a way to execute code as the Domain Admin... Triple Hop Nightmare

[01:58:10](https://youtube.com/watch?v=46RJxJ-Fm0Y&t=7090) - Troubleshooting the error correctly and getting Domain Admin!

[02:03:54](https://youtube.com/watch?v=46RJxJ-Fm0Y&t=7434) - Begin of unintended method (Rooting the initial Linux Hop)

[02:09:54](https://youtube.com/watch?v=46RJxJ-Fm0Y&t=7794) - Root Exploit Found

[02:12:25](https://youtube.com/watch?v=46RJxJ-Fm0Y&t=7945) - Mounting the VMDK Files and accessing AD.

-----------------------------------------------------------

ippsec: [HackTheBox - Tally](https://youtube.com/watch?v=l-wzBhc9wFc)



[01:45](https://youtube.com/watch?v=l-wzBhc9wFc&t=105) - Start of NMAP

[04:17](https://youtube.com/watch?v=l-wzBhc9wFc&t=257) - Begin of Sharepoint/GoBuster (Special Sharepoint List)

[06:32](https://youtube.com/watch?v=l-wzBhc9wFc&t=392) - Manually browsing to Sitecontent (Get FTP Creds)

[10:18](https://youtube.com/watch?v=l-wzBhc9wFc&t=618) - Mirror FTP + Pillage for information, Find keypass in Tim's directory and crack it.

[18:22](https://youtube.com/watch?v=l-wzBhc9wFc&t=1102) - Mounting/Mirroring ACCT Share with found Creds and finding hardcoded SQL Creds

[25:24](https://youtube.com/watch?v=l-wzBhc9wFc&t=1524) - Logging into MSSQL with SQSH, enabling xp_cmdshell and getting a Nishang Rev Shell

[34:35](https://youtube.com/watch?v=l-wzBhc9wFc&t=2075) - Finding SPBestWarmUp.ps1 Scheduled Task that runs as Administrator

[40:00](https://youtube.com/watch?v=l-wzBhc9wFc&t=2400) - Begin of RottenPotato without MSF (Decoder's Lonely Potato)

[45:56](https://youtube.com/watch?v=l-wzBhc9wFc&t=2756) - Using Ebowla Encoding for AV Evasion to create an exe for use with Lonely Potato

[58:00](https://youtube.com/watch?v=l-wzBhc9wFc&t=3480) - Lonely Potato Running to return a Admin Shell

[01:04:22](https://youtube.com/watch?v=l-wzBhc9wFc&t=3862) - Finding CVE-2017-0213

[01:08:33](https://youtube.com/watch?v=l-wzBhc9wFc&t=4113) - Installing Visual Studio 2015 && Compiling the exploit

[01:15:50](https://youtube.com/watch?v=l-wzBhc9wFc&t=4550) - Exploit Compiled, trying to get it to work....

[01:18:11](https://youtube.com/watch?v=l-wzBhc9wFc&t=4691) - Just noticed the SPBestWarmUp.ps1 executed and gave us a shell!

[01:28:37](https://youtube.com/watch?v=l-wzBhc9wFc&t=5317) - Found the issue, exploit seems to require interactive process

[01:30:00](https://youtube.com/watch?v=l-wzBhc9wFc&t=5400) - Begin of Firefox Exploit Cluster (Not recommended to watch lol).  It's a second unreliable way to get user

-----------------------------------------------------------

ippsec: [HackTheBox - CrimeStoppers](https://youtube.com/watch?v=bgKth1K44QA)

0xdf: [HTB: CrimeStoppers](https://0xdf.gitlab.io//2018/06/03/htb-crimestoppers.html)

[01:18](https://youtube.com/watch?v=bgKth1K44QA&t=78) - Begin of Recon: Getting ubuntu version

[04:00](https://youtube.com/watch?v=bgKth1K44QA&t=240) - Navigating to the CrimeStoppers Page

[05:15](https://youtube.com/watch?v=bgKth1K44QA&t=315) - First Hint - Read The Source!

[05:50](https://youtube.com/watch?v=bgKth1K44QA&t=350) - 2nd Hint - No SQL Databases and playing with the upload form

[07:55](https://youtube.com/watch?v=bgKth1K44QA&t=475) - 3rd Hint - Setting Admin cookie to 1 to see whiterose.txt

[09:00](https://youtube.com/watch?v=bgKth1K44QA&t=540) - Explanation of PHP App and why I went down testing $op parameter

[10:45](https://youtube.com/watch?v=bgKth1K44QA&t=645) - Testing $op parameter, another hint what year is it?

[12:20](https://youtube.com/watch?v=bgKth1K44QA&t=740) - Finding out $op appends .php

[13:05](https://youtube.com/watch?v=bgKth1K44QA&t=785) - Using php b64 filter to view php files ("Read the source luke")

[22:50](https://youtube.com/watch?v=bgKth1K44QA&t=1370) - Looking into PHP Wrappers to try to gain code execution

[24:50](https://youtube.com/watch?v=bgKth1K44QA&t=1490) - Placing our PHP Script in a zip so we can reference it with zip://, also improperly upload it to the server

[26:20](https://youtube.com/watch?v=bgKth1K44QA&t=1580) - Attempting to use the zip:// wrapper to execute our php script, then troubleshooting the bad upload.

[30:30](https://youtube.com/watch?v=bgKth1K44QA&t=1830) - Easy way to copy binary data into BurpSuite (Base64)

[34:10](https://youtube.com/watch?v=bgKth1K44QA&t=2050) - Getting a shell

[37:18](https://youtube.com/watch?v=bgKth1K44QA&t=2238) - Downloading ThunderBird Directory and reading email + getting dom's password

[46:20](https://youtube.com/watch?v=bgKth1K44QA&t=2780) - Begin of looking into Apache Rootkit (mod_rootme)

[48:04](https://youtube.com/watch?v=bgKth1K44QA&t=2884) - Begin of using r2 (Radare) to analyze rootkit, basic intro

[50:55](https://youtube.com/watch?v=bgKth1K44QA&t=3055) - Analyzing DarkArmy Function

[55:30](https://youtube.com/watch?v=bgKth1K44QA&t=3330) - Grabbing the strings and using python to XOR them to get secret that allows root

[58:35](https://youtube.com/watch?v=bgKth1K44QA&t=3515) - Get Root 

[59:10](https://youtube.com/watch?v=bgKth1K44QA&t=3550) - Potential rabbit hole in the binary /var/www/html/whiterose.txt in the binary

[01:04:20](https://youtube.com/watch?v=bgKth1K44QA&t=3860) - Second way to get root, looking around at file modification times to find FunSociety in logs

-----------------------------------------------------------

ippsec: [HackTheBox - Jeeves](https://youtube.com/watch?v=EKGBskG8APc)



[01:19](https://youtube.com/watch?v=EKGBskG8APc&t=79) - Begin of Enumeration

[04:15](https://youtube.com/watch?v=EKGBskG8APc&t=255) - Avoiding the Rabbit Hole on port 80 (IIS)

[06:00](https://youtube.com/watch?v=EKGBskG8APc&t=360) - Begin of Jenkins

[09:00](https://youtube.com/watch?v=EKGBskG8APc&t=540) - Using Jenkins Script Console (Groovy) to gain code execution

[12:00](https://youtube.com/watch?v=EKGBskG8APc&t=720) - Reverse TCP Shell via Nishang

[17:00](https://youtube.com/watch?v=EKGBskG8APc&t=1020) - Reverse Shell returned.  PowerSplit dev branch to find unintended privesc (Tokens)

[22:20](https://youtube.com/watch?v=EKGBskG8APc&t=1340) - Powersploit's Invoke-AllChecks completes

[24:20](https://youtube.com/watch?v=EKGBskG8APc&t=1460) - Finding Keepass Database using Impack-SMBServer to transfer files

[27:00](https://youtube.com/watch?v=EKGBskG8APc&t=1620) - Cracking the KeePass Database

[30:20](https://youtube.com/watch?v=EKGBskG8APc&t=1820) - Using KeePass2 to open database

[34:25](https://youtube.com/watch?v=EKGBskG8APc&t=2065) - PassTheHash via pth-winexe to gain administrator shell

[35:20](https://youtube.com/watch?v=EKGBskG8APc&t=2120) - Grabbing root.txt that is hidden via Alternate Data Streams (ADS)

[39:00](https://youtube.com/watch?v=EKGBskG8APc&t=2340) - Using RottenPotato to escalate to root via MSF

[41:00](https://youtube.com/watch?v=EKGBskG8APc&t=2460) - Using Unicorn to gain a reverse MSF SHell

[45:20](https://youtube.com/watch?v=EKGBskG8APc&t=2720) - Performing the attack

[48:00](https://youtube.com/watch?v=EKGBskG8APc&t=2880) - Impersonating Token to gain root

-----------------------------------------------------------

ippsec: [HackTheBox - Flux Capacitor](https://youtube.com/watch?v=XLIBbkQJKuY)



[01:25](https://youtube.com/watch?v=XLIBbkQJKuY&t=85) - Begin of recon

[02:20](https://youtube.com/watch?v=XLIBbkQJKuY&t=140) - Wiresharking NMAP to identify fingerprint

[05:53](https://youtube.com/watch?v=XLIBbkQJKuY&t=353) - Checking the WebPage

[09:15](https://youtube.com/watch?v=XLIBbkQJKuY&t=555) - Finding /sync and why web browser has a 403

[12:45](https://youtube.com/watch?v=XLIBbkQJKuY&t=765) - Using wfuzz to find what arguments /sync takes

[15:45](https://youtube.com/watch?v=XLIBbkQJKuY&t=945) - The actual wfuzz command

[20:30](https://youtube.com/watch?v=XLIBbkQJKuY&t=1230) - Finding Bad Characters with wfuzz

[24:51](https://youtube.com/watch?v=XLIBbkQJKuY&t=1491) - Getting command execution

[32:00](https://youtube.com/watch?v=XLIBbkQJKuY&t=1920) - Getting a reverse shell

[43:40](https://youtube.com/watch?v=XLIBbkQJKuY&t=2620) - Privesc to root abusing custom script

[47:48](https://youtube.com/watch?v=XLIBbkQJKuY&t=2868) - Examining how NGINX/OpenResty was configured

-----------------------------------------------------------

HackTheBox - Bashed
https://youtube.com/watch?v=2DqdPcbYcy8

-----------------------------------------------------------

ippsec: [HackTheBox - Ariekei](https://youtube.com/watch?v=Pc4tzsn-ats)



[00:23](https://youtube.com/watch?v=Pc4tzsn-ats&t=23) - Explaining VM Layout

[01:47](https://youtube.com/watch?v=Pc4tzsn-ats&t=107) - Nmap Start

[05:20](https://youtube.com/watch?v=Pc4tzsn-ats&t=320) - Poking at Virtual Host Routing (Beehive & Calvin)

[10:25](https://youtube.com/watch?v=Pc4tzsn-ats&t=625) - Fixing GoBuster to find /cgi-bin/

[11:48](https://youtube.com/watch?v=Pc4tzsn-ats&t=708) - Enumerating WAF (Web Application Firewall), to see how it detects Shellshock

[15:08](https://youtube.com/watch?v=Pc4tzsn-ats&t=908) - Using VirtualHostRouting to navigate to Calvin.htb.htb

[18:15](https://youtube.com/watch?v=Pc4tzsn-ats&t=1095) - Using ImageTragick to exploit Calvin

[25:30](https://youtube.com/watch?v=Pc4tzsn-ats&t=1530) - Calvin Reverse shell returned

[31:35](https://youtube.com/watch?v=Pc4tzsn-ats&t=1895) - Poking at /common, which allows pivot to Bastion Host

[34:20](https://youtube.com/watch?v=Pc4tzsn-ats&t=2060) - SSH into the Bastion Host

[38:45](https://youtube.com/watch?v=Pc4tzsn-ats&t=2325) - Explain SSH Local and Remote Port Forwarding

[46:00](https://youtube.com/watch?v=Pc4tzsn-ats&t=2760) - Beehive Reverse Shell Returned

[50:00](https://youtube.com/watch?v=Pc4tzsn-ats&t=3000) - Finding the root password via /common/containers/bastion-live/Dockerfile

[54:50](https://youtube.com/watch?v=Pc4tzsn-ats&t=3290) - PrivEsc via Docker (much like the LXC shown in Calamity)

[57:05](https://youtube.com/watch?v=Pc4tzsn-ats&t=3425) - Getting root access to filesystem

[58:10](https://youtube.com/watch?v=Pc4tzsn-ats&t=3490) - Failing to get root shell via Crontab

[01:06:20](https://youtube.com/watch?v=Pc4tzsn-ats&t=3980) - Yeah screw crontab, lets just create an ssh key.

-----------------------------------------------------------

ippsec: [HackTheBox - Inception](https://youtube.com/watch?v=J2I-5xPgyXk)



[01:05](https://youtube.com/watch?v=J2I-5xPgyXk&t=65) - Start of Recon + Finding dompdf

[08:30](https://youtube.com/watch?v=J2I-5xPgyXk&t=510) - PHP Wrappers + Failed testing for RCE

[11:35](https://youtube.com/watch?v=J2I-5xPgyXk&t=695) - Writing Python Program to automate file disclosure bug

[18:40](https://youtube.com/watch?v=J2I-5xPgyXk&t=1120) - Finding WebDav Configuration + Uploading Files for RCE

[25:50](https://youtube.com/watch?v=J2I-5xPgyXk&t=1550) - Modifying Sokar's Forward Shell (PTY over HTTP)

[33:55](https://youtube.com/watch?v=J2I-5xPgyXk&t=2035) - Forward shell returned

[38:50](https://youtube.com/watch?v=J2I-5xPgyXk&t=2330) - Using Squid to pivot to ports listening locally + NMAP via ProxyChains

[47:48](https://youtube.com/watch?v=J2I-5xPgyXk&t=2868) - Getting nmap on Inception to speed up scanning private network

[59:16](https://youtube.com/watch?v=J2I-5xPgyXk&t=3556) - Nmap results returned for 192.168.0.1, FTP Anonymous Login

-----------------------------------------------------------

ippsec: [HackTheBox - Minion](https://youtube.com/watch?v=IbVmpr6IFQU)



[00:40](https://youtube.com/watch?v=IbVmpr6IFQU&t=40) - Begin of Recon

[04:00](https://youtube.com/watch?v=IbVmpr6IFQU&t=240) - Start of GoBuster

[05:40](https://youtube.com/watch?v=IbVmpr6IFQU&t=340) - Finding a SSRF

[09:00](https://youtube.com/watch?v=IbVmpr6IFQU&t=540) - Passing arguments to cmd.aspx via SSRF

[12:05](https://youtube.com/watch?v=IbVmpr6IFQU&t=725) - Firewall Enumeration 

[16:35](https://youtube.com/watch?v=IbVmpr6IFQU&t=995) - Begin of setting up ICMP Reverse Shell

[22:25](https://youtube.com/watch?v=IbVmpr6IFQU&t=1345) - Begin of sending ICMP Rev Shell to Server (Warning: Lots of Fail)

[46:31](https://youtube.com/watch?v=IbVmpr6IFQU&t=2791) - Return of ICMP Rev Shell

[52:20](https://youtube.com/watch?v=IbVmpr6IFQU&t=3140) - PrivEsc form IIS to Decoder

[01:11:15](https://youtube.com/watch?v=IbVmpr6IFQU&t=4275) - Unzipping via Powershell

[01:14:05](https://youtube.com/watch?v=IbVmpr6IFQU&t=4445) - Finding Administrator password hidden in NTFS File Stream

[01:16:30](https://youtube.com/watch?v=IbVmpr6IFQU&t=4590) - Using Net Use to mount C: As Administrator

[01:19:30](https://youtube.com/watch?v=IbVmpr6IFQU&t=4770) - Using IDA to analyze root.exe and grab the flag (Misses last character of hash)

[01:24:15](https://youtube.com/watch?v=IbVmpr6IFQU&t=5055) - Using Invoke Command to execute root.exe as admin (Lots of Fail)

[01:32:52](https://youtube.com/watch?v=IbVmpr6IFQU&t=5572) - Opening up the Firewall then just using RDP to gain access

-----------------------------------------------------------

ippsec: [HackTheBox - Sense](https://youtube.com/watch?v=d2nVDoVr0jE)



[01:20](https://youtube.com/watch?v=d2nVDoVr0jE&t=80) - Star of Recon

[03:40](https://youtube.com/watch?v=d2nVDoVr0jE&t=220) - GoBuster

[04:45](https://youtube.com/watch?v=d2nVDoVr0jE&t=285) - Getting banned and Pivoting to verify

[10:20](https://youtube.com/watch?v=d2nVDoVr0jE&t=620) - Logging into PFSense

[16:50](https://youtube.com/watch?v=d2nVDoVr0jE&t=1010) - Manually Exploiting PFsense 

[38:30](https://youtube.com/watch?v=d2nVDoVr0jE&t=2310) - Using Metasploit to exploit

[42:00](https://youtube.com/watch?v=d2nVDoVr0jE&t=2520) - Creating a Bruteforce Script in Python ( CSRF )

-----------------------------------------------------------

ippsec: [HackTheBox - Enterprise](https://youtube.com/watch?v=NWVJ2b0D1r8)



[01:00](https://youtube.com/watch?v=NWVJ2b0D1r8&t=60) - Begin of recon

[10:00](https://youtube.com/watch?v=NWVJ2b0D1r8&t=600) - Finding the vulnerable Wordpress Plugin

[17:50](https://youtube.com/watch?v=NWVJ2b0D1r8&t=1070) - Exploiting lcars plugin 

[28:30](https://youtube.com/watch?v=NWVJ2b0D1r8&t=1710) - Logging into WP and Getting Reverse Shell

[35:00](https://youtube.com/watch?v=NWVJ2b0D1r8&t=2100) - Wordpress RevShell Returned

[40:00](https://youtube.com/watch?v=NWVJ2b0D1r8&t=2400) - Using Meterpreter to pivot and provide access to MySQL

[50:00](https://youtube.com/watch?v=NWVJ2b0D1r8&t=3000) - MySQL Shell Returned

[52:00](https://youtube.com/watch?v=NWVJ2b0D1r8&t=3120) - Logging into Joomla and Getting Reverse Shell

[57:20](https://youtube.com/watch?v=NWVJ2b0D1r8&t=3440) - Joomla Reverse Shell returned

[59:00](https://youtube.com/watch?v=NWVJ2b0D1r8&t=3540) - Getting Reverse Shell on Host OS (port 443)

-----------------------------------------------------------

ippsec: [HackTheBox - Kotarak](https://youtube.com/watch?v=38e-sxPWiuY)



[01:38](https://youtube.com/watch?v=38e-sxPWiuY&t=98) - Start of nmap

[03:40](https://youtube.com/watch?v=38e-sxPWiuY&t=220) - Accessing port 60000

[06:20](https://youtube.com/watch?v=38e-sxPWiuY&t=380) - Manually enumerating ports on localhost via SSRF

[07:00](https://youtube.com/watch?v=38e-sxPWiuY&t=420) - Using wfuzz to portscan localhost via SSRF

[10:00](https://youtube.com/watch?v=38e-sxPWiuY&t=600) - Tomcat creds exposed & Uploading tomcat reverse shell

[13:40](https://youtube.com/watch?v=38e-sxPWiuY&t=820) - Return of shell

[14:20](https://youtube.com/watch?v=38e-sxPWiuY&t=860) - Extracting NTDS + SYSTEM Hive

[20:20](https://youtube.com/watch?v=38e-sxPWiuY&t=1220) - Using HashKiller to crack the hashes

[21:30](https://youtube.com/watch?v=38e-sxPWiuY&t=1290) - Escalating to Atanas & Identifying wget vulnerability

[27:10](https://youtube.com/watch?v=38e-sxPWiuY&t=1630) - Starting exploit

[33:22](https://youtube.com/watch?v=38e-sxPWiuY&t=2002) - Exploit failed, light debugging

[35:40](https://youtube.com/watch?v=38e-sxPWiuY&t=2140) - Issue found, not listening all interfaces

[39:35](https://youtube.com/watch?v=38e-sxPWiuY&t=2375) - Root shell returned.

[40:10](https://youtube.com/watch?v=38e-sxPWiuY&t=2410) - Unintentional Root Method (Edited Footage, IP Change)

-----------------------------------------------------------

ippsec: [HackTheBox - Node](https://youtube.com/watch?v=sW10TlZF62w)



[00:45](https://youtube.com/watch?v=sW10TlZF62w&t=45) - Begin of NMAP

[03:00](https://youtube.com/watch?v=sW10TlZF62w&t=180) - GoBuster (Fails)

[08:15](https://youtube.com/watch?v=sW10TlZF62w&t=495) - Screw GoBuster, BurpSpider FTW

[09:12](https://youtube.com/watch?v=sW10TlZF62w&t=552) - Examing Routes File to find more pages

[10:10](https://youtube.com/watch?v=sW10TlZF62w&t=610) - Finding Credentials and downloading backup

[14:45](https://youtube.com/watch?v=sW10TlZF62w&t=885) - Cracking the zip with fcrackzip

[16:45](https://youtube.com/watch?v=sW10TlZF62w&t=1005) - Finding more credentials (SSH) within MongoSource

[21:50](https://youtube.com/watch?v=sW10TlZF62w&t=1310) - Privesc to Tom User

[35:04](https://youtube.com/watch?v=sW10TlZF62w&t=2104) - Analyzing Backup Binary File

[36:49](https://youtube.com/watch?v=sW10TlZF62w&t=2209) - Using strace to find binary password

[40:25](https://youtube.com/watch?v=sW10TlZF62w&t=2425) - Finding blacklisted characters/words

[50:00](https://youtube.com/watch?v=sW10TlZF62w&t=3000) - Unintended method one, abusing CWD

[52:20](https://youtube.com/watch?v=sW10TlZF62w&t=3140) - Unintended method two, wildcards to bypass blacklist

[54:45](https://youtube.com/watch?v=sW10TlZF62w&t=3285) - Unintended method three, command injection via new line

[59:15](https://youtube.com/watch?v=sW10TlZF62w&t=3555) - Intended root Buffer Overflow ASLR Brute Force

-----------------------------------------------------------

ippsec: [HackTheBox - Mantis](https://youtube.com/watch?v=VVZZgqIyD0Q)



[01:20](https://youtube.com/watch?v=VVZZgqIyD0Q&t=80) - Start of nmap

[03:22](https://youtube.com/watch?v=VVZZgqIyD0Q&t=202) - Poking at a rabbit hole (8080)

[08:08](https://youtube.com/watch?v=VVZZgqIyD0Q&t=488) - GoBuster to find hidden directory

[09:50](https://youtube.com/watch?v=VVZZgqIyD0Q&t=590) - Finding SQL Creds in hidden directory

[13:40](https://youtube.com/watch?v=VVZZgqIyD0Q&t=820) - Using dbeaver to enumerate database

[16:50](https://youtube.com/watch?v=VVZZgqIyD0Q&t=1010) - Impacket-PSExec to Admin

[19:00](https://youtube.com/watch?v=VVZZgqIyD0Q&t=1140) - Proving James is not an Admin

[20:35](https://youtube.com/watch?v=VVZZgqIyD0Q&t=1235) - Using MSF to Enable Remote Desktop to do Incident Response

[27:00](https://youtube.com/watch?v=VVZZgqIyD0Q&t=1620) - Start of Remote Desktop Looking at Event Log + Active Directory

[31:00](https://youtube.com/watch?v=VVZZgqIyD0Q&t=1860) - Installing Sysmon to get better logs

[36:15](https://youtube.com/watch?v=VVZZgqIyD0Q&t=2175) - Looking at Sysmon Logs

[42:20](https://youtube.com/watch?v=VVZZgqIyD0Q&t=2540) - Proving the PrivEsc was due to Impacket-PSExec not cleaning up

[48:00](https://youtube.com/watch?v=VVZZgqIyD0Q&t=2880) - Using Forensics to get Service Creation Date

[53:30](https://youtube.com/watch?v=VVZZgqIyD0Q&t=3210) - Finding a HTB User creating a Git Issue to Impacket (LOL)

[55:10](https://youtube.com/watch?v=VVZZgqIyD0Q&t=3310) - Intended Route - Forging a Kerberos Ticket MS14-068

71:00 - Explaining why the unintended route probably got created

-----------------------------------------------------------

ippsec: [HackTheBox - Shocker](https://youtube.com/watch?v=IBlTdguhgfY)



[00:39](https://youtube.com/watch?v=IBlTdguhgfY&t=39) - Begin Nmap, OS Enum via SSH/HTTP Banner

[05:00](https://youtube.com/watch?v=IBlTdguhgfY&t=300) - GoBuster

[07:08](https://youtube.com/watch?v=IBlTdguhgfY&t=428) - Viewing CGI Script

[08:50](https://youtube.com/watch?v=IBlTdguhgfY&t=530) - Begin NMAP Shellshock

[09:50](https://youtube.com/watch?v=IBlTdguhgfY&t=590) - Debugging Nmap HTTP Scripts via Burp

[11:10](https://youtube.com/watch?v=IBlTdguhgfY&t=670) - Fixing the HTTP Request & nmap script

[14:45](https://youtube.com/watch?v=IBlTdguhgfY&t=885) - Performing Shellshock & more fixing

[18:25](https://youtube.com/watch?v=IBlTdguhgfY&t=1105) - Getting a reverse shell

[21:19](https://youtube.com/watch?v=IBlTdguhgfY&t=1279) - Running LinEnum.sh

[23:00](https://youtube.com/watch?v=IBlTdguhgfY&t=1380) - Rooting the box

-----------------------------------------------------------

ippsec: [HackTheBox - Mirai](https://youtube.com/watch?v=SRmvRGUuuno)



[00:49](https://youtube.com/watch?v=SRmvRGUuuno&t=49) - Nmap

[01:31](https://youtube.com/watch?v=SRmvRGUuuno&t=91) - Examining some odd behavior. Nmap different result than browser.

[04:00](https://youtube.com/watch?v=SRmvRGUuuno&t=240) - Getting to /admin and testing for Zone Transfer

[05:40](https://youtube.com/watch?v=SRmvRGUuuno&t=340) - Testing SSH Default Raspberry Pi Creds

[06:11](https://youtube.com/watch?v=SRmvRGUuuno&t=371) - Escalate to root 'sudo su'

[07:10](https://youtube.com/watch?v=SRmvRGUuuno&t=430) - Recovering the deleted root.txt

[08:38](https://youtube.com/watch?v=SRmvRGUuuno&t=518) - GrepFu

[10:40](https://youtube.com/watch?v=SRmvRGUuuno&t=640) - Downloading /dev/sdb via SSH

[12:48](https://youtube.com/watch?v=SRmvRGUuuno&t=768) - Running Binwalk against it

[13:18](https://youtube.com/watch?v=SRmvRGUuuno&t=798) - Trying to recover with TestDisk

[14:37](https://youtube.com/watch?v=SRmvRGUuuno&t=877) - Trying to recover with PhotoRec

-----------------------------------------------------------

ippsec: [HackTheBox - Shrek](https://youtube.com/watch?v=tI592BjTd4o)



[01:00](https://youtube.com/watch?v=tI592BjTd4o&t=60) - Nmap

[02:23](https://youtube.com/watch?v=tI592BjTd4o&t=143) - Examining the Web Page

[04:08](https://youtube.com/watch?v=tI592BjTd4o&t=248) - GoBuster

[04:53](https://youtube.com/watch?v=tI592BjTd4o&t=293) - Finding /uploads/ Directory

[05:50](https://youtube.com/watch?v=tI592BjTd4o&t=350) - Finding /secret_area_51/ Directory

[06:20](https://youtube.com/watch?v=tI592BjTd4o&t=380) - Using Audacity to find Steg in Audio

[08:50](https://youtube.com/watch?v=tI592BjTd4o&t=530) - FTP With Creds revealed from Steg

[10:06](https://youtube.com/watch?v=tI592BjTd4o&t=606) - Examining files downloaded from FTP

[12:43](https://youtube.com/watch?v=tI592BjTd4o&t=763) - Finding decryption key + blob

[14:33](https://youtube.com/watch?v=tI592BjTd4o&t=873) - Using Python seccure to decrypt ecc

[16:05](https://youtube.com/watch?v=tI592BjTd4o&t=965) - SSH Into Shrek as SEC

[16:35](https://youtube.com/watch?v=tI592BjTd4o&t=995) - Farquad Rabbit Hole

[17:42](https://youtube.com/watch?v=tI592BjTd4o&t=1062) - Incident Response : Finding files modified between two times

[20:47](https://youtube.com/watch?v=tI592BjTd4o&t=1247) - What is /usr/src/thoughts.txt?

[21:45](https://youtube.com/watch?v=tI592BjTd4o&t=1305) - Privesc through cron running: chown *

-----------------------------------------------------------

HackTheBox - SolidState
https://youtube.com/watch?v=_QapCUx55Xk

-----------------------------------------------------------

ippsec: [HackTheBox - Calamity](https://youtube.com/watch?v=EloOaaGg3nA)



[01:28](https://youtube.com/watch?v=EloOaaGg3nA&t=88) - Begin of recon

[02:20](https://youtube.com/watch?v=EloOaaGg3nA&t=140) - GoBuster

[03:30](https://youtube.com/watch?v=EloOaaGg3nA&t=210) - admin.php discovered, finding the pw

[04:50](https://youtube.com/watch?v=EloOaaGg3nA&t=290) - Getting Code Execution

[07:45](https://youtube.com/watch?v=EloOaaGg3nA&t=465) - Finding out why Reverse Shells weren't working

[09:45](https://youtube.com/watch?v=EloOaaGg3nA&t=585) - Getting a reverse shell by renaming nc

[11:30](https://youtube.com/watch?v=EloOaaGg3nA&t=690) - Transfering files via nc

[14:00](https://youtube.com/watch?v=EloOaaGg3nA&t=840) - Opening the wav file

[16:25](https://youtube.com/watch?v=EloOaaGg3nA&t=985) - Using audiodiff to identify differences in sound

[17:05](https://youtube.com/watch?v=EloOaaGg3nA&t=1025) - The next step, why is the same song there twice?

[19:25](https://youtube.com/watch?v=EloOaaGg3nA&t=1165) - Importing files into Audacity and Inverting

[22:25](https://youtube.com/watch?v=EloOaaGg3nA&t=1345) - Attempting to exploit the process blacklist

[24:25](https://youtube.com/watch?v=EloOaaGg3nA&t=1465) - Unintended root LXC Background

[28:30](https://youtube.com/watch?v=EloOaaGg3nA&t=1710) - Creating an Alpine LXC

[30:40](https://youtube.com/watch?v=EloOaaGg3nA&t=1840) - Importing the image into lxc

[32:00](https://youtube.com/watch?v=EloOaaGg3nA&t=1920) - Creating the container

[32:40](https://youtube.com/watch?v=EloOaaGg3nA&t=1960) - Adding the host drive to container

[34:20](https://youtube.com/watch?v=EloOaaGg3nA&t=2060) - Starting the container and entering it

[35:05](https://youtube.com/watch?v=EloOaaGg3nA&t=2105) - Examining the Process Blacklist script 

[35:54](https://youtube.com/watch?v=EloOaaGg3nA&t=2154) - Running through the exploit again on a Ubuntu Host

-----------------------------------------------------------

ippsec: [HackTheBox - Blue](https://youtube.com/watch?v=YRsfX6DW10E)



[00:38](https://youtube.com/watch?v=YRsfX6DW10E&t=38) - Start of Recon

[01:20](https://youtube.com/watch?v=YRsfX6DW10E&t=80) - Finding NMAP Scripts (Probably a stupid way)

[02:00](https://youtube.com/watch?v=YRsfX6DW10E&t=120) - Running Safe Scripts - Not -sC, which is default.

[02:52](https://youtube.com/watch?v=YRsfX6DW10E&t=172) - Listing NMAP Script Categories (Prob a really stupid way)

[03:18](https://youtube.com/watch?v=YRsfX6DW10E&t=198) - Really Cool Grep (Only show matching -oP)

[04:40](https://youtube.com/watch?v=YRsfX6DW10E&t=280) - Nmap Safe Script Output

[06:30](https://youtube.com/watch?v=YRsfX6DW10E&t=390) - Exploiting MS17-010 with MSF

[07:40](https://youtube.com/watch?v=YRsfX6DW10E&t=460) - Setting up Dev Branch of Empire

[09:07](https://youtube.com/watch?v=YRsfX6DW10E&t=547) - Starting a Listener

[10:55](https://youtube.com/watch?v=YRsfX6DW10E&t=655) - Getting a PowerShell Oneliner to launch payload

[12:16](https://youtube.com/watch?v=YRsfX6DW10E&t=736) - Invoke-Expression (IEX) to Execute Launcher

[13:25](https://youtube.com/watch?v=YRsfX6DW10E&t=805) - Interacting with a single agent

[13:40](https://youtube.com/watch?v=YRsfX6DW10E&t=820) - Using Modules - PowerUp Invoke-AllChecks

[14:40](https://youtube.com/watch?v=YRsfX6DW10E&t=880) - Fixing weird issue with PS Module

[16:15](https://youtube.com/watch?v=YRsfX6DW10E&t=975) - Invoke-AllChecks finished

[17:15](https://youtube.com/watch?v=YRsfX6DW10E&t=1035) - Loading PS Modules into Memory

[17:40](https://youtube.com/watch?v=YRsfX6DW10E&t=1060) - Executing funcitons out of above module

[18:20](https://youtube.com/watch?v=YRsfX6DW10E&t=1100) - Why I don't pass to MSF via InjectShellcode

[22:45](https://youtube.com/watch?v=YRsfX6DW10E&t=1365) - How I pass from Empire to MSF (Unicorn + IEX)

[25:53](https://youtube.com/watch?v=YRsfX6DW10E&t=1553) - Just running Powershell CMDs from Empire (Shell)

-----------------------------------------------------------

ippsec: [HackTheBox - Jail](https://youtube.com/watch?v=80-73OYcrrk)



[00:52](https://youtube.com/watch?v=80-73OYcrrk&t=52) - Recon - NMAP

[04:05](https://youtube.com/watch?v=80-73OYcrrk&t=245) - Recon - Getting Linux Distro

[04:35](https://youtube.com/watch?v=80-73OYcrrk&t=275) - Recon - GoBuster

[05:40](https://youtube.com/watch?v=80-73OYcrrk&t=340) - Analyzing Jail.c source

[09:45](https://youtube.com/watch?v=80-73OYcrrk&t=585) - Begin Binary Exploitation

[15:10](https://youtube.com/watch?v=80-73OYcrrk&t=910) - Verify Buffer Overflow

[17:35](https://youtube.com/watch?v=80-73OYcrrk&t=1055) - Create Exploit Skeleton

[20:50](https://youtube.com/watch?v=80-73OYcrrk&t=1250) - Finding EIP Overwrite

[23:02](https://youtube.com/watch?v=80-73OYcrrk&t=1382) - Adding Reverse TCP Shellcode

[30:15](https://youtube.com/watch?v=80-73OYcrrk&t=1815) - Switching to "Socket Re-Use" Shellcode

[32:20](https://youtube.com/watch?v=80-73OYcrrk&t=1940) - Shell Returned

[34:00](https://youtube.com/watch?v=80-73OYcrrk&t=2040) - NFSv3 Privesc Begin

[40:15](https://youtube.com/watch?v=80-73OYcrrk&t=2415) - Begin incorrectly playing with SetUID

[43:10](https://youtube.com/watch?v=80-73OYcrrk&t=2590) - SELinux Escape

[45:25](https://youtube.com/watch?v=80-73OYcrrk&t=2725) - Using SELinux Escape to copy SSH Key

[48:55](https://youtube.com/watch?v=80-73OYcrrk&t=2935) - Logging in as Frank

[50:00](https://youtube.com/watch?v=80-73OYcrrk&t=3000) - Privesc to adm (sudo rvim)

[51:44](https://youtube.com/watch?v=80-73OYcrrk&t=3104) - Begin of finding a way to root

[55:58](https://youtube.com/watch?v=80-73OYcrrk&t=3358) - Begin cracking rar file 

[57:18](https://youtube.com/watch?v=80-73OYcrrk&t=3438) - Using Hashcat to generate custom wordlist

60:40 - Cracking with JohnTheRipper

62:30 - RsaCtfTool to exploit weak SSH Pub Key

63:36 - Login as root with SSH Private Key

64:11 - EXTRA CONTENT: Alternative Privesc to ADM (NFS)

65:21 - Creating a directory to give other users NFS Write access

67:30 - Correct way to do SetUID Program

71:04 - Using SetUID Programs to write to disk

-----------------------------------------------------------

ippsec: [HackTheBox - Nineveh](https://youtube.com/watch?v=K9DKULxSBK4)



[00:00](https://youtube.com/watch?v=K9DKULxSBK4&t=0) - Intro

[01:58](https://youtube.com/watch?v=K9DKULxSBK4&t=118) - Begin Recon (NMAP)

[04:19](https://youtube.com/watch?v=K9DKULxSBK4&t=259) - GoBuster HTTP + HTTPS

[06:35](https://youtube.com/watch?v=K9DKULxSBK4&t=395) - Accessing Pages 

[07:05](https://youtube.com/watch?v=K9DKULxSBK4&t=425) - Using Hydra against HTTP + HTTPS Web Forms

[11:30](https://youtube.com/watch?v=K9DKULxSBK4&t=690) - Logging into HTTP and hunting for vulns

[17:00](https://youtube.com/watch?v=K9DKULxSBK4&t=1020) - Second Hydra attempt against HTTPS

[17:57](https://youtube.com/watch?v=K9DKULxSBK4&t=1077) - Logging into HTTPS (phpLiteAdmin)

[20:17](https://youtube.com/watch?v=K9DKULxSBK4&t=1217) - Chaining Exploits to get Code Execution

[26:38](https://youtube.com/watch?v=K9DKULxSBK4&t=1598) - Reverse Shell Returned

[28:00](https://youtube.com/watch?v=K9DKULxSBK4&t=1680) - LinEnum.sh Script Review

[31:30](https://youtube.com/watch?v=K9DKULxSBK4&t=1890) - Watching for new Processes

[37:00](https://youtube.com/watch?v=K9DKULxSBK4&t=2220) - Found the error in script :)

[39:30](https://youtube.com/watch?v=K9DKULxSBK4&t=2370) - Getting reverse root shell

[41:51](https://youtube.com/watch?v=K9DKULxSBK4&t=2511) - Intended Route to get User

[46:12](https://youtube.com/watch?v=K9DKULxSBK4&t=2772) - Reviewing Knockd configuration

[49:33](https://youtube.com/watch?v=K9DKULxSBK4&t=2973) - Doing the PortKnock

-----------------------------------------------------------

ippsec: [HackTheBox - Blocky](https://youtube.com/watch?v=C2O-rilXA6I)



[01:15](https://youtube.com/watch?v=C2O-rilXA6I&t=75) - Begin Recon with Reconnoitre

[03:15](https://youtube.com/watch?v=C2O-rilXA6I&t=195) - Examining findings from Reconnoitre

[06:50](https://youtube.com/watch?v=C2O-rilXA6I&t=410) - Decompiling java Jar Files with JAD

[08:18](https://youtube.com/watch?v=C2O-rilXA6I&t=498) - Using JD-GUI

[10:33](https://youtube.com/watch?v=C2O-rilXA6I&t=633) - Running WPScan

[12:10](https://youtube.com/watch?v=C2O-rilXA6I&t=730) - Manually enumerating wordpress users

[12:43](https://youtube.com/watch?v=C2O-rilXA6I&t=763) - SSH To the box and PrivEsc

[15:30](https://youtube.com/watch?v=C2O-rilXA6I&t=930) - Rabbit hole, gaining access through FTP

[17:09](https://youtube.com/watch?v=C2O-rilXA6I&t=1029) - Finding Wordpress DB Password

[18:33](https://youtube.com/watch?v=C2O-rilXA6I&t=1113) - Switching to WWW-DATA by using phpMyAdmin + Wordpress

[20:10](https://youtube.com/watch?v=C2O-rilXA6I&t=1210) - Generating a PHP Password for Wordpress

[21:50](https://youtube.com/watch?v=C2O-rilXA6I&t=1310) - Gaining code execution with Wordpress Admin access

[25:40](https://youtube.com/watch?v=C2O-rilXA6I&t=1540) - Shell as www-data

[26:40](https://youtube.com/watch?v=C2O-rilXA6I&t=1600) - Enumerating Kernel Exploits with Linux-Exploit-Suggester

[30:10](https://youtube.com/watch?v=C2O-rilXA6I&t=1810) - Attempting CVE-2017-6074 Dccp Kernel Exploit (Unstable AF)

-----------------------------------------------------------

ippsec: [HackTheBox - Europa](https://youtube.com/watch?v=OsxDB41jg6A)



[00:24](https://youtube.com/watch?v=OsxDB41jg6A&t=24) - Recon with Sparta

[02:00](https://youtube.com/watch?v=OsxDB41jg6A&t=120) - Enumerating SSL Certificate 

[03:55](https://youtube.com/watch?v=OsxDB41jg6A&t=235) - Manually View SSL Certificate

[04:35](https://youtube.com/watch?v=OsxDB41jg6A&t=275) - VirtualHostRouting Explanation

[07:42](https://youtube.com/watch?v=OsxDB41jg6A&t=462) - SQL Injection - Auth Bypass

[13:00](https://youtube.com/watch?v=OsxDB41jg6A&t=780) - Dumping the Database with SQLMap

[16:45](https://youtube.com/watch?v=OsxDB41jg6A&t=1005) - Begin of Web Exploit (Regex //e)

[23:00](https://youtube.com/watch?v=OsxDB41jg6A&t=1380) - Getting a Shell

[27:10](https://youtube.com/watch?v=OsxDB41jg6A&t=1630) - Begin PrivEsc (CronJob)

-----------------------------------------------------------

ippsec: [HackTheBox - Apocalyst](https://youtube.com/watch?v=TJVghYBByIA)



[01:26](https://youtube.com/watch?v=TJVghYBByIA&t=86) - Enumeration Start

[02:58](https://youtube.com/watch?v=TJVghYBByIA&t=178) - WPScan Start

[05:40](https://youtube.com/watch?v=TJVghYBByIA&t=340) - Directory Scanning with GoBuster

[10:54](https://youtube.com/watch?v=TJVghYBByIA&t=654) - Examining WPScan Output

[13:40](https://youtube.com/watch?v=TJVghYBByIA&t=820) - Bruteforcing with WPScan

[14:40](https://youtube.com/watch?v=TJVghYBByIA&t=880) - Bruteforcing HTTP Post with Hydra

[18:30](https://youtube.com/watch?v=TJVghYBByIA&t=1110) - Edit WP Theme to get Code Execution

[22:09](https://youtube.com/watch?v=TJVghYBByIA&t=1329) - Return of Reverse Shell

[26:25](https://youtube.com/watch?v=TJVghYBByIA&t=1585) - Privelege Escalation Word Writeable Passwd

-----------------------------------------------------------

ippsec: [HackTheBox - Holiday](https://youtube.com/watch?v=FvHyt7KrsPE)



[00:46](https://youtube.com/watch?v=FvHyt7KrsPE&t=46) - NMAP Scan and Review

[01:53](https://youtube.com/watch?v=FvHyt7KrsPE&t=113) - GoBuster and identify User Agent based Routing

[04:09](https://youtube.com/watch?v=FvHyt7KrsPE&t=249) - SQLMap the Login

[08:00](https://youtube.com/watch?v=FvHyt7KrsPE&t=480) - Login to the page

[08:55](https://youtube.com/watch?v=FvHyt7KrsPE&t=535) - Begin of XSS

[11:15](https://youtube.com/watch?v=FvHyt7KrsPE&t=675) - Bypass first XSS Filter

[14:45](https://youtube.com/watch?v=FvHyt7KrsPE&t=885) - Encoded JS Payload - Getting XSS to call back to us

[16:56](https://youtube.com/watch?v=FvHyt7KrsPE&t=1016) - Using Python to encode JS which will call back to us.

[24:25](https://youtube.com/watch?v=FvHyt7KrsPE&t=1465) - Executing the paylaod

[25:06](https://youtube.com/watch?v=FvHyt7KrsPE&t=1506) - Stage 2 XSS Attack - XMLHttpRequest

[31:30](https://youtube.com/watch?v=FvHyt7KrsPE&t=1890) - Troubleshooting, No code works the first time.

[36:00](https://youtube.com/watch?v=FvHyt7KrsPE&t=2160) - Stage 2 Fixed.

[40:57](https://youtube.com/watch?v=FvHyt7KrsPE&t=2457) - Initial access to /admin

[42:00](https://youtube.com/watch?v=FvHyt7KrsPE&t=2520) - Finding Command Injection

[43:40](https://youtube.com/watch?v=FvHyt7KrsPE&t=2620) - Explanation of IP "Encoding"

[48:40](https://youtube.com/watch?v=FvHyt7KrsPE&t=2920) - Rev Shell obtained

[49:30](https://youtube.com/watch?v=FvHyt7KrsPE&t=2970) - How I found out about the IP Encode Trick

[51:40](https://youtube.com/watch?v=FvHyt7KrsPE&t=3100) - Begin of PrivEsc

-----------------------------------------------------------

ippsec: [HackTheBox - Sneaky](https://youtube.com/watch?v=1UGxjqTnuyo)



[00:00](https://youtube.com/watch?v=1UGxjqTnuyo&t=0) - Intro

[00:44](https://youtube.com/watch?v=1UGxjqTnuyo&t=44) - Recon + Web Enum

[01:33](https://youtube.com/watch?v=1UGxjqTnuyo&t=93) - SQL Injection

[05:30](https://youtube.com/watch?v=1UGxjqTnuyo&t=330) - Start of IPv6 Talk

[06:30](https://youtube.com/watch?v=1UGxjqTnuyo&t=390) - What is an IPv6 IP Address?

[11:27](https://youtube.com/watch?v=1UGxjqTnuyo&t=687) - Types of IPv6 Addresses

[14:06](https://youtube.com/watch?v=1UGxjqTnuyo&t=846) - IPv6 Subnetting Explained

[21:20](https://youtube.com/watch?v=1UGxjqTnuyo&t=1280) - End of IPv6 Primer, Exploit time!

[22:43](https://youtube.com/watch?v=1UGxjqTnuyo&t=1363) - Method 1: Getting MAC and calculating fe80

[30:30](https://youtube.com/watch?v=1UGxjqTnuyo&t=1830) - Method 2: Enumerating Networks by pinging Multicast

[33:56](https://youtube.com/watch?v=1UGxjqTnuyo&t=2036) - Extra: Getting Windows to respond from Multicast Ping

[38:07](https://youtube.com/watch?v=1UGxjqTnuyo&t=2287) - Extra: NMAP Scanning ipv6 local networks

[40:15](https://youtube.com/watch?v=1UGxjqTnuyo&t=2415) - Convert RPM to DEB (Needed for install nmap on tenten)

[41:30](https://youtube.com/watch?v=1UGxjqTnuyo&t=2490) - Intended Solution: Getting IPv6 via SNMP

[43:58](https://youtube.com/watch?v=1UGxjqTnuyo&t=2638) - No SNMP MIB Output

[45:58](https://youtube.com/watch?v=1UGxjqTnuyo&t=2758) - Getting SNMP MIBS Installed and Configured

[47:52](https://youtube.com/watch?v=1UGxjqTnuyo&t=2872) - Tool: Enyx - SNMPv6 Enumeration via Python

[50:44](https://youtube.com/watch?v=1UGxjqTnuyo&t=3044) - Privesc Enumeration

[52:49](https://youtube.com/watch?v=1UGxjqTnuyo&t=3169) - Buffer Overflow

-----------------------------------------------------------

ippsec: [HackTheBox - Charon](https://youtube.com/watch?v=_csbKuOlmdE)



[12:04](https://youtube.com/watch?v=_csbKuOlmdE&t=724) - Finding PHP Files in /cmsdata/ (GoBuster)

[12:53](https://youtube.com/watch?v=_csbKuOlmdE&t=773) - Manual Identification of SQL Injection

[15:50](https://youtube.com/watch?v=_csbKuOlmdE&t=950) - SQL Injection Explanation

[17:20](https://youtube.com/watch?v=_csbKuOlmdE&t=1040) - Rabbit Hole - Starting SQLMap in the Background

[18:10](https://youtube.com/watch?v=_csbKuOlmdE&t=1090) - SQL Union Injection Explanation

[19:30](https://youtube.com/watch?v=_csbKuOlmdE&t=1170) - Identifying "Bad/Filtered Words" in SQL Injection

[21:02](https://youtube.com/watch?v=_csbKuOlmdE&t=1262) - SQL Union Finding number of items returned

[21:48](https://youtube.com/watch?v=_csbKuOlmdE&t=1308) - Returning data from Union Injection

[22:48](https://youtube.com/watch?v=_csbKuOlmdE&t=1368) - SQL Concat Explanation

[23:55](https://youtube.com/watch?v=_csbKuOlmdE&t=1435) - Enumerating SQL Databases Explanation (Information_Schema)

[25:46](https://youtube.com/watch?v=_csbKuOlmdE&t=1546) - Returning Database, Table, Columns from Information_Schema

[29:30](https://youtube.com/watch?v=_csbKuOlmdE&t=1770) - Scripting to dump all columns

[36:45](https://youtube.com/watch?v=_csbKuOlmdE&t=2205) - Listing of columns in SuperCMS

[37:15](https://youtube.com/watch?v=_csbKuOlmdE&t=2235) - Dumping User Credentials

[41:36](https://youtube.com/watch?v=_csbKuOlmdE&t=2496) - Logging in and exploiting SuperCMS

[47:00](https://youtube.com/watch?v=_csbKuOlmdE&t=2820) - Return of reverse shell

[48:40](https://youtube.com/watch?v=_csbKuOlmdE&t=2920) - Transfering small files from shell to my machine

[50:56](https://youtube.com/watch?v=_csbKuOlmdE&t=3056) - Using RsaCtfTool to decrypt contents with weak public key

[52:52](https://youtube.com/watch?v=_csbKuOlmdE&t=3172) - Breaking weak RSA manually

-----------------------------------------------------------

HackTheBox - Pivoting Update: Granny and Grandpa
https://youtube.com/watch?v=HQkDL-xh7es

-----------------------------------------------------------

ippsec: [HackTheBox - Granny and Grandpa](https://youtube.com/watch?v=ZfPVGJGkORQ)



[13:00](https://youtube.com/watch?v=ZfPVGJGkORQ&t=780) - User Shell Returned

[16:23](https://youtube.com/watch?v=ZfPVGJGkORQ&t=983) - Get Admin Shell (ms14-070)

[17:14](https://youtube.com/watch?v=ZfPVGJGkORQ&t=1034) - Beginning of Pivot Fail.  Socks Proxy

[29:35](https://youtube.com/watch?v=ZfPVGJGkORQ&t=1775) - Shell on Grandpa (CVE-2017-7269)

[32:45](https://youtube.com/watch?v=ZfPVGJGkORQ&t=1965) - Using portfwd to access ports not exposed to routable interfaces

[34:45](https://youtube.com/watch?v=ZfPVGJGkORQ&t=2085) - Cracking LM Hash Explanation

[38:30](https://youtube.com/watch?v=ZfPVGJGkORQ&t=2310) - Cracking LM Hashes via Hashcat

[41:30](https://youtube.com/watch?v=ZfPVGJGkORQ&t=2490) - Grandpa acts cranky.  Revert. 

[42:30](https://youtube.com/watch?v=ZfPVGJGkORQ&t=2550) - Expected behavior when exploiting via CVE-2017-7269.  None of that auto system weirdness (45:20 gets admin)

[45:50](https://youtube.com/watch?v=ZfPVGJGkORQ&t=2750) - Using Hashcat to crack NTLM using LM Hashes

[48:50](https://youtube.com/watch?v=ZfPVGJGkORQ&t=2930) - Finally log into SMB using the portfwd from 32:45

[49:07](https://youtube.com/watch?v=ZfPVGJGkORQ&t=2947) - Random pivot attempt failure.

-----------------------------------------------------------

ippsec: [HackTheBox - Optimum](https://youtube.com/watch?v=kWTnVBIpNsE)



[11:54](https://youtube.com/watch?v=kWTnVBIpNsE&t=714) - Shell returned

[13:15](https://youtube.com/watch?v=kWTnVBIpNsE&t=795) - Finding exploits with Sherlock

[15:15](https://youtube.com/watch?v=kWTnVBIpNsE&t=915) - Using Empire Module without Empire for Privesc

[21:00](https://youtube.com/watch?v=kWTnVBIpNsE&t=1260) - Start of doing the box with Metasploit

[22:36](https://youtube.com/watch?v=kWTnVBIpNsE&t=1356) - Reverse Shell Returned (x32)

[24:45](https://youtube.com/watch?v=kWTnVBIpNsE&t=1485) - MSF Error during PrivEsc

[25:35](https://youtube.com/watch?v=kWTnVBIpNsE&t=1535) - Reverse Shell Returned (x64)

[26:19](https://youtube.com/watch?v=kWTnVBIpNsE&t=1579) - Same PrivEsc as earlier, different result

[28:47](https://youtube.com/watch?v=kWTnVBIpNsE&t=1727) - Examining how Rejetto MSF Module works with Burp

-----------------------------------------------------------

ippsec: [HackTheBox - Devel](https://youtube.com/watch?v=2LNyAbroZUk)

0xdf: [HTB: Ethereal Shell Development](https://0xdf.gitlab.io//2019/03/09/htb-ethereal-shell.html)

0xdf: [HTB: Devel](https://0xdf.gitlab.io//2019/03/05/htb-devel.html)

[01:02](https://youtube.com/watch?v=2LNyAbroZUk&t=62) - Going over NMAP

[02:00](https://youtube.com/watch?v=2LNyAbroZUk&t=120) - Anonymous FTP + File Upload

[04:30](https://youtube.com/watch?v=2LNyAbroZUk&t=270) - MSFVenom 

[07:20](https://youtube.com/watch?v=2LNyAbroZUk&t=440) - Metasploit

[10:00](https://youtube.com/watch?v=2LNyAbroZUk&t=600) - Exploit Suggestor

[11:30](https://youtube.com/watch?v=2LNyAbroZUk&t=690) - Getting Root

-----------------------------------------------------------

ippsec: [HackTheBox - Lazy](https://youtube.com/watch?v=3VxZNflJqsw)



[00:39](https://youtube.com/watch?v=3VxZNflJqsw&t=39) - Basic Web Page Discovery

[03:30](https://youtube.com/watch?v=3VxZNflJqsw&t=210) - Examining Cookies - Pt1 (Burp Sequencer)

[05:05](https://youtube.com/watch?v=3VxZNflJqsw&t=305) - Fuzzing Usernames (2nd Order SQL Injection)

[07:15](https://youtube.com/watch?v=3VxZNflJqsw&t=435) - Examining Cookies - Pt2

[07:40](https://youtube.com/watch?v=3VxZNflJqsw&t=460) - Cookie Bitflip

[12:45](https://youtube.com/watch?v=3VxZNflJqsw&t=765) - Oracle Padding Attack - Pt1

[15:30](https://youtube.com/watch?v=3VxZNflJqsw&t=930) - Rooting the Box

[22:50](https://youtube.com/watch?v=3VxZNflJqsw&t=1370) - Oracle Padding Attack - Pt2

-----------------------------------------------------------

ippsec: [HackTheBox - Haircut](https://youtube.com/watch?v=9ZXG1qb8lUI)



[01:45](https://youtube.com/watch?v=9ZXG1qb8lUI&t=105) - GoBuster

[04:40](https://youtube.com/watch?v=9ZXG1qb8lUI&t=280) - Exploiting exposed.php

[11:40](https://youtube.com/watch?v=9ZXG1qb8lUI&t=700) - Getting Shell

[20:09](https://youtube.com/watch?v=9ZXG1qb8lUI&t=1209) - Screen Privesc

-----------------------------------------------------------

ippsec: [HackTheBox - Joker](https://youtube.com/watch?v=5wyvpJa9LdU)



[00:27](https://youtube.com/watch?v=5wyvpJa9LdU&t=27) - Port Enumeration

[02:54](https://youtube.com/watch?v=5wyvpJa9LdU&t=174) - UDP Port Review

[03:40](https://youtube.com/watch?v=5wyvpJa9LdU&t=220) - TFTP Enumeration

[06:30](https://youtube.com/watch?v=5wyvpJa9LdU&t=390) - Cracking Squid PW

[08:00](https://youtube.com/watch?v=5wyvpJa9LdU&t=480) - FoxyProxy Setup

[09:45](https://youtube.com/watch?v=5wyvpJa9LdU&t=585) - Burp Setup

[14:45](https://youtube.com/watch?v=5wyvpJa9LdU&t=885) - Running Commands

[21:20](https://youtube.com/watch?v=5wyvpJa9LdU&t=1280) - Reverse Shell

[22:30](https://youtube.com/watch?v=5wyvpJa9LdU&t=1350) - PrivEsc to Alekos #1

[28:00](https://youtube.com/watch?v=5wyvpJa9LdU&t=1680) - PrivEsc to Alekos #2

[30:37](https://youtube.com/watch?v=5wyvpJa9LdU&t=1837) - Root #1 (SymLink)

[30:48](https://youtube.com/watch?v=5wyvpJa9LdU&t=1848) - Root #2 (Tar Checkpoint)

[44:45](https://youtube.com/watch?v=5wyvpJa9LdU&t=2685) - Root #3 (Remove Development)

-----------------------------------------------------------

ippsec: [HackTheBox - Bank](https://youtube.com/watch?v=JRPWFSzFaG0)



[00:39](https://youtube.com/watch?v=JRPWFSzFaG0&t=39) - Nmap Results

[01:15](https://youtube.com/watch?v=JRPWFSzFaG0&t=75) - DNS Enumeration

[04:08](https://youtube.com/watch?v=JRPWFSzFaG0&t=248) - HTTP VirtualHost Routing

[05:28](https://youtube.com/watch?v=JRPWFSzFaG0&t=328) - DirSearch (Web Enumeration) 

[08:50](https://youtube.com/watch?v=JRPWFSzFaG0&t=530) - HTTP Redirect Vulnerability

[13:23](https://youtube.com/watch?v=JRPWFSzFaG0&t=803) - PW in Balance-Transfer

[18:00](https://youtube.com/watch?v=JRPWFSzFaG0&t=1080) - File Upload, WebShell

[21:48](https://youtube.com/watch?v=JRPWFSzFaG0&t=1308) - First Shell

[30:10](https://youtube.com/watch?v=JRPWFSzFaG0&t=1810) - First Privesc Method (SUID)

[31:38](https://youtube.com/watch?v=JRPWFSzFaG0&t=1898) - Second Privesc Method (passwd)

-----------------------------------------------------------

HackTheBox - Bastard
https://youtube.com/watch?v=lP-E5vmZNC0

-----------------------------------------------------------

ippsec: [HackTheBox - Beep](https://youtube.com/watch?v=XJmBpOd__N8)



[16:03](https://youtube.com/watch?v=XJmBpOd__N8&t=963) - Method 2: Turning LFI into RCE

[37:46](https://youtube.com/watch?v=XJmBpOd__N8&t=2266) - Method 3: Code exec via call

[54:00](https://youtube.com/watch?v=XJmBpOd__N8&t=3240) - Method 4: Shellshock

-----------------------------------------------------------

ippsec: [HackTheBox - Brainfuck](https://youtube.com/watch?v=o5x1yg3JnYI)



[10:30](https://youtube.com/watch?v=o5x1yg3JnYI&t=630) - Logged into WP

[15:00](https://youtube.com/watch?v=o5x1yg3JnYI&t=900) - Login to SuperSecretForum

[25:00](https://youtube.com/watch?v=o5x1yg3JnYI&t=1500) - Cracking the SSH Key

[27:15](https://youtube.com/watch?v=o5x1yg3JnYI&t=1635) - Begin of getting root.txt (RSA Cracking)

-----------------------------------------------------------

HackTheBox - CronOS
https://youtube.com/watch?v=CYeVUmOar3I

-----------------------------------------------------------

ippsec: [HackTheBox - October](https://youtube.com/watch?v=K05mJazHhF4)

0xdf: [HTB: October](https://0xdf.gitlab.io//2019/03/26/htb-october.html)

[00:45](https://youtube.com/watch?v=K05mJazHhF4&t=45) - Pulling up Web Page.

[01:10](https://youtube.com/watch?v=K05mJazHhF4&t=70) - Searchsploit

[02:40](https://youtube.com/watch?v=K05mJazHhF4&t=160) - Enumerating Version (Download Versions, Hash Static Files)

[08:20](https://youtube.com/watch?v=K05mJazHhF4&t=500) - Default cred /backend -- Upload Shell

[09:51](https://youtube.com/watch?v=K05mJazHhF4&t=591) - User Reverse Shell

[12:10](https://youtube.com/watch?v=K05mJazHhF4&t=730) - Transfering file over nc

[14:45](https://youtube.com/watch?v=K05mJazHhF4&t=885) - Begin "fuzzing" Binary

[16:15](https://youtube.com/watch?v=K05mJazHhF4&t=975) - GDB Analysis

[18:46](https://youtube.com/watch?v=K05mJazHhF4&t=1126) - Get a full reverse shell with tab autocomplete.

[19:00](https://youtube.com/watch?v=K05mJazHhF4&t=1140) - Showing ASLR changing address 

[20:20](https://youtube.com/watch?v=K05mJazHhF4&t=1220) - Disable ASLR on Exploit Dev Machine

[21:15](https://youtube.com/watch?v=K05mJazHhF4&t=1275) - Start of exploit development for ovrflw binary (Pattner_Create)

[27:27](https://youtube.com/watch?v=K05mJazHhF4&t=1647) - Start of Return to LibC attack - Getting Addresses

[37:20](https://youtube.com/watch?v=K05mJazHhF4&t=2240) - Grabbing memory locations off October Machine

[41:00](https://youtube.com/watch?v=K05mJazHhF4&t=2460) - Convert script to Bruteforce ASLR

-----------------------------------------------------------

ippsec: [HackTheBox - Arctic](https://youtube.com/watch?v=e9lVyFH7-4o)



[00:00](https://youtube.com/watch?v=e9lVyFH7-4o&t=0) - Intro

[00:12](https://youtube.com/watch?v=e9lVyFH7-4o&t=12) - Enumerate with nmap

[00:40](https://youtube.com/watch?v=e9lVyFH7-4o&t=40) - Going to the webpage

[01:50](https://youtube.com/watch?v=e9lVyFH7-4o&t=110) - Using SearchSploit to find ColdFusion Exploits

[02:40](https://youtube.com/watch?v=e9lVyFH7-4o&t=160) - Attempt to exploit through MSF. Debug why it failed.

[03:50](https://youtube.com/watch?v=e9lVyFH7-4o&t=230) - Setting up a Burp Redirect listener

[04:55](https://youtube.com/watch?v=e9lVyFH7-4o&t=295) - Examining request send by MSF Exploit

[06:35](https://youtube.com/watch?v=e9lVyFH7-4o&t=395) - Getting a reverse shell

[07:50](https://youtube.com/watch?v=e9lVyFH7-4o&t=470) - Using Unicorn to create a Powershell Meterpreter Loa

[11:35](https://youtube.com/watch?v=e9lVyFH7-4o&t=695) - Reverseshell returned

[12:10](https://youtube.com/watch?v=e9lVyFH7-4o&t=730) - Using the MSF post module local_exploit_suggestor

[15:29](https://youtube.com/watch?v=e9lVyFH7-4o&t=929) - Privesc via MS10-092

-----------------------------------------------------------

ippsec: [HackTheBox - Popcorn](https://youtube.com/watch?v=NMGsnPSm8iw)



[00:25](https://youtube.com/watch?v=NMGsnPSm8iw&t=25) - TMUX and Connecting to HTB

[02:00](https://youtube.com/watch?v=NMGsnPSm8iw&t=120) - Virtual Host Routing Explanation

[02:40](https://youtube.com/watch?v=NMGsnPSm8iw&t=160) - File Enumeration (Dirb)

[03:59](https://youtube.com/watch?v=NMGsnPSm8iw&t=239) - Discover of Web App

[05:45](https://youtube.com/watch?v=NMGsnPSm8iw&t=345) - Starting SQLMap in the Background

[09:30](https://youtube.com/watch?v=NMGsnPSm8iw&t=570) - Uploading a PHP Shell

[14:01](https://youtube.com/watch?v=NMGsnPSm8iw&t=841) - Python PTY Reverse Shell (Tab Autocomplete!)

[19:25](https://youtube.com/watch?v=NMGsnPSm8iw&t=1165) - MOTD Root (Method 1)

[23:50](https://youtube.com/watch?v=NMGsnPSm8iw&t=1430) - Dirtyc0w Root (Method 2)