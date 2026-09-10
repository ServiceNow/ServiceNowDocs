---
title: Map request types to data subjects for a jurisdiction
description: Configure the request types available to each data subject type within a jurisdiction. When a requester selects a data subject type in the external-facing Personal Data Rights \(PDR\) form, only the request types scoped to it appear.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/privacy-workspace/map-request-type-to-ds.html
release: australia
product: Privacy Workspace
classification: privacy-workspace
topic_type: task
last_updated: "2026-05-26"
reading_time_minutes: 3
breadcrumb: [Configure the external-facing PDR form, Configure, Personal Data Rights \(PDR\), Privacy Management, Governance, Risk, and Compliance]
---

# Map request types to data subjects for a jurisdiction

Configure the request types available to each data subject type within a jurisdiction. When a requester selects a data subject type in the external-facing Personal Data Rights \(PDR\) form, only the request types scoped to it appear.

## Before you begin

Verify that the data subject types are mapped to their relevant jurisdictions. For steps, see [Configure the data subject types for a jurisdiction](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/privacy-workspace/config-pdr-ds-types.md).

Role required: sn\_grc\_pdr.pdr\_admin

## About this task

A request type mapping ties one or more privacy requests, such as right to delete or right to correct, to a specific data subject type within a jurisdiction. Add a separate mapping for each data subject type and request type combination you want to make available. The external-facing form lists a request type only when an active mapping exists for the location and data subject type the requester selects.

For each mapping, you can hide specific fields from the form and mark others as mandatory. This ensures that the form collects only the information relevant to the request.

## Procedure

1.  Navigate to **All** &gt; **Personal Data Rights** &gt; **External form configuration**.

2.  Open the active external form configuration record.

3.  From the PDR external facing form location configs related list, open the location configuration record to which you added data subject types.

4.  From the PDR external facing form data subject maps related list, open the data subject type to which you want to map request types.

5.  Map request types in one of the following ways.

<table><thead><tr><th align="left" id="d104945e124">

Choice

</th><th align="left" id="d104945e127">

Steps

</th></tr></thead><tbody><tr><td id="d104945e133">

**Map all active request types at once**

</td><td>

1.  Select **Map all request types**.

This creates an active mapping for every re quest type currently active in the request types table for your organization.

2.  Verify that the activated mappings appear in the PDR external facing form request type maps related list.
 To customize an individual mapping afterward, open the record from the PDR external facing form request type maps related list, and update it.

</td></tr><tr><td id="d104945e159">

**Map one request type at a time**

</td><td>

1.  In the PDR external facing form request type maps related list, select **New**.
2.  In **Request types**, select the unlock icon and add the request types you want to map.

**Note:** The available request types are limited to those defined under the PDR request parent record. To add a request type, see [Configuring Personal Data Rights request type](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/privacy-workspace/configure-pdr-request-type.md).

3.  Select the **Active** option.
4.  \(Optional\) In **Fields to hide**, add the fields that you want to hide from the external-facing form for the selected request type\(s\). For example, to prevent an authorized agent from submitting a request in a particular jurisdiction, hide the agent's first name, last name, and phone number fields.
5.  \(Optional\) In **Mandatory fields**, specify the fields that the requester must fill to submit the form.
6.  Select **Submit**.


</td></tr></tbody>
</table>
## Result

The mapped request types appear in the PDR external facing form request type maps related list of the corresponding data subject type mapping.

Requesters who choose the corresponding location and data subject type can select these request types on the external-facing form.

**Parent Topic:**[External-facing Personal Data Rights form configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/privacy-workspace/configure-pdr-ext-form.md)

**Related topics**  


[Personal Data Rights \(PDR\) external-facing form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/privacy-workspace/pdr-external-facing.md)

[External-facing Personal Data Rights form configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/privacy-workspace/configure-pdr-ext-form.md)

