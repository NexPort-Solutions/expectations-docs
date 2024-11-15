# System Utilities Form: Backup/Restore Tab 
---

To bring up the Backup/Restore tab on the 
[System 
Utilities form](<7mk0.md>) select the 
Administrator - Backup/Restore menu item on the
[main 
form](<7jjr.md>).

The controls on the Backup/Restore tab provide the means to make backups of the 
application database for the purpose of restoring at a later time, should the 
need arise.&nbsp; They work when connected to an Access database or a local SQL 
Server database.&nbsp; Backing up or restoring a remote SQL Server database is 
not allowed.&nbsp; 

## Auto Backup Settings

Use these controls to configure Expectations to automatically back up the 
database.&nbsp; By setting the Auto Backup option to On and setting Days to the 
desired backup interval, a backup will automatically be performed when a user 
logs in and the backup interval has been exceeded. 

## Auto Delete Settings 

Use these controls to configure Expectations to automatically delete backups 
from the set of existing backups.&nbsp; By setting the Auto Delete option to On 
and setting Days to the time period to keep a backup, a backup will 
automatically be deleted when a user logs in and the backup file is older than 
the time period.

## Manually Managing Backups 

A backup of the database can be manually created by selecting the Backup 
button.&nbsp; The new backup file will appear in the Existing Backups list with 
the name of the file indicating the date and time it was created.&nbsp; To 
manually delete a backup file, select the backup in the Existing Backups list 
then click on the Delete button.&nbsp; A confirmation dialog will be displayed, 
offering the opportunity to abort the delete.&nbsp; Upon confirming to delete 
the backup it will be removed from the list of Existing Backups.

## Restoring The Database 

The restore utility is used to restore the application database from an 
existing backup.&nbsp; 
Before running the utility, all other Expectations forms must be closed.&nbsp; Also, all 
connections to the shared database by other Expectations applications must be 
closed.&nbsp; To restore the database, select a backup from the list of Existing 
Backups and click on the Restore button.&nbsp; A confirmation dialog will be 
displayed.&nbsp; At this point the operator can either continue the restore or 
abort.&nbsp; Upon confirmation, the database is restored from the selected 
backup.&nbsp;&nbsp; Before this happens, the user is automatically logged out of 
Expectations and the database connection is closed.&nbsp; An error dialog window 
is displayed if any Expectations forms remain open or if other applications are 
connected to the shared database.&nbsp; A restore complete dialog window 
notifies the user when finished.

| <font size="3" color="#FF0000"><b>WARNING:</b></font><font color="#FF0000">Restoring the database may result in user logins and <br>    passwords being changed.&amp;nbsp; It is important to know the login and <br>    password of at least one level 3 user in the backup database to keep from <br>    being locked out of the system.&amp;nbsp; As a precaution, prior to performing a <br>    restore it would be a good idea to save the existing �expectations.mdb� file to a <br>    backup folder.&amp;nbsp; </font> |
---