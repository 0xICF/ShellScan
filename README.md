![Alt text](https://0xicf.files.wordpress.com/2014/10/shellshock.jpg "ShellScan - A simple Shellshock Vulnerability Scanner ")


ShellScan
============
ShellScan - A simple Shellshock Vulnerability Scanner in python allow cyber security researchers to explore and discover new application and systems that vulnerable to the ShellShock exploit.
ShellScan supports different BASH vulnerabilities: CVE-2014-6271 and CVE-2014-6278 to be tested by cyber security researchers in order to explore and discover new applications and systems that vulnerable to Shellshock exploit.

ShellScan developed for research purposes only, It is strongly recommended that you do not use this tool for illegal purposes. 



Download
-
https://github.com/0xICF/ShellScan



How to Use
-

1. Define a list of host to scan in /config/host.txt
2. Define a list of CGIs in /config/cgi.txt
3. Run ShellScan.py 



ShellScan will scan a list of hosts with a list of CGIs while trying to exploit the ShellShock vulnerability with different methods and payloads (CVE-2014-6271, CVE-2014-6278)


Example:

$ ./ShellScan.py config/host.txt config/cgi.txt


ShellScan tool will perform few different ShellShock vulnerability tests:

Test 1: uses the command sleep in different headers and check differences between delays. 

Test 2: uses the command ping -cX 127.0.0.1 and check differences between delays. 

Test 3: try to print a string and get it (causes a lot of False Positives)



Configuration
-
The ShellScan tool is receives a host list and a cgi list (see an example files at “config” directory) and the number of threads.

Note: While using threads, It uses only 1 thread per host to avoid time differences caused by multiple requests at the same time.

TIP: ShellScan can cause some False positives so it is better to retest the possible positives if having an issues.




WARNING
-
ShellScan allows a malicious attacker to execute a remote commands on a vulnerable target system.
0xICF will not be responsible for any damage that caused by using this tool.



Change log
-
October 03, 2014 - ShellScan v1.0 Beta

ShellScan is currently not the most portable code but... it works. 

Any improvement is always welcome.


Screenshots
- 

![Alt text](https://0xicf.files.wordpress.com/2014/10/shellscan_run.png "ShellScan is running- A simple Shellshock Vulnerability Scanner ")



 
Mailing list
-
blackpiano0xicf@yahoo.com

Authors
-
CarbonFiber51

BlackPian0


License
-
GPL v3

References
-
http://0xicf.wordpress.com

