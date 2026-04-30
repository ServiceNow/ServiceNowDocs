---
title: Download evidence files
description: Download DLP incident evidence files that violate the DLP policy on Symantec.
locale: en-US
release: yokohama
product: Data Loss Prevention
classification: data-loss-prevention
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Create a profile for Symantec DLP integration, Symantec Integration for Data Loss Prevention Incident Response, DLP integrations, Data Loss Prevention Incident Response, Security Operations]
---

# Download evidence files

Download DLP incident evidence files that violate the DLP policy on Symantec.

## Before you begin

Download this file onto your local machine from the DLP IR Analyst workspace and DLP IR End user workspace. Download Files action will be available only for the approvers on the DLP IR End User workspace.

Role required:

-   sn\_dlir.analyst
-   sn\_dlir.secure\_file\_download \(any approver with this role\)

## Procedure

1.  Navigate to **All** &gt; **Symantec DLP Integration** &gt; **Setting**.

2.  Enable **Should downloading the violating file of the reported incident be allowed** property.

    After you enable this property, you will now be able to see the **Download File** action on the DLP Analyst Workspace for any Symantec DLP incident.

3.  Navigate to **All** &gt; **DLP Incident Management** &gt; **DLP Analyst Workspace**.

4.  Open a DLP incident record which is ingested from Symantec source.

5.  Click **Download File**.

    **Note:** The file that violated the DLP policy on Symantec will be downloaded to the user’s local machine.

    For the approver to view the Download File action, follow below mentioned steps:

6.  Navigate to **All** &gt; **DLP Incident Management** &gt; **DLP User Workspace**.

    My DLP Incidents page will be displayed in a new tab.

7.  Select **My Approvals** module available under My DLP Incidents module.

    My Approvals list view will be displayed.

8.  Open an approval request record which is raised for Symantec DLP Incident.

9.  Click on info icon \(i\) available on the DLP Incident field in the form view.

10. Click **Download File**.


## Result

After performing this action, the evidence file in either ZIP format \(if the incident has violations in multiple components and/or the original message data is also available\) or a single file \(if incident has violations in single component or only original message data is available\) will be downloaded to the user's local machine.

**Note:** As a DLP admin, you can control the access of **Download File** action by disabling the **Should downloading the violating file of the reported incident be allowed**option from the **Advanced Settings** page. For more information, see [Configure advanced settings for Data Loss Prevention Incident Response](https://servicenow.com/docs/bundle/washingtondc-security-management/page/product/data-loss-prevention/task/configure-advanced-settings-dlp.html).

**Parent Topic:**[Create a profile for Symantec DLP integration](create-profile-symantec-dlp.md)

