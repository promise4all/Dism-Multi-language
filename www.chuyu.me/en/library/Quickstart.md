# Quick Start
The core function of the program is to clean up the update, so you may need to feel the value of the program after installing the update.

## interface layout
As shown, from the tab(s) at the top of the screen, you can switch between different systems `(if you have multiple operating systems)`. The left is a list of features, you can choose the features you need. For the average user, click on the `space recycling` and you're good.

! [MainUI] (./ images / MainUI.png)

## clean system trash
<br>
We suggest that you do not perform Cleanup frequently, especially on SSD! It is generally recommended  to clean up once a month.

! [CleanupUI] (./ images / CleanupUI.png)

<br>
After the program starts, click on 'Disk Clean', to view this interface. Then select the items you want to clean up, click `Scan '(to get estimate of things that can be removed) or click` clean out' (no estimate of size, delete immediately). Finally, if you have a better cleanup project or suggestion, click 'Help - Feedback BUG` and submit your rules.

<br>
> Tips: Use orange logo projects at your own risk, while there are some side effects of certain projects, the selected program will pop up a warning box, be sure to double-check!

## backup system
As the saying goes, "spare no trouble", and now Dism++ can directly backup the current system WIM, ESD, Without entering Windows PE. Very simple to use, select the current system, click recovery - system backup can be.

![BackupImage] (./ images / BackupImage.png)

![BackupImage-WimPath] (./ images / BackupImage-WimPath.png)
<br> Enter the WIM file path, and finally click OK.
> If the WIM file already exists, it is automatically incremented to an existing WIM file and an incremental backup is performed.

In addition, in order to fix a system that can not be started use system restore, go to options - more settings -> enable integrated boot menu, After enabling the BCD startup item there will be an extra Dism ++,, you can use this option if necessary to restore your system.

## restore system
When the system crashes, you can use the system backup to restore, fast recovery of the computer environment. Dism ++ To reduce the difficulty of restoring the system, the program supports hot-restore mode. That is, users do not need to start PE directly on this machine to be able to restore. If your computer is a faulty, you can start Dism++, click on the recovery function - system Restore. Select WIM file path, click OK, as shown below.

![RecoveryImage] (./ images / RecoveryImage.png)

> Tips: If your system has failed to start, then through the BCD menu Dism++ `(need to open the integrated boot menu)` or start the PE for these steps.

<br> Quick Start is over, users who want to study in depth can refer to follow-up documents, I wish you all have fun.
