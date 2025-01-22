# Step-2 Eliminate Decommissioned machines
## to delete machines manually one-by-one <br>

go to your Azure Portal, and open Azure Arc<br>

![Alt text](IMAGES/010_AzurePortal_SearchAzureArc.jpg "Search for Azure Arc")

1. type Azure Arc at search bar<br>
2. Click on Azure Arc<br>

3. Azure Arc screen will display<br>

![Alt text](IMAGES/011_AzureArc_LandingPage.jpg "Azure Arc Landing Page")
<br>

4. At the left bar, Select Machines from the Azure Arc resources<br>

![Alt text](IMAGES/012_AzureArcResources_Machines_menu.jpg "Azure Arc Resources - Machine - Menu option")
<br>

5. All registered machines will be displayed<br>

![Alt text](IMAGES/013_AzureArcResources_AllMachines.jpg "Azure Arc Resources - All Machines")
<br>

6. using the listing, identify the Machine to be deleted and click on its name (left most column) <br>
7. Details of that machine will be shown <br>

![Alt text](IMAGES/014_AzureArcResources_MachinesToBeDeleted.jpg "Azure Arc Resources - Delete Machine")
<br>

8. A confirmation dialog will pop up. Click on YES<br>

![Alt text](IMAGES/015_AzureArcResources_ConfirmDeletion.jpg "Azure Arc Resources - Confirm Deletion")
<br>

9. Observe the notification at the top right of the portal<br>

![Alt text](IMAGES/016_AzureArcResources_DeletionNotification.jpg "Azure Arc Resources - Deletion Notification")
<br>

10. Once that machines is deleted, the portal will display a confirmation at the notification panel<br>

![Alt text](IMAGES/017_AzureArcResources_NotificationConfirmation.jpg "Azure Arc Resources - Notification Confirmation")
<br>
11. Dismiss that notification<br>
<br>
<br>
## to delete machines at scale <br>
### Using PowerShell<br>
1. Open PowerShell: Ensure you have the Azure PowerShell module installed. If not, you can install it using:<br>
Install-Module -Name Az -AllowClobber -Scope CurrentUser<br>
![Alt text](IMAGES/018_AzureArcResources_PowerShellInstallModule.jpg "Azure Arc Resources - PowerShell Module Installation")<br>
2. Confirm the prompt<br>
![Alt text](IMAGES/019_AzureArcResources_PowerShellInstallModuleConfirmationPrompt.jpg "Azure Arc Resources - Module Installation Confirmation Prompt")<br>
3. Connect to your Azure account:<br>
Connect-AzAccount<br>
![Alt text](IMAGES/020_AzureArcResources_PowerShellConnectToAzure.jpg "Azure Arc Resources - PowerShell Connect to Azure Account")<br>
Select the account to Login using the browser<br>
![Alt text](IMAGES/021_AzureArcResources_PowerShellSelectAccount.jpg "Azure Arc Resources - PowerShell Select the Account")<br>
4. Delete the Azure Arc resource:<br>
Remove-AzResource -ResourceId "/subscriptions/{subscription-id}/resourceGroups/{resource-group-name}/providers/Microsoft.HybridCompute/machines/{resource-name}" -Force<br>
Replace {subscription-id}, {resource-group-name}, and {resource-name} with your specific detail<br>
![Alt text](IMAGES/022_AzureArcResources_PowerShellDeleteCommand.jpg "Azure Arc Resources - PowerShell Delete Command")<br>
After few seconds the resource is deleted and PowerShell replies confirming:<br>
![Alt text](IMAGES/023_AzureArcResources_PowerShellDeleteConfirmation.jpg "Azure Arc Resources - PowerShell Delete Confirmation")<br>

### Using Azure CLI<br>
1. Open your command line interface: Ensure you have the Azure CLI installed. If not, you can install it from the An external link was removed to protect your privacy..<br>
2. Log in to your Azure account:<br>
az login<br>
3. Delete the Azure Arc resource:<br>
az resource delete --ids "/subscriptions/{subscription-id}/resourceGroups/{resource-group-name}/providers/Microsoft.HybridCompute/machines/{resource-name}"<br>
Replace {subscription-id}, {resource-group-name}, and {resource-name} with your specific details.<br>






