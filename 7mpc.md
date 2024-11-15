# Backup Restore

***

To bring up the Backup/Restore tab on the [System Utilities form](7mk0.md) select the Administrator - Backup/Restore menu item on the [main form](7jjr.md).

The controls on the Backup/Restore tab provide the means to make backups of the application database for the purpose of restoring at a later time, should the need arise.  They work when connected to an Access database or a local SQL Server database.  Backing up or restoring a remote SQL Server database is not allowed.&#x20;

## Auto Backup Settings

Use these controls to configure Expectations to automatically back up the database.  By setting the Auto Backup option to On and setting Days to the desired backup interval, a backup will automatically be performed when a user logs in and the backup interval has been exceeded.

## Auto Delete Settings

Use these controls to configure Expectations to automatically delete backups from the set of existing backups.  By setting the Auto Delete option to On and setting Days to the time period to keep a backup, a backup will automatically be deleted when a user logs in and the backup file is older than the time period.

## Manually Managing Backups

A backup of the database can be manually created by selecting the Backup button.  The new backup file will appear in the Existing Backups list with the name of the file indicating the date and time it was created.  To manually delete a backup file, select the backup in the Existing Backups list then click on the Delete button.  A confirmation dialog will be displayed, offering the opportunity to abort the delete.  Upon confirming to delete the backup it will be removed from the list of Existing Backups.

## Restoring The Database

The restore utility is used to restore the application database from an existing backup.  Before running the utility, all other Expectations forms must be closed.  Also, all connections to the shared database by other Expectations applications must be closed.  To restore the database, select a backup from the list of Existing Backups and click on the Restore button.  A confirmation dialog will be displayed.  At this point the operator can either continue the restore or abort.  Upon confirmation, the database is restored from the selected backup.   Before this happens, the user is automatically logged out of Expectations and the database connection is closed.  An error dialog window is displayed if any Expectations forms remain open or if other applications are connected to the shared database.  A restore complete dialog window notifies the user when finished.

\| WARNING:Restoring the database may result in user logins and\
passwords being changed.\&nbsp; It is important to know the login and\
password of at least one level 3 user in the backup database to keep from\
being locked out of the system.\&nbsp; As a precaution, prior to performing a\
restore it would be a good idea to save the existing �expectations.mdb� file to a\
backup folder.\&nbsp; |
-----------------------
