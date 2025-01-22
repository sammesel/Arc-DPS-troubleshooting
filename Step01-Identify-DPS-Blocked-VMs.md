## Step-1 identify Servers with SQL Server installed that are deemed as DPS BLOCKED
A. go to your Azure Portal, and open Resource Graph Explorer<br>

![Alt text](IMAGES/001_AzurePortal_OpenResourceGraph.jpg "Azure Portal")

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

