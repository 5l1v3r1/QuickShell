# QuickShell

QuickShell allows you to instantly gain a local Shell on a Mac OS X Machine, in less than 3 Seconds, with the help of an HID USB Device (such as the Malduino, the Hak5 USB Rubber Ducky and more).

Unlike many other attacks, QuickShell does not require an Internet Connection to be successful.

## How to perform the Attack
1. Create a new Wi-Fi Network from your Computer, or have an Access Point do the job.
2. Set the SSID of the Network to `q`, its encryption type to `WEP` and its Password to `quick`. Take note of the local IP Address of the device.
3. Open up `QuickShell.txt` and replace `1.2.3.4` with your local IP Address.
4. Ensure the Access Point is physically near the victim machine.
5. On your side, connect to the Wi-Fi Network and open up Terminal.
6. Then, execute the following command: `nc -l 4444`. *This will listen for connections on port `4444` using Netcat. If you do not have Netcat installed on your System, I recommend using EggShell.*
7. Plug in the BadUSB on the victim machine, and as soon as the Terminal is closed, you may plug the BadUSB back out.

The attack has been successfully completed, and within a few seconds, a new connection should pop up on your Computer. Mission accomplished.

# Credits
PyInfect was created by [@0xCoto](https://github.com/0xCoto).
