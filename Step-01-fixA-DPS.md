# DPS Issues

go to the VM deemed as having DPS issues<br>
open an elevated DOS prompt or PowerShell<br>
issue the command: <br>
```
azcmagent check --extensions all --location “<region>”
```
replace \"\<region\>\" with the appropriate region name, for example eastus as illustrated below<br>

![Alt text](IMAGES/009_DPS_Blocked.jpg "blocked DPS") <br>

:red_circle:As it can be seen on the last 3 rows of the image, the column **Reachable** shows **false** indicating there is a problem to reach these endpoints. <br>

:green_circle: Work with the networking team to add the URLs to the whitelist, the required port to be opened is 443

once firewall settings take effect, running the same azcmagent command above will present the following output:<br>

![Alt text](IMAGES/009_DPS_OK.jpg "DPS OK") <br>
