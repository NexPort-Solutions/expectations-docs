# Expectations Email Service: Configuration

***

To get started with the Expectations Email Service, a few configuration settings are required.  The required settings are located in the "Email Setup", "Email Test", and (if applicable) "Network Share Credentials (MS Access)" sections. The "Message Processing and Sending" and "Email Message Type" setting sections may also be configured, but are not mandatory for the proper function of the email service.

The following controls (by section) are used to configure the email service: **Email Setup**

* An "SMTP Host" textbox where a valid email host address is required
* A "Return address" textbox where a valid return email address is \*required (NOTE: Expectations requires that this field not be blank, and that the supplied address is considered a valid address by the requirements of the specified SMTP Host for using the host's "SMTP Relay" feature)
* A "Host requires SSL authentication" checkbox which, when checked, enables and requires the supply of valid information in the...
* "User ID" and "Password" textboxes

**Email Test**

* The "Test address" textbox where at least one valid test email address must be supplied before:
  * the "Send" button becomes enabled for sending out a test email (also requires "Email Setup" configuration listed above)
  * the service itself can be turned on

(any additional test addresses should be separated by commas)

**Network Share Credentials (MS Access)**

* "User Name" and "Password" textboxes which, when Expectations is set to access a central expectations.mdb database located on the network, \*must contain the user name and password credentials of a valid Windows account belonging to a Group (on the domain/machine which hosts the share) that has been given permission to Read/Write/Execute in the share folder.  (NOTE: These controls are only enabled, and account info mandated for email service-enabling purposes, when Expectations is configured to use a remote MS Access database as the central database.  These credentials are not required when using a local MS Access or SQL Server database, and the controls will correspondingly be disabled.)

**Message Processing and Sending**

* A "Reviewer Email Notifications" checkbox which, when checked, sends evaluation approval/disapproval email messages to particular Trainer/Supervisors as the Reviewers assigned to them perform these actions (see [Expectations Email Service: User Setup](emailbuslog.md)).
* A "Time Interval for Monitoring" selector which sets the interval of time that the email service waits before performing a "review" on the database (to determine if there are any new outgoing emails) in HH:MM:SS format (default interval: 1 hour / minimum interval: 1 minute)

**Email Message Type**

* Three radio buttons for each of the three supported email form-factors that the service is able to make use of when sending notification emails to users (default: "Standard" HTML / also available: "Mobile-First" HTML, plain "Text")

**"Enable Email Notifications Service" Checkbox**The "Enable Email Notifications Service" checkbox becomes enabled and may be used to turn on/off the Expectations Email Service when:

* Machine OS is Windows Vista or higher
* All required email service configuration items are supplied
* Windows Administrator-level permissions are available when prompted upon checking/unchecking the service checkbox

Only one instance of the email service may run from each database in use on any Expectations-ready computer on the network.  So if all Expectations installs on all machines at a facility are configured to use the same central database (for example), only one of them at a time may run the Expectations Email Service.  The service may only be shutdown and uninstalled from the machine where it was originally launched.

**Email Template Customization** While not required for the proper functioning of the email service, each of the email templates may be customized in accordance with the guidelines provided in the commented sections of the approved, disapproved, due, overdue, and test email templates available in the messages folder of the installation's data path (default location for Windows Vista and up: C:\ProgramData\Smart Horizons\Expectations Evaluation Software\messages). **Users and Notifications** Once configuration of the Expectations Email Service is complete, you'll want to [setup users](emailbuslog.md) to begin receiving notifications.  Also discover [how notifications work](emailguide.md) towards supplying evaluation-based information via email to your facility's Trainers/Supervisors.
