# System Properties

***

The System Properties tab on the [System Utilities form](7mk0.md) is accessed via the Administrator - System Properties menu item on the [main form](7jjr.md).

The System Properties tab is divided into the following five sections:

* System Type: used to designate a workstation as being either an evaluation writing station or a central repository for evaluations.
* Database: compact and repair utility.
* Department: utility for managing the departments under which the trainers/supervisors and trainees/employees are assigned.
* Shift: utility for managing the shifts that are designated in a trainee's/employee's evaluation.
* Phase: utility for managing the phases that are designated in a trainee's/employee's evaluation.

## Managing Departments, Shifts, And Phases

A department, shift, or phase can be added by clicking the Add button under the respective category.  Double-click the < New ... > item to specify a text description, 50 characters maximum.  The lists are sorted alphabetically.  Item texts can be modified upon double-clicking the item.  Items can also be deleted by making a selection in one of the lists and then clicking on the respective Delete button.  The **'Department ALL'** selection is a reserved department used to provide assigned level 3 Trainer/Supervisors the additional abilities of writing evaluations and printing worksheets on all Trainee/Employees, irrespective of department.  Since the 'Department ALL' selection is reserved, it may not be modified in, or deleted from, the Department list.  The Delete button is not active until an item is selected in the corresponding category.

## Compact And Repair Utility

The compact and repair button is enabled when connected to an Access database.  It is used to maximize the database performance, reducing its size and increasing the speed of queries.  Before running the utility, all other Expectations forms must be closed.  Also, all connections to the shared database by other Expectations applications must be closed.  To start the utility select the Compact and Repair button at the top right of the tab.  A confirmation dialog will be displayed.  At this point the operator can either continue or abort.  Upon confirmation, a new database is created from the existing database and the existing database is replaced.  Before this happens, the user is automatically logged out of Expectations and the database connection is closed.  An error dialog window is displayed if any Expectations forms remain open or if other applications are connected to the shared database.  A compact and repair complete dialog window notifies the user when finished.

## Setting The System Type

The System Type setting is used to configure a workstation as being either a central system or a stand-alone system, a central system being a repository for evaluations and a stand alone system being an evaluation writing station.  It is a means of maintaining a centralized database when network access is not available.  Typically there will be one central system.  Trainers/supervisors, trainees/employees, and criteria sets, are entered at the central system and then selectively transferred to each of the stand-alone systems.  Evaluations authored at the stand-alone systems are then transferred back to the central system.  The data transfers are accomplished using the [download](broken-reference) and [upload](broken-reference) utilities.

Where network access is available, workstations can be configured to work from a common database.  Use the [File - Close Database](broken-reference) and [File - Open Database](broken-reference) menu items on the [main form](7jjr.md) to locate a shared database on the network.  When working from a common database, data transfers become unnecessary.

\| WARNING: Do not manipulate the system type on a central system\
in order to upload\
trainers/supervisors, trainees/employees, or criteria sets.\&nbsp; This may result in lost of data. |
-----------------------------------------------------------------------------------------------------
