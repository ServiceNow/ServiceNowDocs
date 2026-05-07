---
title: Create TAXII Collection
description: Use this section to learn how to configure and define TAXII collections for sharing intelligence.
locale: en-US
release: australia
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Exploring TAXII Outbound Server, Configuring Threat Intelligence External Sharing, Administer, Threat Intelligence Security Center, Security Operations]
---

# Create TAXII Collection

Use this section to learn how to configure and define TAXII collections for sharing intelligence.

## Before you begin

Role required: sn\_sec\_tisc.admin

## Procedure

1.  Navigate to **Workspaces** &gt; **Threat Intelligence Security Center** &gt; **Administration** &gt; **TAXII Outbound Server**.

2.  Select **TAXII Collections**.

3.  Select **New** to create a TAXII Collection.

4.  On the form, fill in the fields.

<table id="table_syl_ztc_mfc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the TAXII collection.

</td></tr><tr><td>

Description

</td><td>

Description of the TAXII collection.

</td></tr><tr><td>

Spec Version

</td><td>

Specifies the version of the TAXII used for data formatting and exchange.**Note:** The only supported spec version for data formatting is 2.1.

</td></tr><tr><td>

Expiry period \(days\)

</td><td>

Specifies the number of days after which the records added to the TAXII Collection expires. **Note:** After expiration, the records will be marked as inactive and subsequently removed from the collection.

</td></tr><tr><td>

Enable Versioning

</td><td>

Select this check box to enable versioning for the records being added to the TAXII collection.**Note:** When a record is added to a TAXII collection and if it differs from its previous version, the application will add the new version only if the versioning is enabled.

If the versioning is not enabled, the existing record will be overwritten with the updated data.

</td></tr><tr><td>

Access to all TAXII API users

</td><td>

Specifies access for TAXII users. When selected, all users assigned the TAXII Server API role will be granted permission to retrieve data from this collection.**Note:** When the **Access to all TAXII API users** field is not selected, only the users specified in this field will have access to the TAXII collection records.

</td></tr><tr><td>

Read Access

</td><td>

When the **Access to all TAXII API users** field is not selected, then only the users specified in this field will be able to access the TAXII collection records.

</td></tr></tbody>
</table>5.  Select **Save**.

6.  **System property to add records**

    The system property for TAXII collections limits the number of records that can be added to a TAXII collection.

    The following is the system property for the TAXII Collection configuration:

<table id="table_rzw_ds3_4fc"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_sec\_tisc.taxii\_server\_collection\_record\_limit

</td><td>

Maximum number of records that can be added to an outbound TAXII server collection.The default value is 10000.

</td></tr></tbody>
</table>7.  View the system property information for adding records to the TAXII collection.

8.  Navigate to the **Flow Designer** &gt; **Flows**.

    This navigation displays the template flow for adding TAXII Collections.

9.  Select the **Automatically add threat intelligence to a TAXII Collection** flow.

10. Navigate to the **Flow Designer** &gt; **Actions**.

11. **Adding records to the TAXII Collection**

    Currently, the only method for adding records to the TAXII server collection is via an automated process. The following are the two actions that are provisioned in the base system:

    1.  **Add Record to TAXII Server Collection**
    2.  **Add Records to TAXII Server Collection**
12. View the respective TAXII server collection action.


**Parent Topic:**[Exploring TAXII Outbound Server](tisc-taxii-outbound-server.md)

**Related topics**  


[Automated Sharing of TAXII Collections](../task/tisc-automated-share-taxii.md)

[Viewing TAXII Collection Records](tisc-view-taxii-collection.md)

[Automated Sharing of TAXII Collections](../task/tisc-automated-share-taxii.md)

[Configuring Outbound Intel Sharing Templates](../task/tisc-intel-sharing-templates.md)

