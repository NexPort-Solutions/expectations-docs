# Training Requirements Editor

***

The Training Requirements Editor is accessed via the Training Requirements -> Edit menu item on the main form, or via the Ctrl+E keyboard hotkey.

The editor loads automatically upon login for a level 3 Trainer/Supervisor and allows them to create training for use in the [Training Requirements Manager](tdmanage.md).

The Training Requirements Editor provides the means to add/modify/delete the following organizational units:

* **Task Items**: Individual, unique task description texts
* **Task Lists**: Uniquely-named groups of task items, each of which may be optionally given a description
* **Training Requirements**: Uniquely-named groups of task lists, each of which may be optionally given a description
* **Training Modules**: Uniquely-named groups of training requirements, each of which may be optionally given a description
* **Training Programs**: Uniquely-named groups of training modules, each of which may be optionally:
  * given a description
  * designated as a certification
  * set as recurring, with a specified recurrence time period

## Task Items

The Task Items tab is where unique task descriptions may be added, modified, and deleted.  Task descriptions initially load in alphanumeric order.

To create a new task item, click the New button or press Alt+N on the keyboard.  The uneditable label in the "Task Items" list will take on the form < Task Item # > in an auto-incrementing fashion, and the task description will initially be blank.  When typing in a description, ensure that it is unique from the others in the list.

To remove a selected task item from the Task Items tab, click the Delete button or press Alt+E on the keyboard.  You will be prompted to confirm the deletion.

> **NOTE** : Upon deletion of a training item from the Training Modules, Training Requirements, Task Lists, or Task Items tab, the corresponding item is deleted from all higher-level lists to which the item may have belonged.

***

## Task Lists

The Task Lists tab is where uniquely-named task lists may be:

* added
* modified by:
  * name
  * description
  * list of associated task items
* deleted

Task lists initially load in the Task Lists tab alphanumerically by name.  Upon selecting a task list, any associated task items will appear in the Task Items list on the right.

Upon clicking the New button (keyboard hotkey Alt+N), a new task list will appear in the Task Lists list with a default name in the form of < New Task Item > or < New Task Item # > in an auto-incrementing fashion.  To rename a task list, either double-click the label on the left side, or click in the corresponding field of the Name column, then supply a unique task list name.  Clicking Delete (keyboard hotkey Alt+E) will open a prompt which, upon confirmation, will cause a selected task list to be deleted.

> **NOTE** : Renaming any training item in the Training Modules, Training Requirements, and Task Lists tabs will cause the item's name to also change in any higher-level lists to which the item may belong.  Similarly, changing the description of a Task Item will cause the item's description to also change in all Task Lists to which the item may belong.

***

After the task list name is accepted, you may optionally supply a description for the corresponding task list under the Description column.

All text-based columns in the center portion of all tabs in the Training Requirements Editor have the ability to check spelling for errors.  The Spell Check dialog is available at Tools -> Check Spelling from the main menu, or via the Ctrl+S keyboard hotkey.

If any spelling errors are found, one or more suggestions may appear at the bottom of the Spell Check dialog.

After making choices in the Spell Check dialog on one or more misspelled words (if any), the selected text-based cell should reflect any choices that were made.

The Task Items selection list allows for task items to be added to, reordered in, and removed from a selected task list.  Task items that make up a task list are all unique.  Reorder a selected task item upwards by clicking the up arrow (keyboard hotkey Alt+U), or downwards by clicking the down arrow (keyboard hotkey Alt+D).

Upon clicking the Add button (keyboard hotkey Alt+A), the Add Task Items window will appear.  A task item may be selected in the Add Task Items window, and more than one task item may be selected for addition by:

* holding the Ctrl key as individual items are mouse-clicked in the list, or
* clicking on an item, holding the Shift key, and pressing the up or down arrow a number of times to select items.

Add the item(s) from the Add Task Items window to the task list by clicking OK.

> **NOTE** : Each training item in the Training Modules, Training Requirements, and Task Lists tabs may be added to more than one higher-level list, but training item names in each of those tabs must be unique from one another.  Similarly, each task item present in the Task Items tab may also be added to more than one task list in the Task Lists tab, but task item descriptions must be unique from one another.

***

To remove a task item from a selected task list, click the Delete button or press Alt+T on the keyboard.  You will be prompted to confirm the deletion.

## Training Requirements

Training requirements initially load in the Training Requirements tab alphanumerically by name.  Upon selecting a training requirement, any associated task lists will appear in the Task Lists list on the right.  The Training Requirements tab is similar in functionality to the Task Lists and Training Modules tabs.

## Training Modules

Training modules initially load in the Training Modules tab alphanumerically by name.  Upon selecting a training module, any associated training requirements will appear in the Requirements list on the right.  The Training Modules tab is similar in functionality to the Training Requirements and Task Lists tabs.

## Training Programs

Training programs initially load in the Training Programs tab alphanumerically by name.  Upon selecting a training program, any associated training modules will appear in the Modules list on the right.  The Training Programs tab is similar in functionality to the Training Modules, Training Requirements, and Task Lists tabs, but with the following additional columns:

* Certification
* Recurring
* Recurrence Time Period

To designate a selected training program as a certification, check (via mouse-click or the Spacebar key) the checkbox under the Certification column.  Certification-based training programs designated as such, when assigned to a training individual in the [Training Requirements Manager](tdmanage.md), will cause the 'In Progress' and 'Completed' status for that training individual's certification-based training to appear in the [Certification Viewer](tdcert.md).

To begin making a training program a recurring item, click the corresponding cell (or press Spacebar on the keyboard) under the Recurrence Time Period column.  The Recurrence Time Period dialog will appear where a recurring time may be specified for the selected training program from 1 month to 100 years.  Click OK in the Recurrence Time Period dialog to set the selected training program's recurrence time period.

After setting the recurrence time period, the ability to set a training program as recurring is made available by enabling the selected training program's Recurring checkbox.

Upon checking the Recurring checkbox, an entry of this training program assigned to a training individual in the [Training Requirements Manager](tdmanage.md) will cause the entry to be highlighted yellow when only 10% of the entry's recurrence time period remains, or red when the entry was not set in the Reviewed state by the deadline.  More information on the color coding of recurring training program entries may be found in the [Training Requirements Manager](tdmanage.md) help topic.

> **NOTE** : The Samples Database feature was used as-is in most of the examples found in this help entry.  For those Typical and Custom installations which do not currently have the Samples Database installed, a 'Change' installation may be initiated to add the feature onto a workstation where Expectations is already installed.  After installation, more information may be found out about the Samples Database feature by reading the "Samples Readme.txt" file (accessible via shortcut from the Start menu).

***
