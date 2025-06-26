## Step-1 Identify Servers with issues
go to Azure Portal, and open Resource Graph Explorer<br>

![Alt text](IMAGES/001_AzurePortal_OpenResourceGraph.jpg "Azure Portal")

1. type Resource Graph at search bar<br>
2. Click on Resource Graph Explorer<br>

3. Azure Resource Graph explorer screen will show with an empty query<br>

![Alt text](IMAGES/002_ResourceGraph_NewQuery.jpg "New Query")
<br>

4. Copy/Paste the KQL query from the file "01_KQL_query_to_obtain_list_of_resources.KQL" located on SCRIPTS folder

5. the screen will look like:<br>

![Alt text](IMAGES/003_ResourceGraph_DPSQuery.jpg "KQL Query")<br>

6. Execute the Query by clicking at the [Run Query] button at the toolbar<br>

7. Results will be shown at the results panel below the query, as seen in the image below:<br>

![Alt text](IMAGES/004_ResourceGraph_DPSQuery_Results.jpg "Query Results")<br>

8. scroll to the right to find the column **DPS Status**<br>
* look for entries not showing DPS Status **OK**<br>
* alternatively edit the KQL query to add a filter by removing the comment sign (//) leading the line 69:<br>
```
//| where ['DPS Status'] != "OK"
```
![Alt text](IMAGES/005_ResourceGraph_DPSQuery_edited.jpg "KQL Query for DPS")<br>

## Step-2 Fix issues
Navigate to the following pages according to the issues:<br>

Connectivity Issues: For **DPS Status not OK**, or for **TLS related issues**  go to [Step-01-A-fix-Connectivity.md](Step-01-A-fix-Connectivity.md)<br>
Agent Issues: For **SQL Extension State not Healthy** go to [Step-01-fix-B-SQLExtension.md](Step-01-B-fix-SQLExtension.md)<br>



