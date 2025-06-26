## Step-1 Identify Servers with SQL Server installed that are deemed as DPS BLOCKED
go to Azure Portal, and open Resource Graph Explorer<br>

![Alt text](IMAGES/001_AzurePortal_OpenResourceGraph.jpg "Azure Portal")

1. type Resource Graph at search bar<br>
2. Click on Resource Graph Explorer<br>

3. Azure Resource Graph explorer screen will show with an empty query<br>

![Alt text](IMAGES/002_ResourceGraph_NewQuery.jpg "New Query")
<br>

4. Copy/Paste the KQL query from the file "01_KQL_query_to_obtain_list_of_resources.KQL" located on SCRIPTS folder

5. the screen will look like:<br>

![Alt text](IMAGES/003_ResourceGraph_DPSQuery.jpg "KQL Query")
<br>

6. Execute the Query by clicking at the [Run Query] button at the toolbar<br><br>

7. Results will be shown at the results panel below the query, as seen in the image below:<br>

![Alt text](IMAGES/004_ResourceGraph_DPSQuer_Results.jpg "Query Results")<br>
scroll to the right to find the column **Server Status**

