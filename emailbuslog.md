# Expectations Email Service: User Setup 
| --- |

Setting users up with the Expectations email service consists of supplying values for service-related controls in the "Add..." and "Modify..." dialogs for Trainers/Supervisors and Trainees/Employees.

**Add & Modify Trainer/Supervisor Dialogs**

Trainers/Supervisors with an email address supplied in the above "Email Address" field are available for selection to receive email notifications.

**Add & Modify Trainee/Employee Dialogs**

The above controls provide the means to setup email notifications to the Trainer/Supervisor responsible for evaluating the particular Trainee/Employee.

**"Trainer/Supervisor Email Notifications" checkbox:**
Once the "Trainer/Supervisor Email Notifications" checkbox is checked, the following four email notification setup controls become enabled.

- **"Trainer/Supervisor" combobox:** All Trainers/Supervisors whose profile includes their email address (see "Add & Modify Trainer/Supervisor Dialogs" above), and who are in the same department as the current Trainee/Employee, will appear for selection in the "Trainer/Supervisor" combobox.&nbsp; A Trainer/Supervisor must be selected in order to turn on notifications for the given Trainee/Employee.
- **"Evaluate this employee every 'x' month(s)" number selector:** Choose an evaluation period from 1 to 24 months to set when evaluations are due on the Trainee/Employee.
- **"Begin notifying trainer 'x' days prior to due date" number selector:** Select a number from 1 to 28 days prior to the date the evaluation is due on the Trainee/Employee.
- **"Send reminders every 'x' days until completed" number selector:** Select an interval from 1 to 45 days to continue sending email reminders of both due and overdue email notifications.&nbsp; The first reminder will go out on the specified number of days after the first due or overdue notification, with subsequent reminders going out the same number of days from the previously-sent reminder.&nbsp; Reminders may be turned off by selecting '0'.

**Service Configuration and Use**

The user setup choices you make are immediately put into use as long as the Expectations Email Service is [configured and running](<emailinfra.md>), otherwise they will be used the next time the service runs.&nbsp; More on how the email service makes use of user setup and global configuration to provide email notifications is explained in the help page illustrating [how it works](<emailguide.md>).