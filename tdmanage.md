| <font size="4" color="#0000FF"><b>Training Requirements Manager</b></font> |
-----

The Training Requirements Manager is accessed via the Training Requirements -&gt; Manage menu item on the main form, or via the Ctrl+M keyboard hotkey.

The manager loads automatically upon login for level 1 and 2 Trainers/Supervisors.&nbsp; Level 3 Trainers/Supervisors may launch the manager manually, and they may edit which training program entries are assigned to other training individuals through their access to the Write tab.&nbsp; All levels of Trainers/Supervisors may use the Progress and Completed tabs to adjust the accessibility and status of training program entry items in the [Training Requirements Reviewer](<tdreview.md>) and [Certification Viewer](<tdcert.md>) forms.

The Training Requirements Manager provides the means to:

- Add, remove, and see the completed/reviewed statuses of a training individual's training program entries
- Adjust the Reinstated date of an assigned training program entry
- Mark any number of items in a particular training program entry as complete and/or reviewed
- Send a training individual's active training program entries to that individual's archive
- Retrieve an archived training program entry and make it active for a training individual

## Write

The Write tab is where level 3 Trainers/Supervisors may perform the following training program entry actions:

- Assign one or more training programs to a training individual
- View completed/incomplete statuses of assigned training program entries in a color-coded fashion
- Remove the assignment of a selected training program entry from a training individual
- Send a selected training program entry to the training individual's archive for posterity and/or possible future use

First, select a Training Individual from the corresponding combobox at the top of the form to enable controls on the Write tab.&nbsp; Afterwards, click the Add button (keyboard hotkey Alt+A) to open the Add Training Programs dialog.&nbsp; From there, one or more training programs (if available) that are not already present in the current training individual's Write tab may be selected and aassigned to the selected training individual by clicking the dialog's OK button.

To remove a selected training program assignment (entry) from the Write tab, click the Remove button or press Alt+R on the keyboard.&nbsp; You will be prompted to confirm deletion of the entry.

**Red Entries**: Training program entries are initially color-coded red when originally assigned to a training individual.&nbsp; Otherwise, a red background indicates that an entry is not in the Reviewed state when it is non-recurring, or the entry 'expired' prior to being set as Reviewed in the case of a recurring entry.&nbsp; Entry expiration is based on the reinstated date, and whether or not the recurrence time period has fully elapsed since that date, when compared to today's date.**Yellow Entries**: When less than 10% of time remains before a recurring entry expires (based on how much time has elapsed of the recurrence time period since the reinstated date) and the entry has not yet been fully reviewed, the near-expired entry will have a yellow background.**Green Entries**: Training program entries which are Completed and Reviewed will have a green background.

To adjust the Reinstated date of an assigned training program entry, click the corresponding cell (or press Spacebar on the keyboard) under the Reinstated column.

The Entry Reinstated Date/Time dialog will appear where a new reinstated date may be chosen.&nbsp; Click OK in the Entry Reinstated Date/Time dialog to set the selected training program entry's date (current system time will be appended upon clicking OK).

Check (or press Spacebar on the keyboard) the Archived checkbox to deactivate and send an assigned training program entry to the training individual's archive.&nbsp; An archived training program entry will not appear in the Write, Progress, or Completed tabs (including the Completed tab of the [Training Requirements Reviewer](<tdreview.md>)), but will appear in the Archive tab of both the manager and reviewer forms.

## Progress

The Progress tab may be used by all Trainers/Supervisors to enable training program entry items for review by the training individual to whom the training program entry was assigned.&nbsp; As a Trainer/Supervisor determines that one or more training program entry items have been completed by the training individual, the Trainer/Supervisor may check the checkboxes (via mouse-click or the Spacebar key) next to the completed items in the Progress tab.

> **NOTE** : The training program entry items in the Progress tab may also be navigated via the keyboard, though checking/unchecking the checkboxes next to training program entry items using Spacebar will require a second press of the down arrow (when navigating top to bottom) or the up arrow (when navigating bottom to top) on the keyboard so that the checkbox is first put into focus. |
-----

Checking training program entry items in the Progress tab will cause the corresponding items to become enabled in the Completed tab, where either a Trainer/Supervisor may check them or the training individual (to whom the training program entry was assigned) may check them as part of the review process.&nbsp; Trainees/Employees may check training program entry items in the Completed tab through use of the [Training Requirements Reviewer](<tdreview.md>). 

## Clearing Completed/Reviewed Items

Unchecking a checkbox next to a training program entry item in the Progress tab will open a dialog to begin the process of clearing the checkmark next to that particular training program entry item, as well as the corresponding checkmark (if present) of that training program entry item in the Completed tab.

The Clear Completed/Reviewed Statuses dialog appears to ensure that the Trainer/Supervisor intended to clear the checkmark next to a completed training program entry item, and informs the Trainer/Supervisor what will occur upon confirmation of clearing the checkmark.

**IMPORTANT**: Confirmation of clearing the checkmark next to a training program entry item in the Progress tab also clears the checkmark next to any child items, as well as clearing all checkmarks of corresponding upward groups of training program entry items, for both the Progress and Completed tabs.&nbsp More information on the behavior of directly clearing the checkmark next to a training program entry item in the Completed tab may be found in the [Training Requirements Reviewer](<tdreview.md>) help topic.

## Archive

The Archive tab is where a training program entry of a particular training individual may be sent when a level 3 Trainer/Supervisor checks the Archived checkbox in the Write tab in order to:

- Deactivate that entry from the other three Training Requirements Manager tabs, as well as from the Completed tab of the [Training Requirements Reviewer](<tdreview.md>)
- Store the entry for possible future reactivation
- Create a historical record of past entries in the Archive tabs of:
    - the manager form (for Trainers/Supervisors)
    - the [Training Requirements Reviewer](<tdreview.md>) (for a Trainee/Employee who underwent the training)

Archived training program entries may be reactivated by unchecking the Archived checkbox.

**Archiving Considerations**:

- If a recurring training program entry is reactivated for use, the Trainer/Supervisor who is performing the reactivation may wish to clear any previous reviewed and/or completed statuses if present in the Completed and/or Progress tabs (respectively) in order for level 3 Trainers/Supervisors to properly make use of the entry color-coding available in the Write tab.
- Archived entries which are certifications will not remove the corresponding training individual's entry in the [Certification Viewer](<tdcert.md>)

> **NOTE** : The Samples Database feature was used as-is in most of the examples found in this help entry.&nbsp; For those Typical and Custom installations which do not currently have the Samples Database installed, a 'Change' installation may be initiated to add the feature onto a workstation where Expectations is already installed.&nbsp; After installation, more information may be found out about the Samples Database feature by reading the "Samples Readme.txt" file (accessible via shortcut from the Start menu). |
-----