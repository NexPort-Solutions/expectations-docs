# Trainee/Employee Reports

***

The **Trainee/Employee Reports** form is used to select the evaluations that are displayed on the [Trainees/Employees Charts](7mi8.md) window.  Note that a level 1 trainer/supervisor is only allowed to select and view their own evaluations.  Evaluations shown in the chart are ordered by the end date of the evaluation period.  The **Trainee/Employee Reports** form includes the following labeled controls:

* **Trainee/Employee (required selection):** A drop down list showing active trainees/employees, by last name then first and sorted alphabetically.  Select the trainee/employee from the list whose evaluations are to be used in the chart.
* **Trainer/Supervisor:** A drop down list showing active trainers/supervisors who have authored evaluations, by last name then first and sorted alphabetically.  The list is generated after a trainee/employee has been chosen.  Select the trainer/supervisor whose evaluations are to be used in the chart.  If no selection is made, then all evaluations for indicated trainee/employee are used.
* \*\*Range:\*\*Option buttons used to further screen the evaluations.
  * **All DOR's (default selection):** No further screening is performed.  All evaluations for the indicated trainee/employee and, if applicable, trainer/supervisor are selected for the chart.
  * **Evaluation #:** Further screen the evaluations by sequence number.  This is the order they would appear with **All DOR's** selected.  The total number of evaluations is displayed at the far right.  Start and end evaluation numbers are initially defaulted to those of the first and last evaluation.
  * **Date:** Further screens the evaluations by the end date of the evaluation period.  The two date picker controls are used to specify the window of inclusion.  They are initially defaulted to the dates of the first and last evaluation which would be returned with **All DOR's** selected.
  * **Criteria Set:** Further screens the evaluations by criteria set.  The drop down list shows the criteria sets from evaluations that would be returned with **All DOR's** selected.
  * **Comments Include:** Further screens the evaluations by comments.  This range selection searches all of the comments fields of evaluations and their criteria choice selections, as well as reviewer and signature comments, for up to 255 characters of individual term or exact-phrase texts.  Commas and/or spaces may be used when supplying more than one individual term in the text field.  One exact phrase surrounded by double quotes may be supplied instead of individual terms.
* **View:** This button is enabled after a trainee/employee selection has been made.  It opens the [Trainees/Employees Charts](7mi8.md) window, which is then loaded with evaluations that meet the specified criteria.
* **Close:** Selecting this button closes the **Trainee/Employee Reports** window.
