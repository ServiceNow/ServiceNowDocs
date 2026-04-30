---
title: Create a data lineage for a processing activity
description: Establish a data lineage to visualize data consumption, sharing, and the associated risks for a processing activity. Each processing activity involves multiple information objects classified as personal information. These objects exchange data with various other entities, making it essential to establish a data lineage or hierarchy that tracks where personal data is shared. This understanding helps mitigate privacy-related risks.
locale: en-US
release: xanadu
product: Privacy Workspace
classification: privacy-workspace
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Use, Privacy Management, Governance, Risk, and Compliance]
---

# Create a data lineage for a processing activity

Establish a data lineage to visualize data consumption, sharing, and the associated risks for a processing activity. Each processing activity involves multiple information objects classified as personal information. These objects exchange data with various other entities, making it essential to establish a data lineage or hierarchy that tracks where personal data is shared. This understanding helps mitigate privacy-related risks.

## Before you begin

Role required: sn\_privacy.business\_user

## About this task

Although data lineage can be created from the Hierarchy tab of a processing activity, this procedure shows how to create it from the Data Lineage page, which offers a visual representation of the hierarchy. When creating the hierarchy, make sure not to use the same asset as both the source and the destination.

When you create the hierarchy of relationships, you can view up to five levels of relationships. However, you can configure the number of levels according to your preference in the **sn\_privacy.nodemap.maxLevel** property.

## Procedure

1.  Navigate to **All** &gt; **Privacy Management** &gt; **Privacy Workspace** &gt; **Processing activities** &gt; **All processing activities**.

2.  Open the processing activity to which you want to create data lineage.

3.  On the form, select **Data lineage**.

4.  Select the record for which you want to create a relationship.

5.  Select **Create new relationship**.

6.  In the New relationship dialog box, fill in the fields.

<table id="table_fhc_fj4_xbc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Primary Node

</td><td>

Record for which you're creating the relationship. While this field is automatically set to the record that is selected, you can change the node.

</td></tr><tr><td>

Hierarchy

</td><td>

Level at which you want to create the relationship. The choices are as follows.-   **Data coming from**: If you select this option, the data will flow to the levels above the primary node.
-   **Data sent to**: If you select this option, the data will flow to the levels below the primary node.


</td></tr><tr><td>

Related to

</td><td>

CMDB record with which the personal data is associated. For example, if the primary node is related to a business application, a business process, a business service, and so on. After you make a selection in this field, select the required records. This field provides the following choices.-   **Business Application**
-   **Business Process**
-   **Business Service**
-   **Company**
-   **Vendor**
-   **Entity**
-   **Processing Activity**


</td></tr><tr><td>

Relationship Type

</td><td>

Nature of the relationship between the personal data and the selected item. The choices are as follows.-   **Depends**: Indicates that the personal data is reliant on the specified item.
-   **Contains**: Specifies that the item includes or holds the personal data.
-   **Sends data to**: Shows that the item transmits the personal data to another application or party.
-   **Uses**: Demonstrates that the item utilizes the personal data for its operations or processes.
**Note:** You can add more choices to appear in this field in the sn\_grc\_choice table.

</td></tr><tr><td>

Description

</td><td>

Brief description of the relationship.

</td></tr></tbody>
</table>7.  Select **Create**.

    The relationship node is created.

8.  To view the inflow and outflow of data for a particular record, select the ![Recenter nodemap](../image/recenter-nodemap.jpg) icon.

9.  To view the details of the processing activity and the entity if a processing activity is associated with the selected record, select the ![Details](../image/details-icon.jpg) icon.


**Parent Topic:**[Using Privacy Management](../concept/using-privacy-mgmt.md)

