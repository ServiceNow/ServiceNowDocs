---
title: Create taxonomy nodes
description: Create an unlimited number of nodes, or branches, and add them to your service portfolio taxonomy layers. By configuring taxonomy nodes, you can successfully achieve a highly detailed and organized service portfolio containing multiple elemental layers—from general to specific.
locale: en-US
release: australia
product: Service Portfolio Management
classification: service-portfolio-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Service Portfolio Management taxonomy, Create a portfolio, Use, Service Portfolio Management, IT Service Management]
---

# Create taxonomy nodes

Create an unlimited number of nodes, or branches, and add them to your service portfolio taxonomy layers. By configuring taxonomy nodes, you can successfully achieve a highly detailed and organized service portfolio containing multiple elemental layers—from general to specific.

## Before you begin

Role required: portfolio\_admin

## About this task

Add new nodes as needed and edit existing nodes, as well as reparent nodes or delete nodes. You can reparent a node to another node at the same taxonomy layer.

In Service Portfolio Management, taxonomy nodes typically represent service types within the configured taxonomy layers. These types act as containers for child nodes or services. Examples for an IT services portfolio could include the following taxonomy nodes:

-   Data Center Management
-   Hardware Support
-   Software Management

If the Service Portfolio Management Taxonomy Content Pack \[com.snc.spm.content\] plugin sample data is activated on your instance, review the provided taxonomy data to gain an understanding of how to best define your taxonomy layers. Refer to [Activate Service Portfolio Management Sample Content Pack](activate-SPM2-content-pack-plugin.md) for more details.

## Procedure

1.  Navigate to **Service Portfolio Management** &gt; **Taxonomy Nodes** and select **New**.

    To edit an existing taxonomy node, select the name of the taxonomy node to open the form. Change any of the form field data as needed. To delete an existing node, select **Delete**.

2.  Fill in or edit the form fields.

<table id="table_obz_2jh_ygb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Unique name that defines the purpose of the node.

</td></tr><tr><td>

Short description

</td><td>

Brief detail about the taxonomy node purpose.

</td></tr><tr><td>

Description

</td><td>

In-depth details about the node.

</td></tr><tr><td>

Service portfolio

</td><td>

Service portfolio this taxonomy node is associated with.

</td></tr><tr><td>

Taxonomy layer

</td><td>

Taxonomy layer this node is associated with.

</td></tr><tr><td>

Parent

</td><td>

Taxonomy node to which the taxonomy node is associated. Use this form field to reparent a node at the same taxonomy level.

</td></tr><tr><td>

Owned by

</td><td>

Owner of the taxonomy node.

</td></tr><tr><td>

Valid from

</td><td>

The date the taxonomy code is valid.

</td></tr><tr><td>

Valid to

</td><td>

The date the taxonomy code is no longer valid.

</td></tr><tr><td>

Performance score**Note:** Appears with a Service Owner Workspace subscription.

</td><td>

Most recent performance score for this node. The performance score is calculated by a nightly script.**Note:** Only an admin can change the score, if necessary.

</td></tr></tbody>
</table>3.  **Submit** your taxonomy node.

    Alternatively, you can select **Update** after editing an existing taxonomy node.

4.  Edit or define the taxonomy node weights.

    If available, select the **Edit Weights** related link to edit existing child service weights or child node weights. Alternatively, you can navigate to **Service Portfolio Management** &gt; **Taxonomy Nodes** and find a node in the list. Select to open the form.

    **Note:** The **Edit Weights** related link appears with a Service Owner Workspace subscription. Weight values for associated child nodes are specified at the service offering level via the **Edit Metric Weights** related link on the Service Offering form.

5.  Specify weight values for each associated child node.

    Total weight must equal 100 percent. For more information on weights and specifying weight values, refer to .

6.  Review the related list records.

    Depending on the type of node, whether it is a leaf node or a non-leaf node, related lists display the following associated data.

<table id="choicetable_wpd_xth_ygb"><tbody><tr><td id="d278251e315">

**Taxonomy Nodes**

</td><td>

List of all associated child nodes. You can edit an existing child node by selecting a Taxonomy Node name. Create a new child node by clicking **New** and completing the **Taxonomy Node** form.

</td></tr><tr><td id="d278251e330">

**Services**

</td><td>

List of all associated services shown for leaf nodes. Edit the list by selecting **Edit** and making changes to the form. You can select a service in the Related List to modify and update. Create a new associated service by clicking **New** and completing the **Service** form. Refer to [Create a service in Service Portfolio Management](create-or-modify-SPM2-services.md).

</td></tr></tbody>
</table>
**Parent Topic:**[Service Portfolio Management taxonomy](../concept/SPM2-taxonomy.md)

