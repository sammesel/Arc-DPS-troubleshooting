# Arc-DPS-troubleshooting
Step-by-step process to identify Arc-enabled SQL Server instances that are not connected properly to Arc or are identified as DPS BLOCKED

## Step-1 Identify Servers with SQL Server installed that are having problems
[Find servers with blocked DPS](Step-01-Identify-VMs-with-problems.md)<br>
These problems as well remediation steps explained in details<br>
* DPS Status
* Extension State
* TLS communication

## Step-2 Eliminate decommissioned machines
[Decommision machines](Step-02-Eliminate-decommissioned-machines.md)<br>

## Step-3 Fix "Machine Certification Expired"
[Reonboard machines showing 'Expired' on Status column](Step-03-Fix-expired-cert-machines.md)<br>

## Step-4 Fix "Disconnected Machine"
[Reconnect machines showing 'Disconnected' on Status column](Step-04-Fix-disconnected-machines.md)<br>

## Step-5 Address "Unhealthy Extension"
[Review machines with status other than 'Healthy'](Step-05-Fix-provisioned-failed-status.md)<br>

## Step-6 Address machines with "FAILED" provisioning status
[Review machines with Provisioning status other than 'OK'](Step-06-Fix-unhealthy-extension.md)<br>
