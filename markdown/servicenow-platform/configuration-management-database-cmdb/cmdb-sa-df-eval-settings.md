---
title: Evaluate CMDB settings for Data Foundations
description: Identify and evaluate settings including CMDB reconciliation rules, CI creation business rules, and CMDB Data Manager policies that support data quality and life cycle management for your principal classes.
locale: en-US
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Analyze CMDB settings, Use Data Foundations advisor, CMDB success advisor, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Evaluate CMDB settings for Data Foundations

Identify and evaluate settings including CMDB reconciliation rules, CI creation business rules, and CMDB Data Manager policies that support data quality and life cycle management for your principal classes.

## Before you begin

Role required: sn\_cmdb\_admin

## Procedure

1.  Navigate to the CMDB success advisor landing page.

2.  On the Data Foundations card, select **View insights**.

3.  Select the **Settings** tab.

4.  Select a status tile to view settings by category.

    |Tile|Description|
    |----|-----------|
    |**All**|Total number of evaluated settings.|
    |**Ideal**|Settings that follow general guidelines.|
    |**Requires attention**|Settings that are inactive, incorrectly configured, or missing.|

5.  Evaluate each setting that requires attention and use the available actions to open the related configuration pages and make updates.

<table id="choicetable_acr_fw5_ggc"><thead><tr><th align="left" id="d262666e147">

Action

</th><th align="left" id="d262666e150">

Description

</th></tr></thead><tbody><tr><td id="d262666e156">

**Manage policies**

</td><td>

Opens the Data Manager overview page where you can create or update life cycle policies \(archive, attestation, certification, delete, retire\) for your principal classes.

</td></tr><tr><td id="d262666e165">

**Create policy**

</td><td>

Opens the New policy form to create a policy for a principal class. The **Create policy** action is available in the policy summary dialog box displayed after selecting the policy coverage count in the **Classes with active policies** column within the Review Data Manager policies section.

</td></tr><tr><td id="d262666e182">

**View attributes**

</td><td>

Opens the CI class attributes list to review and manage custom attributes for your principal classes. Use this action to identify classes with more than 10 active custom attributes.

</td></tr><tr><td id="d262666e191">

**Configure property**

</td><td>

Opens the system property configuration page to enable or disable CI creation from assets using IRE for applicable principal classes.

</td></tr><tr><td id="d262666e201">

**CI Class Manager**

</td><td>

Opens CI Class Manager to add the **Managed by group** field to CI classes that are missing it, or to configure reconciliation rules for principal classes.

</td></tr></tbody>
</table>    **Tip:** Select **Learn more** next to a setting to open a related help topic in a new browser tab or window with additional details about that setting.

6.  To view any updated configuration status on the **Settings** tab, select the refresh icon ![](../../api-insights/image/refresh-list.png).


**Related topics**  


[Administer CMDB Data Manager](../../configuration-management/concept/administer-data-manager.md)

