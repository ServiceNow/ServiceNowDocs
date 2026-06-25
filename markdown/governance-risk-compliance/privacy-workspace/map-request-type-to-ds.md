---
title: Map request types to configured data subjects for a jurisdiction
description: Configure the request types available to each data subject type within a jurisdiction. Hide any requester or agent fields that don't apply on the external-facing Personal Data Rights \(PDR\) form.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/privacy-workspace/map-request-type-to-ds.html
release: australia
product: Privacy Workspace
classification: privacy-workspace
topic_type: task
last_updated: "2026-05-26"
reading_time_minutes: 3
breadcrumb: [Configure external-facing PDR form, Configure, Personal Data Rights \(PDR\), Privacy Management, Governance, Risk, and Compliance]
---

# Map request types to configured data subjects for a jurisdiction

Configure the request types available to each data subject type within a jurisdiction. Hide any requester or agent fields that don't apply on the external-facing Personal Data Rights \(PDR\) form.

## Before you begin

Role required: sn\_grc\_pdr.pdr\_admin

## About this task

A request type mapping ties one or more privacy request types to a specific data subject type within a location. For each mapping, you can also hide individual requester and authorized agent fields so that the form doesn't collect information that isn't relevant to the request.

Add a separate mapping for each data subject type and request type combination you want to make available. The form lists a request type only when an active mapping exists for the location and data subject type the requester selects.

## Procedure

1.  Navigate to **All** &gt; **Personal Data Rights** &gt; **External form configuration**.

2.  Open the active external form configuration record.

3.  From the PDR external facing form location configs related list, open the location configuration record to which you added data subject types.

4.  From the PDR external facing form data subject maps related list, open the data subject type to which you want to map request types.

5.  Map request types in one of the following ways.

    -   Select **Map all request types** to map every request type that is currently active in the request types table.

        This creates an active mapping for every request type that is currently active in the request types table for your organization. Use this option to populate the list quickly, then deactivate any individual mappings you don't need for this data subject type and location.

    -   Select **New** from the PDR external facing form request type maps related list.

        The available request types are limited to those defined under the PDR request parent record. To add a request type, see [Configuring Personal Data Rights request type](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/privacy-workspace/configure-pdr-request-type.md).

6.  In the **Fields to hide** field, select the fields that you don't want the external-facing form to show.

    The available options are requester’s first name, last name, and phone number, and agent’s first name, last name, and phone number. For example, if you don’t want to allow an authorized agent to submit a request for a particular jurisdiction, you can hide the agent’s first name, last name, and phone number fields.

7.  Select the **Active** option.

8.  Select **Submit**.


## Result

The mapped request types appear in the PDR external facing form request type maps related list of the corresponding data subject type mapping.

Requesters who choose the corresponding location and data subject type can select these request types on the external-facing form.

**Parent Topic:**[External-facing Personal Data Rights form configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/privacy-workspace/configure-pdr-ext-form.md)

**Related topics**  


[Personal Data Rights \(PDR\) external-facing form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/privacy-workspace/pdr-external-facing.md)

[External-facing Personal Data Rights form configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/privacy-workspace/configure-pdr-ext-form.md)

