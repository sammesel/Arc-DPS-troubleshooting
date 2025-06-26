# Fix Extension issues
Arc uses TLS to communicate from the VM to Azure. Communication to these endpoints uses HTTPS with SSL/TLS and port TCP/443 for encrypted secure connections. The agent initiates communication to send the data to Azure. Azure never initiates communication

go to the VM deemed as having TLS issues<br>
open an elevated PowerShell prompt<br>
issue the command: <br>
```
"[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12"    
```
replace "<region>" with the appropriate region name, for example eastus as illustrated below<br>
