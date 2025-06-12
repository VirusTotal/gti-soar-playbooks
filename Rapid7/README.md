# Workflow

In Rapid7 InsightConnect, as a user, you can leverage workflows to automate tasks and seamlessly integrate various security systems and plugins. A workflow is essentially a series of automated steps that streamline your processes and reduce the need for manual intervention, helping you manage your security operations more efficiently.

1. **Legacy Detection Rule Based IOC Enrichment and Threat Contextualization using GTI** – This workflow is using Legacy Detection rule as the trigger, meaning it will be executed automatically whenever any suspicious activity is detected by the InsightIDR detection rule engine and enriches IOCs with GTI data and sends them to InsightIDR via Webhook.

2. **IDR Alert Based IOC Enrichment and Threat Contextualization using GTI** – With the help of IDR Alert as the trigger, this workflow will be executed automatically whenever any suspicious activity is detected by the user-defined detection rule and enriches IOCs with GTI data and sends them to InsightIDR via Webhook.

3. **Get Ransomware Threat List from GTI** – It fetches data from GTI with a user-defined time interval and sends ransomware threat list content to InsightIDR via Webhook.

4. **Get Malicious Network Infrastructure Threat List from GTI** – It fetches data from GTI with a user-defined time interval and sends malicious network infrastructure threat list content to InsightIDR via webhook.

5. **Get Malware Threat List from GTI** – It fetches data from GTI with a user-defined time interval and sends malware threat list content to InsightIDR via webhook.

6. **Get Threat Actor Threat List from GTI** – It fetches data from GTI with a user-defined time interval and sends threat actors threat list content to InsightIDR via webhook.

7. **Get Daily Top Trending Threat List from GTI** – It fetches data from GTI with a user-defined time interval and sends trending threat list content to InsightIDR via webhook, helping you stay updated with emerging threats.

8. **Get Mobile Threat List from GTI** – It fetches data from GTI with a user-defined time interval and sends mobile threat list content to InsightIDR via webhook.

9. **Get OS X Threat List from GTI** – It fetches data from GTI with a user-defined time interval and sends OS X threat list content to InsightIDR via webhook.

10. **Get Linux Threat List from GTI** – It fetches data from GTI with a user-defined time interval and sends Linux threat list content to InsightIDR via webhook.

11. **Get Internet of Things Threat List from GTI** – It fetches data from GTI with a user-defined time interval and sends IOT threat list content to InsightIDR via webhook.

12. **Get Cryptominers Threats List from GTI** – It fetches data from GTI with a user-defined time interval and sends cryptominer threat list content to InsightIDR via webhook.

13. **Get Phishing List from GTI** – It fetches data from GTI with a user-defined time interval and sends phishing threat list content to InsightIDR via webhook.

14. **Get First Stage Delivery Vector Threat List from GTI** – It fetches data from GTI with a user-defined time interval and sends First Stage Delivery Vector threat list content to InsightIDR via webhook.

15. **Get Vulnerability Weaponization Threat List from GTI** – It fetches data from GTI with a user-defined time interval and sends content involving exploits that target vulnerabilities in systems or software to InsightIDR via webhook.

16. **Get Infostealers Threat List from GTI** – It fetches data from GTI with a user-defined time interval and sends infostealer malware-related content to InsightIDR via webhook.

17. **Get IOC Stream Notifications from GTI** – It fetches the user’s curated personalized IOC streams configured on Google Threat Intelligence platform.

18. **Get IOC Comments from GTI** – It fetches all the comments present on the google threat intelligence platform for the specified IP Address, Domain, URL, or File Hash.

19. **Add Comment to IOC on GTI** – It adds user specified comment on the user provided IP Address, Domain, URL, or File Hash. Furthermore, if the user would like to add tags to the specified comment on the IOC Value then they can pre-append \# in front of the string. e.g. This is malicious ip address \#malicious (Over here, malicious will be added as a tag on the google threat intelligence platform for the provided IOC value)

20. **Delete IOC Comment on GTI** – If the user wishes to delete any comment that they have previously added for any IP Address, Domain, URL, or File Hash, on Google Threat Intelligence platform, then they can delete it with the help of this workflow.

21. **Legacy Detection Rule Based Vulnerability Associations Analysis using GTI** – This workflow is using Legacy Detection rule as the trigger, meaning it will be executed automatically whenever any suspicious activity is detected by the InsightIDR detection rule engine and related vulnerabilities will be retrieved for all the detected IOCs.

22. **IDR Alert Based Vulnerability Associations Analysis using GTI** – With the help of IDR Alert as the trigger, this workflow will be executed automatically whenever any suspicious activity is detected by the user-defined detection rule and related vulnerabilities will be retrieved for all the detected IOCs.

23. **Legacy Detection Rule Based File Sandbox Analysis using GTI** – This workflow is using Legacy Detection rule as the trigger, meaning it will be executed automatically whenever any suspicious activity is detected by the InsightIDR detection rule engine and File Hash Sandbox report will be retrieved for all the detected file hashes.

24. **IDR Alert Based File Sandbox Analysis using GTI** – With the help of IDR Alert as the trigger, this workflow will be executed automatically whenever any suspicious activity is detected by the user-defined detection rule and File Hash Sandbox report will be retrieved for all the detected file hashes.

25. **Legacy Detection Rule Based Passive DNS Data Analysis using GTI** – With the help of Legacy Detection rule as the trigger, this workflow will be executed automatically whenever any suspicious activity is detected by the InsightIDR detection rule engine and will retrieve passive DNS data for the detected IP address or domain from Google Threat Intelligence, providing historical DNS resolution information.

26. **IDR Alert Based Passive DNS Data Analysis using GTI** – With the help of IDR Alert as the trigger, this workflow will be executed automatically whenever any suspicious activity is detected by the user-defined detection rule and will retrieve passive DNS data for the detected IP address or domain from Google Threat Intelligence, providing historical DNS resolution information.

27. **Scan File using GTI** – This is a manual workflow which will retrieve the analysis report for a public file submitted to Google Threat Intelligence for scanning.

28. **Scan Private File using GTI** – This is a manual workflow which will retrieve the analysis report for a file privately submitted to Google Threat Intelligence for scanning.

29. **Get CVE Sources using GTI** – This is a manual workflow which will retrieve a list of information providers that offer original context, metadata, and reference details related to a specific vulnerability.

30. **Scan Url using GTI** – This is a manual workflow which will retrieve the analysis report for a url submitted to Google Threat Intelligence for scanning.

31. **Scan Private Url using GTI** – This is a manual workflow which will retrieve the analysis report for a url privately submitted to Google Threat Intelligence for scanning.

32. **Get ASM Issues from GTI** – This is a polling based workflow running at an interval of 1 hr. With the help of this workflow, users can retrieve the ASM Issues configured on the Google Threat Intelligence platform in the form of events. 

33. **Get DTM Alerts from GTI** – This is a polling based workflow running at an interval of 1 hr. With the help of this workflow, users can retrieve the DTM Alerts configured on the Google Threat Intelligence platform in the form of events.

## Configure Workflow

1. **Automatic Workflows**:  
   1. IDR Alert based Workflows: These are automatic workflows triggered on the basis of configured **Basic Detection Rule** also known as **IDR Alert**. Users need to create basic detection rule based on which these workflows will get executed.  
      1. IDR Alert Based Vulnerability Associations Analysis using GTI  
      2. IDR Alert Based File Sandbox Analysis using GTI  
      3. IDR Alert Based Passive DNS Data Analysis using GTI  
      4. IDR Alert Based IOC Enrichment and Threat Contextualization using GTI  
   2. Legacy Rule based Workflow: These are automatic workflows triggered on the basis of **Legacy Detection Rules**.  
      1. Legacy Detection Rule Based Vulnerability Associations Analysis using GTI  
      2. Legacy Detection Rule Based File Sandbox Analysis using GTI  
      3. Legacy Detection Rule Based Passive DNS Data Analysis using GTI  
      4. Legacy Detection Rule Based IOC Enrichment and Threat Contextualization using GTI  
2. **Get IOC Stream Notifications from GTI**: This is a manual workflow using which users can retrieve their personalized IOC streams configured on Google Threat Intelligence platform.  
   1. Select IOC Stream Notifications workflow  
   2. Click on Edit in Builder button  
   3. Click on IOC Stream Notifications action  
   4. Provide the filter parameter to filter the curated notifications for data retrieval (Optional)  
   5. Once added, click on Save Step  
   6. Click on the toggle button to enable the workflow  
   7. Click on the 3 dots, post that click on Run workflow to execute the workflow  
   8. Once the workflow execution is completed, notifications will be sent to InsightIDR with the help of Webhook  
   9. Click on the toggle button to disable the workflow  
3. **Threat List Workflows**: Threat List workflows run on hourly basis. Moreover, all the threat list workflows support a maximum of past 7 days data retrieval related to the categorised threat list.  
   1. Get Ransomware Threat List from GTI  
      1. Click on Edit in Builder button  
      2. Click on Ransomware Threat List action  
      3. Add query parameter to filter the threat list IOCs (Optional)  
      4. Once added, click on Save Step  
      5. Click on the toggle button to enable the workflow  
      6. To ingest past data (maximum of last 7 days)  
         1. Click on 3 dots  
         2. Click on Run Workflow  
         3. Enter the starting time from when you want to ingest the data from GTI servers related to the ransomware threat list.  
         4. Click on Run Workflow  
   2. Get Malicious Network Infrastructure Threat List from GTI  
      1. Click on Edit in Builder button  
      2. Click on Malicious Network Infrastructure Threat List action  
      3. Add query parameter to filter the threat list IOCs (Optional)  
      4. Once added, click on Save Step  
      5. Click on the toggle button to enable the workflow  
      6. To ingest past data (maximum of last 7 days)  
         1. Click on 3 dots  
         2. Click on Run Workflow  
         3. Enter the starting time from when you want to ingest the data from GTI servers related to the ransomware threat list.  
         4. Click on Run Workflow  
   3. Get Malware Threat List from GTI  
      1. Click on Edit in Builder button  
      2. Click on Malware Threat List action  
      3. Add query parameter to filter the threat list IOCs (Optional)  
      4. Once added, click on Save Step  
      5. Click on the toggle button to enable the workflow  
      6. To ingest past data (maximum of last 7 days)  
         1. Click on 3 dots  
         2. Click on Run Workflow  
         3. Enter the starting time from when you want to ingest the data from GTI servers related to the ransomware threat list.  
         4. Click on Run Workflow  
   4. Get Threat Actor Threat List from GTI  
      1. Click on Edit in Builder button  
      2. Click on Threat Actor Threat List action  
      3. Add query parameter to filter the threat list IOCs (Optional)  
      4. Once added, click on Save Step  
      5. Click on the toggle button to enable the workflow  
      6. To ingest past data (maximum of last 7 days)  
         1. Click on 3 dots  
         2. Click on Run Workflow  
         3. Enter the starting time from when you want to ingest the data from GTI servers related to the ransomware threat list.  
         4. Click on Run Workflow  
   5. Get Daily Top Trending Threat List from GTI  
      1. Click on Edit in Builder button  
      2. Click on Daily Top Trending Threat List action  
      3. Add query parameter to filter the threat list IOCs (Optional)  
      4. Once added, click on Save Step  
      5. Click on the toggle button to enable the workflow  
      6. To ingest past data (maximum of last 7 days)  
         1. Click on 3 dots  
         2. Click on Run Workflow  
         3. Enter the starting time from when you want to ingest the data from GTI servers related to the ransomware threat list.  
         4. Click on Run Workflow  
   6. Get Mobile Threat List from GTI  
      1. Click on Edit in Builder button  
      2. Click on Mobile Threat List action  
      3. Add query parameter to filter the threat list IOCs (Optional)  
      4. Once added, click on Save Step  
      5. Click on the toggle button to enable the workflow  
      6. To ingest past data (maximum of last 7 days)  
         1. Click on 3 dots  
         2. Click on Run Workflow  
         3. Enter the starting time from when you want to ingest the data from GTI servers related to the ransomware threat list.  
         4. Click on Run Workflow  
   7. Get OS X Threat List from GTI  
      1. Click on Edit in Builder button  
      2. Click on OS X Threat List action  
      3. Add query parameter to filter the threat list IOCs (Optional)  
      4. Once added, click on Save Step  
      5. Click on the toggle button to enable the workflow  
      6. To ingest past data (maximum of last 7 days)  
         1. Click on 3 dots  
         2. Click on Run Workflow  
         3. Enter the starting time from when you want to ingest the data from GTI servers related to the ransomware threat list.  
         4. Click on Run Workflow  
   8. Get Linux Threat List from GTI  
      1. Click on Edit in Builder button  
      2. Click on Linux Threat List action  
      3. Add query parameter to filter the threat list IOCs (Optional)  
      4. Once added, click on Save Step  
      5. Click on the toggle button to enable the workflow  
      6. To ingest past data (maximum of last 7 days)  
         1. Click on 3 dots  
         2. Click on Run Workflow  
         3. Enter the starting time from when you want to ingest the data from GTI servers related to the ransomware threat list.  
         4. Click on Run Workflow  
   9. Get Internet of Things Threat List from GTI  
      1. Click on Edit in Builder button  
      2. Click on Internet of Things Threat List action  
      3. Add query parameter to filter the threat list IOCs (Optional)  
      4. Once added, click on Save Step  
      5. Click on the toggle button to enable the workflow  
      6. To ingest past data (maximum of last 7 days)  
         1. Click on 3 dots  
         2. Click on Run Workflow  
         3. Enter the starting time from when you want to ingest the data from GTI servers related to the ransomware threat list.  
         4. Click on Run Workflow  
   10. Get Cryptominers Threat List from GTI  
       1. Click on Edit in Builder button  
       2. Click on Cryptominers Threat List action  
       3. Add query parameter to filter the threat list IOCs (Optional)  
       4. Once added, click on Save Step  
       5. Click on the toggle button to enable the workflow  
       6. To ingest past data (maximum of last 7 days)  
          1. Click on 3 dots  
          2. Click on Run Workflow  
          3. Enter the starting time from when you want to ingest the data from GTI servers related to the ransomware threat list.  
          4. Click on Run Workflow  
   11. Get Phishing Threat List from GTI  
       1. Click on Edit in Builder button  
       2. Click on Phishing Threat List action  
       3. Add query parameter to filter the threat list IOCs (Optional)  
       4. Once added, click on Save Step  
       5. Click on the toggle button to enable the workflow  
       6. To ingest past data (maximum of last 7 days)  
          1. Click on 3 dots  
          2. Click on Run Workflow  
          3. Enter the starting time from when you want to ingest the data from GTI servers related to the ransomware threat list.  
          4. Click on Run Workflow  
   12. Get First Stage Delivery Actors Threat List from GTI  
       1. Click on Edit in Builder button  
       2. Click on First Stage Delivery Actors Threat List action  
       3. Add query parameter to filter the threat list IOCs (Optional)  
       4. Once added, click on Save Step  
       5. Click on the toggle button to enable the workflow  
       6. To ingest past data (maximum of last 7 days)  
          1. Click on 3 dots  
          2. Click on Run Workflow  
          3. Enter the starting time from when you want to ingest the data from GTI servers related to the ransomware threat list.  
          4. Click on Run Workflow  
   13. Get Vulnerability Weaponization Threat List from GTI  
       1. Click on Edit in Builder button  
       2. Click on Vulnerability Weaponization Threat List action  
       3. Add query parameter to filter the threat list IOCs (Optional)  
       4. Once added, click on Save Step  
       5. Click on the toggle button to enable the workflow  
       6. To ingest past data (maximum of last 7 days)  
          1. Click on 3 dots  
          2. Click on Run Workflow  
          3. Enter the starting time from when you want to ingest the data from GTI servers related to the ransomware threat list.  
          4. Click on Run Workflow  
   14. Get Infostealers Threat List from GTI  
       1. Click on Edit in Builder button  
       2. Click on Infostealers Threat List action  
       3. Add query parameter to filter the threat list IOCs (Optional)  
       4. Once added, click on Save Step  
       5. Click on the toggle button to enable the workflow  
       6. To ingest past data (maximum of last 7 days)  
          1. Click on 3 dots  
          2. Click on Run Workflow  
          3. Enter the starting time from when you want to ingest the data from GTI servers related to the ransomware threat list.  
          4. Click on Run Workflow  
4. **Manual Workflows:**  
   1. Get Comments from GTI:  
      1. Click on Edit in Builder button  
      2. Click on Get Comments action, and update the parameters as per requirement. e.g. if user want to get comments for Domain google.com, then update the IOC Type to Domain, and add **google.com** in the IOC Value  
      3. Once updated, click on Save Step button  
      4. Enable the workflow by clicking on the toggle button  
      5. Once activated, navigate to Workflows page  
      6. Click on 3 dots present on the Get Comments workflow, post that click on Run Workflow to retrieve the Comments for the provided IOC Type, and IOC Value  
   2. Add Comment to IOC on GTI:  
      1. Click on Edit in Builder button  
         1. Click on Add Comment action, and update the parameters as per requirement. e.g. if user wants to add comment for URL, then update the IOC type to Url, add the url value in IOC Value, and comment in the comment textbox  
         2. Once added, click on Save Step  
         3. Enable the workflow by clicking on the toggle button  
         4. Once activated, navigate to Workflows page  
         5. Click on 3 dots present on the Add IOC Comment workflow, post that click on Run Workflow to add the Comment for specified IOC  
   3. Delete IOC Comment on GTI: Users can delete comments on the GTI platform only if they have added the comment to the GTI platform with the help of the Add Comment workflow. If the user has previously added a comment with the help of Add Comment workflow, then they have received an ID related to that particular added comment on GTI platform. Users will require that ID to delete the comment from the GTI platform.  
      1. Click on the toggle button to activate the workflow  
      2. Once it is activated, click on 3 dots present on the right hand side of the workflow tile bar. You will be able to visualise various options, one of them would be Run workflow  
      3. Click on Run Workflow option, which will open a pop-up to add the comment ID using which comment will be removed from the GTI platform  
         1. Once added, click on Run workflow.  
   4. Scan File using GTI **:**  
      1. Click on Edit in Builder button  
      2. Click on Scan File action, and add the parameters value as per requirement.  
      3. Users can either upload the file or can provide the base64 encoded format of the file in the Content textbox  
         1. Add appropriate filename (Optional)  
      4. Once added, click on Save Step  
      5. Click on the toggle button to enable the workflow  
      6. Click on the 3 dots, post that click on Run workflow to execute the workflow  
      7. Once the workflow execution is completed, report will be generated and will be sent to InsightIDR with the help of Webhook  
   5. Scan Private File using GTI:  
      1. Click on Edit in Builder button  
      2. Click on Scan Private File action, and add values in all the required parameters  
      3. Users can either upload the file or can provide the base64 encoded format of the file in the Content textbox  
         1. Add appropriate filename (Optional)  
      4. Select Yes if the provided file requires Internet connection in Enable Internet Dropdown  
      5. Once added, click on Save Step  
      6. Click on the toggle button to activate the workflow  
      7. Once activated, click on the 3 dots. Post that, click on Run workflow to execute the workflow  
      8. Once the workflow execution is completed, report will be generated and will be sent to InsightIDR with the help of Webhook  
   6. Scan URL using GTI:  
      1. Click on the toggle button to activate the workflow  
      2. Once it is activated, click on 3 dots present on the right hand side of the workflow tile bar. You will be able to visualise various options, one of them would be Run workflow.  
      3. Click on Run Workflow option, which will open a pop-up to add the URL on which analysis will be performed  
      4. Once the url has been added, click on Run Workflow.  
   7. Scan Private URL using GTI:  
      1. Click on the toggle button to activate the workflow  
      2. Once it is activated, click on 3 dots present on the right hand side of the workflow tile bar. You will be able to visualise various options, one of them would be Run workflow.  
      3. Click on Run Workflow option, which will open a pop-up to add the URL which will privately submit it to GTI and analysis will be performed  
      4. Once the url has been added, click on Run Workflow.  
   8. Get CVE Sources using GTI:  
      1. Click on Edit in Builder button  
      2. Click on Get CVE Sources action, and add Vulnerability ID in Vulnerability ID parameter  
      3. Once added, click on Save Step button  
      4. Enable the workflow by clicking on the toggle button  
      5. Once activated, navigate to Workflows page  
      6. Click on 3 dots present on the Get CVE Sources workflow, post that click on Run Workflow to get the sources for specified vulnerability  
5. **Get ASM Issues from GTI:** ASM Issues workflow runs on hourly basis fetching the user’s system information configured on Google Threat Intelligence platform.  
   1. Click on Edit in Builder button  
   2. Click on Get ASM Issues action, and update the parameters as per requirement.  
   3. The default parameter value for data limit is 1000\. Users can update the value from 1 to 1000 as per their requirement. (Optional)  
   4. Add the historical time from when the user wants to retrieve the data from. Maximum last 5 days data can be retrieved from GTI. (Required)  
   5. Add the Search String on the basis of which data should be retrieved from the GTI. (Optional)  
   6. Once these fields are updated click on the Save Step button.  
   7. Enable the workflow by clicking on the toggle button.  
   8. Once activated, the workflow will run automatically at an interval of 1 hr to fetch the data from the GTI platform and ingestion will happen onto the InsightIDR platform in the form of events. (**Note:** This means that there is no bidirectional flow, and users cannot modify the status of the ASM Issues from the rapid7 platform)  
6. **Get DTM Alerts from GTI:** DTM Alerts workflow runs on hourly basis fetching the user’s curated monitoring data from Google Threat Intelligence platform.  
   1. Click on Edit in Builder button  
   2. Click on Get DTM Alerts action. There are various parameters that users can set to fetch DTM alerts data from GTI.  
   3. The default parameter value for data limit is 1000\. Users can update the value from 1 to 1000 as per their requirement. (Optional)  
   4. Add monitor IDs in comma separated string values in the array format. (Optional)  
   5. Add the time in the Since parameter, from when the user wants to retrieve the historical data. Maximum last 5 days data can be retrieved from GTI. (Required)  
   6. Add status in comma separated string values in the array format. (Optional)  
   7. Add alert type in comma separated string values in the array format. (Optional)  
   8. Add tags in comma separated string values in the array format. (Optional)  
   9. Add severity in comma separated string values in the array format. (Optional)  
   10. Add MScore GTE value to filter the alerts with mscores greater than or equal to the given value. (Optional)  
   11. Add a simple Lucene query string in the search parameter to filter the alerts on the basis of that. (Optional)  
   12. Once these fields are updated click on the Save Step button.  
   13. Enable the workflow by clicking on the toggle button.  
   14. Once activated, the workflow will run automatically at an interval of 1 hr to fetch the data from the GTI platform and ingestion will happen onto the InsightIDR platform in the form of events. (**Note:** This means that there is no bidirectional flow, and users cannot modify the status of the DTM Alerts from the rapid7 platform.)