# Time

This Bash script allows you to decrement the system time instead of incrementing it, creating an effect of time going backwards. Such effect can be useful in certain scenarios.

## Prerequisites

To run this script, you need to have the following:

- A Unix-based operating system (e.g., Linux, macOS), or Microsoft Windows 10 or above.
- If you are using a Unix-based system, a bash shell, if you are using Windows, the ability to run PowerShell scripts.
- `sntp` command-line utility for Unix (usually pre-installed on most systems).

## How to Use

1. Open a terminal window. On macOS you can do this with searching for it in Spotlight, or by going to `/Applications/Utilities` and opening `Terminal.app`.
3. Make the script executable by running the following command: `chmod +x /path/to/yourfile` eg.: `chmod +x /Users/yourprofilename/Downloads/time`
4. Run the script with root privileges using the following command: `sudo ./path/to/the/executable`

Note: Running with root privileges is necessary to modify the system time. (If you live the sudo out, it will not work.)

## Notes

- Press Ctrl+C to stop the script. This will reset the system time to the actual internet time from `time.cloudflare.com`.
- Be cautious when running this script, as it modifies the system time. Make sure to reset the time after running the script to avoid any potential issues. If it would not reset for some reason, you can always use `sudo sntp -sS time.cloudflare.com` on Unix to set the system time to a correct time.

Enjoy!
