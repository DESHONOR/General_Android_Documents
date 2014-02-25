## Android Rules Usage:
(51-Android.rules is a udev scripts which allows for adb to detect your device under linux)


Download 51-Android.rules then open the terminal (make sure to replace username with your actual username) and cd into the directory you have the file
    `cd /path/to/file`
    
Once there copy it into the appropriate directory (need root access)
    `sudo cp 51-Android.rules /etc/udev/rules.d/`
    
If adb is already running kill it now
    `adb kill-server`
    
Connect device and finally run
    `adb devices`
    
Your device should now be detected by adb.
    
