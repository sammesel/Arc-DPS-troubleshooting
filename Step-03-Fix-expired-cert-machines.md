# Step-3 Re-onboard machines showing 'Expired' on Status column

The Arc-enabled machine must be re-onboarded to Arc, as the certificate used to authenticate to Azure has expired.<br>

## go to your Azure Portal, and open Azure Arc<br>

![Alt text](IMAGES/010_AzurePortal_SearchAzureArc.jpg "Search for Azure Arc")

1. type Azure Arc at search bar<br>
2. Click on Azure Arc<br>

3. Azure Arc screen will display<br>

![Alt text](IMAGES/011_AzureArc_LandingPage.jpg "Azure Arc Landing Page")
<br>

4. At the left bar, Select Machines from the Azure Arc resources<br>

![Alt text](IMAGES/012_AzureArcResources_Machines_menu.jpg "Azure Arc Resources - Machine - Menu option")
<br>

5. If there are any machines with that status they will display 'Expired’ in the Agent Status column highlighted below.<br><br>

![Alt text](IMAGES/024_AzureArcResources_CertExpiredMachines.jpg "Azure Arc Resources - Expired Certification Machines")
<br>

6. Uninstall the agent by following the documentation [here](https://learn.microsoft.com/en-us/azure/azure-arc/servers/manage-agent?WT.mc_id=itopstalk-blog-socuff&tabs=windows#uninstall-the-agent)<br>

7. Re-onboard those machines following instructions [here](https://learn.microsoft.com/en-us/azure/azure-arc/servers/deployment-options).<br>

   *NOTE: There is no need to delete the Arc-enabled SQL Server resources in the portal if you are just re-onboarding.*
