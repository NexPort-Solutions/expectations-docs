# Evaluation Viewer: Signatures Tab

***

**Evaluation Viewer Tabs**

The Evaluation Viewer appears with the following tabs:

* [Trainee/Employee Information](7ddc.md)
* [Trainee/Employee Evaluation](7ddh.md)
* [Reviewer Comments](7ddr.md)
* Signatures

**Signatures Tab**

By default, the Signatures tab only appears after all reviewers have approved the evaluation.  Signatures are listed in the Signers section at the top of the tab and are entered from the Signee area below.

## | NOTE: If the "Allow completed evaluations to be signed before they are fully-reviewed" checkbox is checked (in the [Signatures](sig.htm) sub-tab of the [System Utilities](7mk0.htm) form's [Global Settings](globset.htm) tab), the Signatures tab will also appear in the Evaluation Viewer for those evaluations which have not yet been fully-reviewed. |

**Signers**

A list of signatures is seen in the Signers section of the tab.  Each signature is validated as it is entered into the list and is shown with a name, date and colored background.  Green indicates a valid signature while red indicates the signature has somehow become corrupted.  A signer's remarks will appear in the Comments box when their signature is selected in the list.  The signatures in the Signers list also appear on the last page of the report when printing or previewing.

**Signee**

Signatures are entered from the Signee area of the tab.  It is enabled when the following conditions are met:

* A signature key has been created for the current user.
* The current user has not already signed the evaluation.
* The current user is either:
  * the individual being evaluated
  * the author of the evaluation
  * one of the reviewers

Remarks can be entered into the Comments box and spell checked with the spelling button.  To sign the evaluation select the Sign button.  A Browse For Folder dialog window will then open.

Use the Browse For Folder to locate the folder containing the signature key.  The signature key can be either on the local PC, somewhere on the network, or on a memory stick.  Once the key folder is located, select the OK button.  A dialog window appears to indicate whether or not the signature was successful.  If so, then the signature is added to the list.

## | NOTE: Upon clicking "Sign", the folder browser will not appear in the case where the "Disable browsing for Signatures folder" option is checked in the [Signatures](sig.htm) sub-tab of the Global Settings tab.\&nbsp; Instead, an attempt will be made to find and use the user's signature key in the path specified as the "Default Signatures folder" (also configurable in the sub-tab). |
