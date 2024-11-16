# Database Connection

***

After installation, Expectations is configured to establish a connection to an Access database file in the application folder by default. Use the File - Close Database and File - Open Database menu items on the [main form](7jjr.md) to locate and connect to an alternate database.

## Close Database

In order to connect to an alternate database, the existing database connection must be closed. Use the File - Close Database menu item to do this. This menu item is enabled prior to logging in.

>

## Open Database

Use the File - Open Database menu item to locate and open a connection to an alternate database. This menu item is enabled when not connected to a database.

>

## Select Database

Selecting the File - Open Database menu item brings up the Select Database window. Expectations can work from either an Access or SQL Server database. The option buttons on the Select Database window are used to select the database type. Text boxes opposite the option buttons indicate the database to open. Use the associated Change buttons to change the database. A connection attempt is made when the OK button is selected. The Select Database window closes and the Login window appears if the connection attempt is successful.

\| NOTE: Expectations will remember and subsequently\
connect to the last database that was opened. |
-----------------------------------------------

>

Selecting the Access database Change button opens a browser dialog window. Use it to locate and select the Access database file (expectations.mdb) to connect to. Click on the Open button to update the Access database text box on the Select Database window. Selecting the Cancel button closes the browser without updating the database.

>

Selecting the SQL Server database Change button opens the SQL Server database window. It is used to specify a server, connect to the server, and select a database on the server. This process is described in the paragraphs and illustrations that follow.

>

First, use the controls located in the Select Server area of the window to specify the SQL server, either by name or IP address. Instances of SQL servers located on the network are listed in the Server drop down selector. If, for any reason, a server does not appear in the drop down list, the instance name or IP address can be entered into the Server box.

>

Once a SQL server has been specified, use the controls in the Server Log In area to establish a connection. In order to connect to the specified server, it must be configured to use SQL authentication and allow network connections. Additionally, a login and password for the server must be obtained. To make the connection to the server, enter the login name and password into the appropriate boxes and then select the Login button.

>

Once the SQL server connection has been established, Expectations related databases are listed in the Select Database area of the window. Making a database selection from the list enables the OK button at the bottom of the window.

>

To create a new database, enter a name into the text box located to the left of the Create Database button. The button is enabled as long as the entered name is valid. After entering the database name select the Create Database button.

>

If successful, the Database Created window appears with information on how to connect to the newly-created SQL Server database. Click OK to see the new database in the Select Database list.

>

Finally, select the desired database from the list and then click on the OK button. The SQL Server database window now closes and the selected database appears in the SQL Server database text box on the Select Database window. Selecting the Cancel button closes the window without updating the database.

>

## Migration to SQL Server

{% hint style="info" %}
If you experience problems connecting to the SQL Server database please refer to [troubleshooting-database-connectivity-issues-in-expectations.md](readme/7d0y/7mnk/troubleshooting-database-connectivity-issues-in-expectations.md "mention")
{% endhint %}



At launch or when switching the choice in the Select Database dialog, you can choose to automatically migrate older MS Access databases and update them using the [Conversion Options](conv.md) dialog. If your database is already of the current version, or if you wish to manually perform the switch over to using a SQL Server database, please use the following procedure:

1. A server must be available on the network. If not, download and install either [SQL Server 2005 Express](http://www.microsoft.com/sqlserver/2005/en/us/express.aspx) or [SQL Server 2008 Express](http://www.microsoft.com/sqlserver/2008/en/us/express.aspx). These are limited versions of SQL Server. Installation and configuration instructions are available on the download site.
2. Connect to the [central](7mls.md) Access database file as described above.
3. [Download](7mr4.md) the [departments, shifts, and phases](7mye.md) that are to be relocated to the new database.
4. [Download](7mr4.md) the [trainers/supervisors](7msw.md), [trainees/employees](7muo.md), [criteria sets](7myd.md), and [evaluations](7my8.md) that are to be relocated to the new database.
5. Create and connect to the SQL Server database as described above.
6. With Expectations connected to the SQL Server database, [login](7d2o.md) by entering **Admin** and **password** respectively for Login Name and Password.
7. [Upload](7po0.md) the previously downloaded departments, shifts, and phases.
8. Assign a department to the Admin user in the [Modify Trainer/Supervisor](7je8.md) window.
9. [Upload](7po0.md) the previously downloaded trainers/supervisors, trainees/employees, criteria sets, and evaluations.

Note: Relocating evaluations to a SQL Server database is optional. While they are not required for authoring new evaluations, they may be wanted for historical reference.

{% hint style="info" %}
**NOTE** : At this time during the update process, Training & Development application records may only be migrated automatically (rather than manually) from an MS Access database to SQL Server. For those older MS Access databases which do not meet the criteria specified in the [Conversion Options](conv.md) help topic for updating 'in-place', please consider converting your database to SQL Server automatically. If migrating your older MS Access database to SQL Server is not feasible at this time and the "Keep MS Access" button is not enabled, please contact Smart Horizons for assistance in separating out the database into multiple MS Access databases (each of which may be updated separately by the software, as normal).
{% endhint %}

***
