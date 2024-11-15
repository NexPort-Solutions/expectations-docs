# Database Connection
-----

On a machine where the Expectations suite is installed for the first time, both Expectations and the Training & Development application are configured to connect to an MS Access database located in the application folder.&nbsp; Versions of the Expectations suite that are higher than v7.0.x will make use of an existing database configuration for Expectations and the Training & Development application, if present.

The Training & Development application attempts to establish a database connection upon launch.&nbsp; 
If successful, the [Login form](<tdlin.md>) appears after the splash screen goes away.&nbsp; If the Training & Development application is unable to establish a database connection, please do the following:

1. Exit Training & Development
2. Launch the main Expectations application
3. Use the File - Open Database menu item on the Expectations [main form](<7jjr.md>) to set the connection properties for both applications

Afterwards, launch Training & Development again.&nbsp; Once the connection is made to the database, the [Login form](<tdlin.md>) will appear.&nbsp;
It is also possible that, upon connection, the Training & Development application determines the connected database needs to be updated to the current version.&nbsp; If so, you will be prompted with the UPDATE DATABASE dialog where you may choose to update an older database.

Upon selecting 'Yes', you may also choose to automatically migrate an older MS Access database to SQL Server and update it using the [Conversion Options](<tdconv.md>) dialog, or you may have the option to keep using your existing MS Access database (see the referenced Conversion Options help topic).&nbsp; If your database is already of the current version, or if you wish to manually perform the switch over to using a SQL Server database, please do the following:

1. Exit Training & Development, including any UPDATE DATABASE or Conversion Options dialogs that may be open
2. Launch the main Expectations application
3. See the procedure in the Migrate to SQL Server section of the Expectations [Database Connection](<7mnk.md>) help topic.

> **NOTE** : At this time during the update process, Training & Development application records may only be migrated automatically (rather than manually) from an MS Access database to SQL Server.&nbsp; For those older MS Access databases which do not meet the criteria specified in the [Conversion Options](<tdconv.md>) help topic for updating 'in-place', please consider converting your database to SQL Server automatically.&nbsp; If migrating your older MS Access database to SQL Server is not feasible at this time and the "Keep MS Access" button is not enabled, please contact Smart Horizons for assistance in separating out the database into multiple MS Access databases (each of which may be updated separately by the software, as normal). 
-----