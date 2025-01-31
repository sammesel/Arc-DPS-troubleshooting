# Step-4 Fix machines showing '**disconnected**' on Status column

This could be for a variety of reasons: Arc connected machine agent is stopped, disabled or constantly crashing OR it could be that the connectivity is blocked between the agent and Azure.
<br>

A.1. type Resource Graph at search bar<br>
A.2. Click on Resource Graph Explorer<br>

A.3. Azure Resource Graph explorer screen will show with an empty query<br>

![Alt text](IMAGES/002_ResourceGraph_NewQuery.jpg "New Query")
<br>

A.4. Copy/Paste the KQL query from the file 01_KQL_query_to_obtain_list_of_resources.KQL<br>
A.5. the screen will look like:<br>

![Alt text](IMAGES/003_ResourceGraph_DPSQuery.jpg "KQL Query")
<br>
A.6. Execute the Query by clicking at the [Run Query] button at the toolbar<br>
A.7. Results will be shown at the results panel below the query, as seen in the image below:<br>

![Alt text](IMAGES/004_ResourceGraph_DPSQuer_Results.jpg "Query Results")
<br>


## go to Azure Portal, and open Azure Arc<br>

![Alt text](IMAGES/010_AzurePortal_SearchAzureArc.jpg "Search for Azure Arc")

1. type Azure Arc at search bar<br>
2. Click on Azure Arc<br>

3. Azure Arc screen will display<br>

![Alt text](IMAGES/011_AzureArc_LandingPage.jpg "Azure Arc Landing Page")
<br>

4. At the left bar, Select Machines from the Azure Arc resources<br>

![Alt text](IMAGES/012_AzureArcResources_Machines_menu.jpg "Azure Arc Resources - Machine - Menu option")
<br>

5. If there are any machines with that status they will display 'Disconnected’ in the Agent Status column highlighted below.<br><br>

![Alt text](IMAGES/025_AzureArcResources_DisconnectedMachines.jpg "Azure Arc Resources - Disconnected Machines")
<br>

Alternatively, you can open Resource Graph Explorer and load the [query](scripts/02_KQL_query_to_obtain_list_of_DisconnectedMachines.KQL)

6. Uninstall the agent by following the documentation [here](https://learn.microsoft.com/en-us/azure/azure-arc/servers/manage-agent?WT.mc_id=itopstalk-blog-socuff&tabs=windows#uninstall-the-agent)<br>

7. Re-onboard those machines following instructions [here](https://learn.microsoft.com/en-us/azure/azure-arc/servers/deployment-options).<br>

   *NOTE: There is no need to delete the Arc-enabled SQL Server resources in the portal if you are just re-onboarding.*



