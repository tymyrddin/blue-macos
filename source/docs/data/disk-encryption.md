# Enable full disk encryption using FileVault

FileVault is a built-in utility on your Mac that encrypts all the data on your hard drive. When FileVault is enabled, 
the contents of your drive cannot be accessed without a login password or recovery key.

FileVault is off by default, as most users may find that encrypting the entire drive is a bit overkill. Having to type 
a password to open a file and the time required to initially encrypt your entire drive may outweigh the security 
FileVault provides. For home use, in a non-threatening environment, maybe. As activist protecting land, animal and/or 
human rights, most likely not.

## Enable FileVault

* Go to System Preferences -> Security & Privacy and click the FileVault tab.
* Click the lock at the bottom to be able to make changes and enter your administrator password. 
* Click Turn On FileVault
* Choose how to unlock your disk and reset your password if you ever forget it:
  * Use iCloud (easier, but less secure)
  * Create a FileVault recovery key (store on paper and/or dedicated USB stick)

## Create a Vault

On a Mac, DMG files are usually associated with installing apps. DMG files can also be used as encrypted vaults to 
store sensitive files and folders. This feature is like using a program like VeraCrypt on Linux.

* Go to Disk Utility -> File -> New Image -> Blank Image and enter the information for the DMG file
  * File name in Save As
  * Where to save the file
  * Size of Vault
  * Format
  * Encryption type
* Enter a password when asked to secure the DMG file.

Once it is created, it is opened. It shows up in Finder and on the desktop as another drive. Move your private files and 
folders in it. 

* To lock it, eject it from its desktop icon like any other external hard drive connected to your Mac. 
* To open it, double-click on the file and enter your password.