# Time

This program allows you to decrement the system time instead of incrementing it, creating an effect of time going backwards. Such effect can be useful in certain scenarios.

## Prerequisites

To run this script, you need to have the following:

- A Unix-based operating system (e.g., Linux, macOS), or Microsoft Windows 10 or above.
- If you are using a Unix-based system, a bash shell, if you are using Windows, the ability to run PowerShell scripts.
- `sntp` command-line utility for Unix (usually pre-installed on most systems).

## How to Use

### macOS
1. Download the Unix Executable from the releases page.
2. You can move it to any preferred folder, like `Applications`, `Documents`, etc. Remember where you moved it!
3. Open the macOS terminal. You can do this with simply searching for it in spotlight, or opening it from `/Applications/Utilities/Terminal.app`
4. You need to set the permissions for this executable. Using the terminal, make it runnable by writing ```chmod +x /Applications/time-unix``` in the terminal. Of course, the path is where your file actually is: `chmod +x /Downloads/time-unix` if it is in the Downloads folder, etc.
6. After this, you need to navigate to the folder the app is in. You can do this by typing `cd Applications`, `cd Downloads`, etc., wherever the file is.
7. When you are there, you will be able to run the executable. Run it with this command: `sudo ./time-unix`
Done

### Windows
1. Download the Windows Executable from the releases page.
2. Right-click and choose "Run as administrator"!
Done

Note: Running with root/admin privileges is necessary to modify the system time. (If you live the sudo out, or just double-click the exe, it will not work.)

## Notes

- Press Ctrl+C to stop the script on both systems. This will reset your system time to the actual internet time from `time.cloudflare.com`.
- Be cautious when running this script, as it modifies the system time. Make sure to reset the time after running the script to avoid any potential issues. If it would not reset automatically for some reason, you can always use
`sudo sntp -sS time.cloudflare.com`
   ```c
     Start-Service w32time
     w32tm /config /manualpeerlist:"time.cloudflare.com" /syncfromflags:manual /reliable:YES
   w32tm /resync /force
   ```

Enjoy!
