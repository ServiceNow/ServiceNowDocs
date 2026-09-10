---
title: New hierarchy relationship forms in Privacy Management
description: When creating a new hierarchy relationship in Privacy Management, you first define how a node is related to another. Then, you provide details for each related node.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/privacy-workspace/new-relationship-forms.html
release: australia
product: Privacy Workspace
classification: privacy-workspace
topic_type: reference
last_updated: "2026-08-19"
reading_time_minutes: 4
breadcrumb: [Create a hierarchy relationship, Use, Privacy Management, Governance, Risk, and Compliance]
---

# New hierarchy relationship forms in Privacy Management

When creating a new hierarchy relationship in Privacy Management, you first define how a node is related to another. Then, you provide details for each related node.

## Define relationships form

<table id="table_define_relationship_form"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Primary record

</td><td>

Processing activity you're currently working on. Pre-filled and can't be changed.

</td></tr><tr><td>

Primary node

</td><td>

Node for which you're creating the relationship. By default, this field is pre-filled with the current processing activity. You can change it to another node that is already linked to the processing activity.

</td></tr><tr><td>

Primary node location

</td><td>

Location of the primary node.

 It is auto-populated from the location set on the node. If node location isn't specified, the associated entity location is used. If that isn't specified either, the associated CMDB record location is used.

 You can edit this field to change the auto-populated value.

</td></tr><tr><td>

Relationship type

</td><td>

Relationship between the primary node and the related node. The built-in relationship types are:-   **Depends on**: Primary node can’t function without the related node.

For example, a customer onboarding processing activity depends on an identity verification application because onboarding can't proceed without verifying a customer's identity.

-   **Contains**: Primary node is the parent activity that includes the related node as a sub-activity.

For example, an employee management processing activity contains payroll processing and benefits enrollment as sub-activities.

-   **Contained by**: Inverse of the **Contains** relationship type. When you create a **Contains** relationship on a parent activity, the child activity automatically shows a **Contained by** relationship.

For example, if an employee management processing activity contains payroll processing, payroll processing automatically shows a **Contained by** relationship to the employee management processing activity.

-   **Sends data to**: Primary node sends personal data to the related node. Use this relationship when personal data moves between entities, systems, vendors, or jurisdictions.

For example, a payroll processing system in the US sends personal data about employees to an HR platform in the EU.

-   **Received data from**: Primary node is the recipient of personal data from the related node.

For example, an HR platform in the EU receives personal data about employees from a payroll processing system in the US.

-   **Used by**: Primary node is a shared resource consumed by one or more related nodes, without any data flowing between them.

For example, a customer database could be used by multiple marketing campaign activities to look up customer segments.


**Note:** Use **Sends data to** and **Received data from** when personal data moves between two nodes to capture data transfers. For more information, see [Manage data transfers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/privacy-workspace/data-transfers.md).

</td></tr><tr><td>

Related node type

</td><td>

Type of record you're connecting to the primary node. The available related nodes are filtered based on the selected type. The built-in related node types are:-   Business Application
-   Business Process
-   Business Service
-   Company
-   Entity
-   Processing Activity
-   Vendor

For example, if you select `Business Application`, only business applications are available to select as related nodes.

</td></tr></tbody>
</table>## Relationship details form

<table id="table_relationship_details_form"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Part of processing activity

</td><td>

Option that marks the related node as part of the current processing activity. Selected by default.

</td></tr><tr><td>

Related node locations

</td><td>

Locations of the related nodes.

 It is auto-populated from the location set on the node. If node location isn't specified, the associated entity location is used. If that isn't specified either, the associated CMDB record location is used.

 You can edit this field to change the auto-populated value.

</td></tr><tr><td>

Description

</td><td>

Description of the relationship between the primary node and this related node.

</td></tr><tr><td>

Select data subject types involved

</td><td>

Details of the data subject types whose personal data is involved.For each data subject type, update the respective cells in the following columns:

1.  Involved: Mark `Yes or No` to indicate if their personal data is being transferred from the primary node to the related node.
2.  Location: Specify all the locations that process personal data of this data subject type.
3.  Volume: Specify the number of impacted data subjects.
4.  Data elements: Specify which personal data elements are impacted. For example, `home address, salary, work assignments.`

By default, this field appears only when the relationship type is **Sends data to** or **Received data from**. However, a privacy admin can extend this behavior to a custom relationship type. For steps, see [Configure data subject selection in hierarchy relationships](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/privacy-workspace/config-ds-sys-property-hierarchy.md).

</td></tr></tbody>
</table>**Parent Topic:**[Add relationships to a hierarchy for a processing activity](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/privacy-workspace/create-a-data-lineage-for-a-processing-activity.md)

