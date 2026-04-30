---
title: Using Instance Scan dashboard
description: The Instance Scan dashboard is a system wide visual representation of the health of your instance. The dashboard helps you to manage and analyze the results of full scan against your instance.
locale: en-US
release: xanadu
product: Instance Scan
classification: instance-scan
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Instance Scan, Maintain and monitor, Administer the ServiceNow AI Platform]
---

# Using Instance Scan dashboard

The Instance Scan dashboard is a system wide visual representation of the health of your instance. The dashboard helps you to manage and analyze the results of full scan against your instance.

The dashboard offers several options to filter your search results to find the exact check finding that might be causing some issues. The **Instance Scan Category** is the filter picker that shows all the categories of all the checks that were scanned. You can select the type of scan category that you want the dashboard to display as a part of the scan results. **Instance Scan Priority** helps you to select the priority level of the results to decide which scan results must be addressed first. This priority level is often referred to as the rating level of the scans.

![Image showing the categories and priorities of a scan](../image/hs-category.png)

**Note:** The dashboard is only applicable for full scans. The **Instance Scan Category** is only available if you have data or a finding in the result set that are applicable to the categories.

For example, you can use the dashboard to compare the results of the check findings. If you see a sudden change in the number of check findings, select the particular scan result from the Scan Results List.

![Image showing sudden change in the number of findings](../image/hs-findings.png)

You can review all the findings for the scan that generated an unexpected number of findings. This list displays all the findings that are related to one or more of all the scans.

![Image showing the related list of the health scan](../image/hs-list.png)

You can also directly select the column with the required findings to display the related list for a particular scan.

![Image showing how to select a particular scan result column](../image/hs-click.png)

The list also indicates the source from which the finding has been retrieved. You can export the list view data to an external source such as a .csv file or an .xlsv file for further performance comparison and analysis.

