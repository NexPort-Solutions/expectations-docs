# Convert older database from MS Access to SQL Server 
-----

<u>Conversion Options Window</u>

After confirming to update an older MS Access database from the UPDATE DATABASE dialog, the Conversion Options dialog will appear:

While the use of the provided MS Access database may be ideal for those facilities with only a handful of workstations using Expectations semi-regularly or infrequently, converting to SQL Server is a good idea for facilities which plan to frequently take evaluations, whether configured to use a local or centralized database.&nbsp; Clicking the Convert to SQL Server button begins the process of:

- ...finding, selecting, and connecting to a SQL Server instance locally or on the network
- ...creating a new SQL Server database on the selected instance
- ...copying older Expectations records from the MS Access database to the new SQL Server database
- ...updating the copied records in the newly-created SQL Server database

...as well as configuring Expectations to use the new, converted SQL Server database.&nbsp; The Keep MS Access button is enabled for an older MS Access database which is...
- earlier than v7.1.x and less than or equal to 1 Gigabyte (GB) in size, or
- v7.1.x or higher and less than 1.5 Gigabytes (GB) in size.

Upon clicking the Keep MS Access button, the update process will begin as normal on the existing database.&nbsp; Note that update processing times vary greatly depending on how large the database is, processing power, etc.

<u>SQL Server database Window</u>

Upon clicking the Convert to SQL Server button, the SQL Server database window appears:

The SQL Server database window that appears during conversion will only allow for a new SQL Server database to be created and selected for the purposes of converting the older database from MS Access to SQL Server.&nbsp; After a new SQL Server database has been created for conversion, the following confirmation dialog appears:

Click the OK button in the confirmation dialog, then OK in the SQL Server database window.  The Copying Records... progress dialog appears:

After the records have been copied, the Updating... progress dialog will appear to provide the status of the final stage of database conversion from MS Access to SQL Server before either Expectations or the Training and Development application loads:

| <font size="3"><b>NOTE</b>: </font>At this time during the update process, Training & Development application records may only be migrated automatically (rather than manually) from an MS Access database to SQL Server.&nbsp; For those older MS Access databases which do not meet the criteria specified earlier in this help topic for updating 'in-place', please consider converting your database to SQL Server automatically.&nbsp; If migrating your older MS Access database to SQL Server is not feasible at this time and the "Keep MS Access" button is not enabled, please contact Smart Horizons for assistance in separating out the database into multiple MS Access databases (each of which may be updated separately by the software, as normal). |
-----