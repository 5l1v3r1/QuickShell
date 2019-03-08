# QuickShell
* Author: 0xCoto
* Version: Version 1.0
* Target: Mac OS X

# Description
QuickShell allows you to instantly gain a local Shell on a Mac OS X Machine, in under 3 Seconds, with the help of the Hak5 [Bash Bunny](https://hakshop.com/products/bash-bunny)!

Unlike many other attacks, QuickShell does not require an Internet Connection to be successful.

## Performing the Attack
1. Create a new Wi-Fi Network from your Computer, or have an Access Point do the job.
2. Set the SSID of the Network to `q`, its encryption type to `WEP` and its Password to `quick`. Take note of the local IP Address of the device.
3. In the `6`th line of `payload.txt`, replace `1.2.3.4` with your local IP Address.
4. Ensure the Access Point is physically near the target machine.
5. On your side, connect to the Wi-Fi Network and open up Terminal.
6. Then, execute the following command: `nc -l 4444`: This will begin listening for connections on port `4444` using netcat.
7. Plug the Bash Bunny into the target machine, and as soon as the LED turns green, plug it out and walk away.

The payload has been successfully deployed on the target machine and within a few seconds, a new connection should pop up in netcat on your Computer. You now have full remote access of your target machine!

## Status
| LED              | Status                                |
| ---------------- | ------------------------------------- |
| Red              | Failed to open script file            |
| Amber            | Script Running                        |
| Green            | Finished                              |

# Credits
QuickShell was created by [@0xCoto](https://github.com/0xCoto).

p18183@PC210-10:~$ df -h
Filesystem                    Size  Used Avail Use% Mounted on
udev                          1.9G     0  1.9G   0% /dev
tmpfs                         387M   11M  376M   3% /run
/dev/sda5                     111G   11G   94G  11% /
tmpfs                         1.9G   55M  1.9G   3% /dev/shm
tmpfs                         5.0M  4.0K  5.0M   1% /run/lock
tmpfs                         1.9G     0  1.9G   0% /sys/fs/cgroup
//10.1.210.153/Homes/p18183/  165G   27G  130G  17% /tmp/home/p18183/SharedHomeDirectory
tmpfs                         387M   48K  387M   1% /run/user/260803895
p18183@PC210-10:~$ nc -zv 10.1.210.153 21
10.1.210.153: inverse host lookup failed: Unknown host
(UNKNOWN) [10.1.210.153] 21 (ftp) : Connection refused
p18183@PC210-10:~$ nc -zv 10.1.210.153 22
10.1.210.153: inverse host lookup failed: Unknown host
(UNKNOWN) [10.1.210.153] 22 (ssh) open
p18183@PC210-10:~$ nc -zv 10.1.210.153 23
10.1.210.153: inverse host lookup failed: Unknown host
(UNKNOWN) [10.1.210.153] 23 (telnet) : Connection refused
p18183@PC210-10:~$ nc -zv 10.1.210.153 22
10.1.210.153: inverse host lookup failed: Unknown host
(UNKNOWN) [10.1.210.153] 22 (ssh) open
p18183@PC210-10:~$ ^C
p18183@PC210-10:~$ 
