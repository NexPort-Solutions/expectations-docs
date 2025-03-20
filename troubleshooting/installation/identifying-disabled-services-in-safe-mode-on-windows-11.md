# Identifying Disabled Services in Safe Mode on Windows 11

If you're experiencing issues with the **Expectations** software installation that succeeds in Safe Mode but fails in Normal Mode, identifying the services that are **disabled** in Safe Mode can help isolate the problem. Follow these steps to generate a list of disabled services:

***

### **Method 1: Using Command Prompt (CMD)**

1. Boot your computer into **Safe Mode**.
2. Press **Win + R**, type `cmd`, and press **Ctrl + Shift + Enter** to run as Administrator.
3. Run the following command to list **all stopped services**:
4. Alternatively, to list **only services set to Manual or Disabled**:
5. To save the output to a text file for easier review:

***

### **Method 2: Using PowerShell**

1. Boot into **Safe Mode**.
2. Press **Win + R**, type `powershell`, and press **Ctrl + Shift + Enter** to run as Administrator.
3. Run this command to list disabled services:
4. For a more detailed export:

***

### **Method 3: Using System Configuration (msconfig)**

1. Boot into **Safe Mode**.
2. Press **Win + R**, type `msconfig`, and press **Enter**.
3. Go to the **Services** tab.
4. Check the box labeled **Hide all Microsoft services** to filter system services.
5. The remaining list represents third-party services, many of which are likely disabled in Safe Mode.

***

### **Method 4: Using Registry Editor (Advanced)**

1. Press **Win + R**, type `regedit`, and press **Enter**.
2. Navigate to this key:
3. Under `SafeBoot`, you'll see keys like:
   * **Minimal** → Services enabled in **Safe Mode** (basic mode).
   * **Network** → Services enabled in **Safe Mode with Networking**.

Any services **not listed** here are generally **disabled** in Safe Mode.

***

### **Recommended Next Steps**

Once you have the list of disabled services, compare them with the services required for the **Expectations** software installation. Ensure critical services such as:

* **Windows Installer**
* **Background Intelligent Transfer Service (BITS)**
* **Windows Update**

are enabled in Normal Mode for a successful installation. If these services are disabled, re-enable them and attempt the installation again.

For further assistance, refer to the [Expectations Evaluation Software Documentation](https://docs.nexportsolutions.com/expectations-evaluation-software).
