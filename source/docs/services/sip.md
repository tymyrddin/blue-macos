# System integration protection (SIP)

Apple introduced System Integration Protection (SIP), designed to protect the most vulnerable parts of the Mac: SIP 
protects a few core areas of the drive where the operating system is installed, including `/System`, `/bin`, `/sbin`, 
`/usr` (but not `/usr/local`). Some symbolic links from `/etc`, `/tmp`, and `/var` are also protected, though the 
target directories themselves are not. 

The safety measure prevents processes without sufficient privileges (including admin users with root access) from 
writing to these folders and the files stored within.

The technology also prevents other "risky" operations too, like code injection. Apple is concerned that changes made to 
these parts of your system could put your Mac at risk and cause damage to the OS. Locking out root admin access 
safeguards your Mac against sudo-level commands executed remotely and locally.

If you want to use software that depends on modifications which change the way many core OS elements and first party 
apps function, you're going to have to disable SIP first, and reenable it afterwards. I wouldn't though. 
Why trust software that wants me to turn off such an important protection, even if only temporarily.
