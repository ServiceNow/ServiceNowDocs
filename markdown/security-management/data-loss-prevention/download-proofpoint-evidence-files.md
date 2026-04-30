---
title: Download DLP incidents evidence files on Proofpoint
description: Download DLP incident evidence files that violate the DLP policy on Proofpoint.
locale: en-US
release: yokohama
product: Data Loss Prevention
classification: data-loss-prevention
topic_type: task
last_updated: "2024-09-19"
reading_time_minutes: 1
breadcrumb: [Create a Profile for Proofpoint DLP integration, Data Loss Prevention Incident Response Integration with Proofpoint, DLP integrations, Data Loss Prevention Incident Response, Security Operations]
---

# Download DLP incidents evidence files on Proofpoint

Download DLP incident evidence files that violate the DLP policy on Proofpoint.

## Before you begin

Download this file onto your local machine from the DLP IR Analyst workspace and DLP IR End user workspace.

**Note:** **Download File** action will be available only for the approvers who has the secure file access role \(applicable only for ServiceNow storage type and there is no role needed for external storage\) on the DLP IR End User workspace.

Make sure to enable **Should downloading the violating file of the reported incident be allowed** property available under the **Settings** is enabled \(or set to active true\).

Role required:

-   sn\_dlir.analyst
-   sn\_dlir.secure\_file\_download

**Note:** Any approver with this role for internal storage only can download the file.

## Procedure

1.  Navigate to **All** &gt; **DLP Incident Management** &gt; **DLP Analyst Workspace**.

2.  Open a Proofpoint DLP incident with the Scan source as **Email SMTP**.

3.  Click **Download File**.

4.  **For the approver to view the Download File action, follow the below steps:**
5.  Navigate to **All** &gt; **DLP Incident Management** &gt; **DLP User Workspace**.

    My DLP Incidents page will be displayed in a new tab.

6.  Select **My Approvals** module available under My DLP Incidents module.

    My Approvals list view will be displayed.

7.  Open an approval request record which is raised for Proofpoint DLP Incident with Scan source Email SMTP.

8.  Click on info icon \(i\) available on the DLP Incident field on the form view.

9.  Click **Download File**.


## Result

After performing this action, the file that violated the DLP policy on Proofpoint will be downloaded to the user’s local machine.

**Note:**

DLP admin can also control the access of **Download File** action by disabling the **Should downloading the violating file of the reported incident be allowed** setting from the Advanced Settings page. For more information, see [Configure advanced settings for Data Loss Prevention Incident Response](https://servicenow.com/docs/bundle/xanadu-security-management/page/product/data-loss-prevention/task/configure-advanced-settings-dlp.html).

**Parent Topic:**[Create a Profile for Proofpoint DLP integration](create-profile-proofpoint-dlp-integration.md)

