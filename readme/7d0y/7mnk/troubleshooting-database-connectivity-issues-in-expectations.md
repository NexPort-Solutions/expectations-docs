---
cover: >-
  ../../../.gitbook/assets/DALL·E 2024-11-16 12.54.51 - A professional masthead
  image for an article on troubleshooting database connections. The image
  features abstract representations of server connection.webp
coverY: 22
layout:
  cover:
    visible: true
    size: full
  title:
    visible: true
  description:
    visible: false
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: true
---

# Troubleshooting Database Connectivity Issues in Expectations

This guide helps troubleshoot database connectivity problems in Expectations, considering its requirement for both x86 and x64 OLEDB drivers. These products depend on the MSOLEDBSQL provider for connectivity.

#### Prerequisite <a href="#id-1-install-oledb-drivers" id="id-1-install-oledb-drivers"></a>

Installation of the [Microsoft Visual C++ Redistributable](https://learn.microsoft.com/en-us/cpp/windows/latest-supported-vc-redist) is a prerequisite, and while the x64 installer for Microsoft OLE DB Driver installs both the 64-bit and 32-bit driver, the x64 installer for the Microsoft Visual C++ Redistributable doesn't install 32-bit binaries. You must install both the x86 and x64 versions of the C++ redistributable package to install the x64 OLE DB driver package. You may be asked to restart the computer.

#### Install OLEDB Drivers <a href="#id-1-install-oledb-drivers-1" id="id-1-install-oledb-drivers-1"></a>

Expectations requires version 18.7.4 version of the Microsoft OLE DB Driver for SQL Server (MSOLEDBSQL). Some Windows systems do not come with this driver already installed. Follow the directions below to install them.

* Visit the official Microsoft download page: [https://learn.microsoft.com/en-us/sql/connect/oledb/release-notes-for-oledb-driver-for-sql-server?view=sql-server-ver16#](https://learn.microsoft.com/en-us/sql/connect/oledb/release-notes-for-oledb-driver-for-sql-server?view=sql-server-ver16#1874)
* Download x64 version of the 18.7.4 MSOLEDBSQL driver
* Run both installers, following the on-screen prompts.

#### Install .NET Framework <a href="#id-2-install-net-framework" id="id-2-install-net-framework"></a>

* Expectations .NET Framework version 4.7 or greater.
* Please install the .Net Framework runtime version 4.8 or 4.8.1

#### Restart Your System <a href="#id-3-restart-your-system" id="id-3-restart-your-system"></a>

* Restart your computer after driver installations to apply changes.

#### Verify Installation <a href="#id-4-verify-installation" id="id-4-verify-installation"></a>

* Confirm both OLEDB drivers are listed in "Programs and Features" or "Apps & features."
* You can also use a Powershell script to verify: [#verify-the-versions-of-msoledbsql-provider-installed](troubleshooting-database-connectivity-issues-in-expectations.md#verify-the-versions-of-msoledbsql-provider-installed "mention")

#### Test Expectations <a href="#id-5-test-premier-responder" id="id-5-test-premier-responder"></a>

* Launch Expectations and test its database connection.

### Verify the versions of MSOLEDBSQL provider installed <a href="#verify-the-versions-of-msoledbsql-provider-installed" id="verify-the-versions-of-msoledbsql-provider-installed"></a>

**Open up the 32 bit (x86) version of Powershell**

&#x20;​

<figure><img src="https://files.gitbook.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FojMNiS5J0qK6D3VFgdSh%2Fuploads%2FPvSaJG7Ps83pVPo9ZQHJ%2Fimage.png?alt=media&#x26;token=0a6c1c55-349d-4017-9bab-3c8ba033ad6a" alt=""><figcaption></figcaption></figure>

**Paste in the following script:**

```powershell
foreach ($provider in [System.Data.OleDb.OleDbEnumerator]::GetRootEnumerator()) {
    $properties = @{}
    for ($i = 0; $i -lt $provider.FieldCount; $i++) {
        $properties[$provider.GetName($i)] = $provider.GetValue($i)
    }
    [PSCustomObject]$properties
}
```

When you run the script a list of 32bit providers will be displayed. In that list look for a provider with:

```powershell
SOURCES_NAME           :  MSOLEDBSQL
```

If the Provider does not show up then the 32bit (x86) version of the driver is not properly installed. If you see a provider named MSOLEDBSQL19 then you have installed the wrong version, see [#id-1-install-oledb-drivers-1](troubleshooting-database-connectivity-issues-in-expectations.md#id-1-install-oledb-drivers-1 "mention")

### Advanced Troubleshooting <a href="#advanced-troubleshooting" id="advanced-troubleshooting"></a>

* **Install SQL Server Management Studio (SSMS):** This may install missing dependencies or help diagnose connection problems.
* **Contact Nexport Solutions Support:** For persistent issues, contact support for expert assistance.
