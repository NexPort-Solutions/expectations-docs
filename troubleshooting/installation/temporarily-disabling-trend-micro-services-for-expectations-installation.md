# Temporarily Disabling Trend Micro Services for Expectations Installation

If you're encountering issues installing the **Expectations** software due to Trend Micro security software, this guide will help you temporarily disable the related services using a PowerShell script. This allows the installation to proceed without interference, and the services can be restarted afterward.

***

{% hint style="danger" %}
### Important Notes

* This process **temporarily disables** Trend Micro protection. Use it **only** during installation.
* **Administrator privileges are required** to run these commands.
* All services will typically restart automatically after a system reboot or by starting them manually.
{% endhint %}

### Step 1: Open PowerShell as Administrator

1. Press **Windows + X**, then select **Windows Terminal (Admin)** or **PowerShell (Admin)**.
2. If prompted by User Account Control (UAC), click **Yes** to continue.

***

### Step 2: Stop Trend Micro Services

Paste the script below into the PowerShell window and press **Enter**:

```powershell
# List of Trend Micro service names to stop
$trendMicroServices = @(
    "ntrtscan",                    # Real-Time Scan
    "tmlisten",                    # Agent Listener
    "TmCCSF",                      # Common Client Solution Framework
    "svcGenericHost",              # Generic Host Service
    "TMBMServer",                  # Unauthorized Change Prevention
    "TmWSCSvc"                     # Worry-Free Security Center Integration
)

foreach ($service in $trendMicroServices) {
    if (Get-Service -Name $service -ErrorAction SilentlyContinue) {
        Write-Host "Stopping service: $service" -ForegroundColor Yellow
        Stop-Service -Name $service -Force
    } else {
        Write-Host "Service not found: $service" -ForegroundColor Gray
    }
}

Write-Host "All available Trend Micro services have been stopped." -ForegroundColor Green
```

***

### Step 3: Install Expectations

With the security services temporarily disabled:

* Run the **Expectations software installer**.
* Complete the installation process as usual.

After installation:

* **Restart your computer**, or
* Use the restart script below to manually start the services.

***

### Optional: Restart Trend Micro Services Manually

If you prefer not to reboot, run this script in PowerShell to restart the services:

```powershell
$trendMicroServices = @(
    "ntrtscan",
    "tmlisten",
    "TmCCSF",
    "svcGenericHost",
    "TMBMServer",
    "TmWSCSvc"
)

foreach ($service in $trendMicroServices) {
    if (Get-Service -Name $service -ErrorAction SilentlyContinue) {
        Write-Host "Starting service: $service" -ForegroundColor Yellow
        Start-Service -Name $service
    }
}

Write-Host "Trend Micro services have been restarted." -ForegroundColor Green
```

***

### Additional Tips

* On company-managed systems, Trend Micro services may restart automatically due to centralized policies.
* If any services fail to stop or restart, contact your IT administrator or Trend Micro support.

For more assistance, visit the [Expectations Evaluation Software Documentation](https://docs.nexportsolutions.com/expectations-evaluation-software).
