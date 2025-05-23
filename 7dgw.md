# Administrator Screen: Trainers/Supervisors Tab

***

Selecting either the Administrator - Create Trainer/Supervisor Signature Key menu item or the Administrator - Add/Modify/Delete A Trainer/Supervisor menu item on the [main form](7jjr.md) brings up the Trainer/Supervisor tab on the [Administrator form](7df4.md).

&#x20;         &#x20;

The Trainer/Supervisor tab on the Administrator form allows a level 3 user to manage the trainer/supervisor accounts.  It is accessible only on a [central system](7mls.md).   A list of trainers/supervisors appears at the left of the tab.  Use the buttons to the right of the list to create a signature key or to add, modify or delete a trainer/supervisor account.  Selecting the Close button exits the form.

## Create Signature Key Button

The Create Signature Key button is not enabled until after a trainer/supervisor is selected from the list.  It is used to create a signature key for the selected trainer/supervisor.  Selecting the button opens a browse for folder window which is used to select the location where the signature key is to be created.  Note: the folder browser will not appear in the case where the "Disable browsing for Signatures folder" option is checked in the [Signatures](sig.md) sub-tab of the Global Settings tab, and instead the signature key will be created in the "Default Signatures folder" (also configurable in the sub-tab).  To create the key in the specified folder select the OK button.  Keys can be stored together on the local PC or externally on a memory stick and given to the individual.  The key is then used to electronically sign an evaluation, which is accomplished on the [Evaluation Viewer Signatures tab](evlvwsig.md).  Note that a previously created key for an individual will be invalidated and that only the last key created can be used to sign an evaluation.

## Add Trainer/Supervisor Button

The Add Trainer/Supervisor button is enabled at all times.  It is used to add a new trainer/supervisor account.  Selecting the button opens the [Add Trainer/Supervisor form](7gj4.md).

## Modify Trainer/Supervisor Button

The Modify Trainer/Supervisor button is not enabled until after a trainer/supervisor is selected from the list.  It is used to edit an existing trainer/supervisor account.  Selecting the button opens the [Modify Trainer/Supervisor form](7je8.md).

## Delete Trainer/Supervisor Button

The Delete Trainer/Supervisor button is not enabled until after a trainer/supervisor is selected from the list.  It is used to delete an existing trainer/supervisor account.  Selecting it opens a dialog window with Yes and No buttons and a prompt indicating the trainer/supervisor account which is to be deleted.  The selected trainer/supervisor account, along with any [Training & Development](traindev.md) application records associated with that account, are deleted upon selection of the Yes button.

{% hint style="info" %}
**NOTE** : Trainers/supervisors that have written evaluations cannot be deleted.  All Training & Development records associated with a particular trainer/supervisor will be deleted upon deletion of that trainer/supervisor's account.  Additionally, a trainer/supervisor cannot delete their own account.
{% endhint %}

\---
