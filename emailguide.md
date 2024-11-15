# Expectations Email Service: How it Works 
---

The Expectations Email Service is the means by which notification emails are provided to those Trainers/Supervisors who are configured to receive them at specified time intervals, and under particular conditions.

Prior to the use of the email service: all requisite [configuration of the participants](<emailbuslog.md>), as well as [configuration of the service](<emailinfra.md>) itself, should be performed.
**Email Categories and Types**
As discussed in [Expectations Email Service: Configuration](<emailinfra.md>), email templates are present for the approved, disapproved, due, overdue, and test notification categories.&nbsp; There are three individual templates for each category: standard HTML, mobile-first HTML, and plain text.&nbsp; The "Email Message Type" radio buttons (Email Notifications sub-tab of Global Settings) are used to choose which of the three types of emails will go out for all categories.&nbsp; After setting up required portions of the email configuration, but prior to actually turning on the service, choose "Mobile-First" (for example) and click Send from the "Email Test" section to deliver the following notification to the supplied test address(es).&nbsp; If all is configured as it should be, the email recipient(s) should get the message and see:

*Mobile-first email is optimized for smaller screens such as phones and tablets.&nbsp; Choose "Standard" if most email service participants primarily use their workstations to check email, or plain "Text" to remove all HTML formatting & images.*
**Starting the Service: What to Expect**
[A few prerequisites](<emailinfra.md>) must be met before the Expectations Email Service may be turned on.&nbsp; These prerequisites are the same as those needed to successfully complete the sending of a test email (see Email Categories and Types above).&nbsp; Upon activating the service by checking the "Enable Email Notifications Service" checkbox, the same test email will be sent to the address(es) specified in the "Test address" textbox of the Global Settings -&gt; Email Notifications sub-tab.

After test email(s) are sent, the email service review of the current state of the database takes place at regular intervals, based on the value selected in the "Time Interval for Monitoring:" time-picker (Email Notifications sub-tab -&gt; "Message Processing and Sending" section).&nbsp; The database review itself is silent, yet generates a time-stamped confirmation message in the log file at each iteration of the time interval.
**Trainer/Supervisor Notifications**
Through use of the corresponding controls in [user setup](<emailbuslog.md>), the "Due" email will appear in the mailbox of the assigned Trainer/Supervisor on a date derived by:

- adding the months value specified in the "Evaluate this employee every 'x' month(s)" number selector to the last evaluation date (or to today's date when the Trainee/Employee has yet to be evaluated)
...then:- subtracting the value specified in the "Begin notifying trainer 'x' days prior to due date" number selector

The Trainer/Supervisor may be set to receive reminder "Due" emails at each recurring interval of days specified by the "Send reminders every 'x' days until completed" number selector, or they may be set to receive no reminders if the control is set to '0'.
If the Trainer/Supervisor fails to evaluate a particular Trainee/Employee by the due date provided in the initial email (and reminder emails, as applicable), they will begin receiving "Overdue" emails at the same recurring interval as the value set in the "Send reminders every 'x' days until completed" number selector, or just once on the day after the due date if reminders are turned off.

When the evaluation has been completed for the Trainee/Employee, a new evaluation "Due" email sending date is automatically derived using the values from the "Evaluate this employee every 'x' month(s)" and "Begin notifying trainer 'x' days prior to due date" number selectors, as before.
**Reviewer Notifications**
When the "Reviewer Email Notifications" checkbox is checked (in [service configuration](<emailinfra.md>)), an additional two email categories are made part of the recurring email cycle for those Trainers/Supervisors which have Reviewers assigned to them.&nbsp; The "Approved" email goes out for each approval made by a Reviewer of the Trainer/Supervisor's evaluation of a Trainee/Employee.

*This sample of the "Approved" email makes use of Standard HTML, which is the default [Email Message Type](<emailinfra.md>) and is optimized for workstations.*

A "Disapproved" email will arrive in the box of the Trainer/Supervisor if any one of their assigned Reviewers disapprove the evaluation.

*Text email is a versatile choice which is supported across all mail clients.&nbsp; Choosing the plain "Text" message type removes all HTML formatting & images.*