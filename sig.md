# Global Settings Tab:     Signatures Sub-Tab 
| --- |

To open the Signatures sub-tab of the 
[Global Settings tab](<globset.md>), start by selecting the Global Settings menu item from the Administrator menu on the
[main 
form](<7jjr.md>).

The Signatures sub-tab consists of:

- a "Default Signatures folder" read-only textbox (initially defaulting upon install to the Expectations Evaluation Software's "Signatures" folder)
- a "Browse" button which allows for the default signatures folder path to be changed through the use of a folder browser dialog
- a "Disable browsing for Signatures folder" checkbox which, when checked, causes the folder browser that normally appears upon clicking either the [Create Signature Key](<7dgw.md>) or [Sign](<evlvwsig.md>) buttons to not appear, and instead forces the use of the Signatures folder path specified in the "Default Signatures folder" textbox
- a "Show Signature comments in report" checkbox which, when checked, causes any comments made by those who have signed a particular evaluation to be present in the evaluation report inline with their respective digital signatures
and...- an "Allow completed evaluations to be signed before they are fully-reviewed" checkbox which, when checked, allows evaluations saved as 'Complete' to be signed by all involved parties from the [Evaluation Reviewer](<Review1.md>) and/or [Evaluation Viewer](<7ddc.md>) forms

Even when the "Disable browsing for Signatures folder" checkbox is checked, the "Browse" button in the Signatures sub-tab may still be clicked to reveal a "Browse For Folder" dialog.  The path chosen in the dialog will be used to populate the "Default Signatures folder" textbox:

Checking the "Show Signatures Comments in report" checkbox...

...will make available any comments made by signees of a particular evaluation appear inline with their corresponding digital signatures:

Unchecking the "Show Signatures Comments in report" checkbox will again hide any signature comments made by evaluation signees:

As long as the "Prevent unapproved evaluations from appearing in the View Evaluations tab until fully-reviewed" checkbox of the [Unapproved Evaluations](<unapprove.md>) sub-tab of the [System Utilities](<7mk0.md>) form's [Global Settings](<globset.md>) tab is **unchecked**, the "Allow completed evaluations to be signed before they are fully-reviewed" checkbox will be enabled.&nbsp; Checking the "Allow..." checkbox allows evaluations saved as 'Complete' to be signed by all involved parties from the [Evaluation Reviewer](<Review1.md>) and/or [Evaluation Viewer](<7ddc.md>) forms.