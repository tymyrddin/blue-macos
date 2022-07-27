# Password protect files and folders

You can protect all the files on your Mac by [encrypting a Vault (or entire drive) with FileVault](disk-encryption.md).

If you consider FileVault a bit of an overkill for your purposes, you can password protect your files and folders in 
different ways.

## iWork suite documents

If you have Pages, Keynote, or Numbers files with sensitive information, you can password protect those files.

* Open the file you want to protect
* Go to File -> Set Password
* Enter a Password
* Verify the password 
* If you want a hint to help you remember your password, enter a Password Hint 
* Set Password

## PDF Files in Preview

* Open the PDF file you want to protect (does not work for image files)
* Go to the File menu and then press the Option key. The Duplicate menu option becomes Save As. 
* Select the Save As option.
* On the Save dialog box, check the Encrypt box towards the bottom. 
* Enter a Password
* Verify the password
* Save

To remove the password protection from a PDF file, open the file, enter the password, use the Option key to access the 
Save As option again and uncheck the Encrypt option on the Save dialog box. Save the file with a new name and delete 
the old password protected file.

## Microsoft Word files

* Open the Word file you want to protect
* Click the Review tab, and then click Protect Document
* On the Password Protect dialog box, enter 
  * Password 
  * Optionally require a Password to modify the document
  * Optionally add other Protection to the document 
  * Optionally Remove personal information from this file on save
* Save

## Microsoft PowerPoint and Excel files

Password protecting a Microsoft Excel workbook is similar to protecting a PowerPoint presentation, but the dialog box is 
different.

* Go to File -> Passwords
* Under Password to open, check the "Encrypt this presentation and require a password to open" box. 
* On the Set a password for this presentation dialog box, enter 
  * New password
  * Verify the password
  * Click Set Password
* OK

To remove the password from the presentation, open it, go to File -> Passwords, and uncheck the "Encrypt this 
presentation and require a password to open" box.

## Password protect folders

Disk Utility can erase, format, repair, and partition hard drives. It can also can create an encrypted disk image, or a 
single file that contains the entire contents of a drive or other media like external USB drives, CDs, or DVDs.

* Copy the files you want to protect into a folder
* Open Disk Utility
* Go to File -> New Image -> Image from Folder
* Select the folder you want to encrypt and click Choose.
* In box enter
  * Enter a name for the disk image in the Save As box 
  * Where to store the DMG file
  * Encryption type (128-bit or 256-bit AES) (Enter a Password and then Verify the password)
  * Select read/write from the Image Format dropdown list
  * Save
* A progress dialog box appears and a message saying that the operation was successful
* Click Done
* Use Eraser to securely delete the original files

Disk Utility adds the disk image to your desktop. Double-click the disk image icon to access the files inside it. 
To access the files you added to the disk image, double-click on the DMG file and enter the password when prompted. 
Eject the disk image when you're done using it, so the files are password protected again.