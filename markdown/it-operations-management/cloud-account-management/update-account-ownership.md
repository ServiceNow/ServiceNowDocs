---
title: Update cloud account details
description: Keep account details up to date so you can identify and resolve policy violations effectively.
locale: en-US
release: zurich
product: Cloud Account Management
classification: cloud-account-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
keywords: [Cloud Workspace Account Details, Cloud Workspace Ownership]
breadcrumb: [Managing cloud accounts, Use, Cloud Account Management, ITOM Cloud Accelerate, IT Operations Management]
---

# Update cloud account details

Keep account details up to date so you can identify and resolve policy violations effectively.

## Before you begin

Role required: sn\_itom\_cam.cw\_admin

## Procedure

1.  Navigate to **All** &gt; **Cloud Workspace** &gt; **View accounts**.

2.  Under **All cloud accounts**, select an account.

    The **Overview** tab displays General details, Ownership details, and Certification details.

3.  Update account information if necessary.

    1.  Select the Edit icon \(![edit icon](../image/edit-icon-workspace.png)\).

    2.  Update the information.

        |Fields|Description|
        |------|-----------|
        |Cost center|Cost center name to associate with this account.|
        |Business unit|Business unit name to associate with this account.|
        |Application service|The project or application to associate with this account.|
        |Department|Department name to associate with this account.|

4.  Update the account owner details if necessary.

    1.  Select the Edit icon \(![Edit icon](../image/edit-icon-workspace.png)\).

    2.  Select the account owner from the **Account Owner** from the drop-down list.

    3.  Select the primary teams from the**Primary Teams** from the drop-down list.

    4.  Select the secondary teams from the**Secondary Teams** from the drop-down list.

5.  Propagate the name change to associated cloud assets or stop propagation.

    -   Propagate the owner information to the cloud account and all associated CIs directly linked to the cloud account, overriding any existing owner information, by selecting the **Propagate Ownership to Cloud Assets** check-box.

        Associated CIs include items like S3 bucket or VM. CIs not directly linked to the cloud account include things like Azure Availability Zones.

    -   To remove future propagation of the owner information, clear the **Propagate Ownership to Cloud Assets** check-box.

        The owner name is no longer assigned to newly associated CIs but is retained for the existing ones.

    **Note:**

    If you have a large number of CIs, the propagation might take some time and changes might not be reflected immediately. You can check the progress by accessing the sn\_itom\_cam\_subscription\_account\_batch\_job\_list table and checking the status of "owner\_name" jobs listed in the **Parameters** column.

6.  Select the Save icon \(![save icon](../image/save-icon-workspace.png)\).


