# Set up the time machine and backups

The Time Machine works by creating historic backups of your Mac. It keeps older copies of files even after you edit or 
delete them, until a time when you need more storage for newer backups. Thanks to these historic backups, you can 
travel back in time to restore your Mac's data from days, weeks, or months ago.

Requirements are a large speedy solid-state drive with two partitions: a partition for the Time Machine backup and the 
other partition to store files.

## Partitioning the drive

* Connect the external hard drive to the Mac. 
* Go to Applications -> Utilities and launch Disk Utility
* Select the external drive from the sidebar and click the Partition button. 
* Use the Add (+) option to create a new partition and choose Name, Format, and Size for each partition by selecting it in the diagram.
  * The Time Machine partition must use the Mac OS Extended (Journaled) format.
  * The file storage partition can use any format. 
    * Choose ExFat if you plan to use it with Windows.
    * Otherwise choose Mac OS Extended (Journaled).
* Click Apply, followed by Partition.

## Set up time machine

* Go to System Preferences -> Time Machine
* Click Select Disk and choose the Time Machine partition

Time Machine backups will start from scratch from this date forward. After the first backup, you can automatically start 
a backup with Time Machine (check the Backup Up Automatically box), or start a backup manually by accessing the Time 
Machine menu and start the backup from there.

## Backups for the file storage partition

Create separate backups for anything in your file storage partition.

* [Acronis True Image](https://www.acronis.com/en-us/personal/buy-backup/)
* [Carbon Copy Cloner](https://bombich.com/download)
* [ChronoSync](https://www.econtechnologies.com/downloads/downloads.html)
* [Get Backup Pro](https://www.belightsoft.com/products/getbackup/downloads)
* [SuperDuper](https://shirt-pocket.com/SuperDuper/SuperDuperDescription.html)
