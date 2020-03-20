# window-developer


## Windows Settings

### Disable Websearch
[How to](https://pureinfotech.com/disable-web-search-windows-10-version-1803/)

Its annoying to see web search when using the default search

### Clean storage
Removing hibernation storage since its not being used. `powercfg -h off` will delete the hiberation file found in storage. `powercfg -h on` if you need it again. 

### Windows Experimental Terminal
[terminal](https://github.com/microsoft/terminal)

`profiles.json` manages the terminal settings which is located in `c:\Users\me\AppData\Local\Packages\Microsoft.WindowsTerminal_<hash>\LocalState\profile.json`

I only used this to change the default terminal to the wsl, at which point I start using tmux. 

### Ubuntu WSL
[ubuntu 18.04](https://www.microsoft.com/en-us/p/ubuntu-1804-lts/9n9tngvndl3q?activetab=pivot:overviewtab)

Works well with the experimental terminal. There is a shared mount localed in `/mnt/<drive>`

### Firefox
[Shadow fox](https://github.com/overdodactyl/ShadowFox)

To use a darker theme

### Keyboard shortcuts
[stackexchange](https://superuser.com/a/1202601)
otherwise look at `keyboard_layout.reg` to make the changes.

### Bluetooth syncing
If you dualboot your computer and need to share bluetooth keys between the two system I found it easiest to get the key from windows partition, then switching over to the linux partition and configuring the bluetooth info there. It can generally be found in `/var/lib/bluetooth/[mac]/` 


[stackexchange](https://unix.stackexchange.com/a/255510)
`PsExec.exe -s -i regedit /e C:\BTKeys.reg HKEY_LOCAL_MACHINE\SYSTEM\ControlSet001\Services\BTHPORT\Parameters\Keys`
