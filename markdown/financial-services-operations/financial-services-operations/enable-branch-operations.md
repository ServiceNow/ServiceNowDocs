---
title: Enable branch operations
description: You can enable a set of branch operations features so that managers can gain views into operational performance and cases across the branches they manage.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 5
---

# Enable branch operations

You can enable a set of branch operations features so that managers can gain views into operational performance and cases across the branches they manage.

Branch banking enables banks to provide banking services through a wide network of branch offices, and provides customers the option to conveniently bank with a branch in their vicinity. Using branch operations features for FSO, Location managers responsible for managing operations can view performance metrics, and view and create cases, for the branches that they manage.

Branch operations for FSO includes these components:

-   Location manager contributor role \(sn\_bom.location\_manager\_contributor\)
-   Branch location support
-   Branch location field on case tables and records
-   Location manager workspace with landing page, case list, and metrics dashboard
-   Demo data

## FSO Applications that support branch operations

These FSO applications support branch operations by installing the branch location field and demo data components.

-   Financial Services Card Operations
-   Financial Services Complaint Management
-   Financial Services Credit Operations
-   Financial Services Business Lifecycle
-   Financial Services Client Lifecycle
-   Financial Services Business Deposit Operations
-   Financial Services Personal Deposit Operations
-   Financial Services Business Loan Operations
-   Financial Services Personal Loan Operations
-   Financial Services Payment Operations
-   Financial Services Treasury Operations

The following additional plugins must be installed to fully enable branch operations.

## Required plugins to enable branch operations

The following plugins install the Location manager contributor role and workspace, location table field, branch location support, and demo data components that comprise branch operations.

-   Financial Services Operations \(FSO\) application plugin - Applicable FSO application plugins install branch operations demo data and add the branch location field on case tables and records.
-   Financial Services Operations Core application plugin - The Financial Services Operations Core application plugin \(sn\_bom\) is automatically installed when you install an applicable FSO application. The sn\_bom plugin installs the Location manager contributor role \(sn\_bom.location\_manager\_contributor\). The Location manager contributor role enables a personalized Workspace with dashboard for viewing metrics and managing cases. The role can collect and submit case documents, and add staff members to a branch location.

    **Note:** The Business Location plugin must be activated for the sn\_bom.location\_manager\_contributor role to be enabled. For more information, see [https://servicenow.com/docs/bundle/tokyo-customer-service-management/page/product/customer-service-management/task/activate-business-location.html](https://servicenow.com/docs/bundle/tokyo-customer-service-management/page/product/customer-service-management/task/activate-business-location.html)

-   Business Location plugin \(com.snc.business\_location\) - The com.snc.business\_location plugin enables support for banks that interact with customers through branches. The com.snc.business\_location plugin automatically activates the Service Organization plugin \(com.snc.service\_organization\), which enables support for internal branches. For information on activating the Business Location plugin, see [Activate business locations](https://www.servicenow.com/docs/access?context=activate-business-location&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US).

## Location manager contributor workspace

The Location manager contributor workspace contains these pages.

-   Customized landing page under the business location associated with the role. The landing page shows an overview of open cases, breakdown of open cases by application, and quick links to each installed application that enable Location managers to initiate creating cases for customers.
-   List view of cases assigned to branches managed by the role. The Location manager contributor role can open a case form record to edit the branch location field. The branch location field is editable until a case is closed.
-   Branch Performance Metrics dashboard page

The Location manager contributor role can select metric numbers from the landing or Branch Performance Metrics dashboard pages to drill down to a breakdown list or KPI Details performance analytics view.

For more information about analytics and reporting for Financial Services Operations, see [Platform Analytics Solutions for Financial Services Operations](../../../use/application-content-packs/concept/fso-content-pack.md) and [KPI Details](https://www.servicenow.com/docs/access?context=kpi-details&version=xanadu&pubname=xanadu-now-intelligence&ft:locale=en-US).

For more information on workspaces in Financial Services Operations, see [Workspaces](fso-workspace.md).

## Branch Performance Metrics dashboard

The Branch Performance Metrics dashboard enables Location managers to get a operational and trend insights into how their team and businesses are performing across branches they manage. The dashboard shows the following metrics.

|Indicator|Description|
|---------|-----------|
|Closed cases|Number of cases closed in the last 30 days for the branch. The number and percentage change in the current period appears under the total percentage.|
|SLA met|Number and percentage of SLAs met across all FSO cases in the last 30 days for the branch location. The number and percentage change in the current period appears under the total percentage.|
|SLA breached|Number of SLAs breached across all FSO cases in the last 30 days for the branch location.|
|CSAT score|Percentage average customer satisfaction across all FSO cases based on surveys completed for the branch location in the last 30 days. The number and percentage change in the current period appears under the total percentage. For more information about CSAT, see [Customer service satisfaction surveys](https://www.servicenow.com/docs/access?context=c_CustomerServiceSatisfactionSurvey&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US).|
|Trend of SLA met and breached closed cases|Trend of closed cases with SLAs breached vs closed cases with SLAs not breached in last 30 days for the branch, trended weekly.|
|Trend of closed, open and created cases|Trend of closed cases, open cases, and cases created in the last 30 days for the branch location, trended weekly.|

|Indicator|Description|
|---------|-----------|
|Customers onboarded|Number of customers onboarded in last 30 days for the branch location, trended by week.|
|Closed cases|Number of closed cases with SLAs breached vs. closed cases with SLAs not breached in last 30 days for the branch location, trended by week.|
|SLA met|Percentage of SLAs met across all FSO cases in the last 30 days for the branch location.|
|SLA breached|Percentage of SLAs breached across all FSO cases in the last 30 days for the branch location.|
|Average time to close|Average time to close cases in the last 30 days for the branch location.|
|Trend of \[application\] cases created|Trend of application cases created in the last 30 days for the branch location, trended by week.|
|Initial deposit received|Initial deposit amount received from checking and savings deposit accounts opened in the last 30 days for the branch location.|
|Write offs|Number of write-offs from cases closed in the last 30 days for the branch location.|

**Parent Topic:**[Configuring Financial Services Operations](setting-up-fso-applications.md)

