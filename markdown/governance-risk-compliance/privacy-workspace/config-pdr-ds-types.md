---
title: Configure the data subject types for a jurisdiction
description: Specify which data subject types the external-facing Personal Data Rights \(PDR\) form offers in each location, so the form presents only the data subject types that local regulation supports.
locale: en-us
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/privacy-workspace/config-pdr-ds-types.html
release: australia
product: Privacy Workspace
classification: privacy-workspace
topic_type: task
last_updated: "2026-05-14"
reading_time_minutes: 2
keywords: [PDR data subject type, data subject mapping]
breadcrumb: [Configure external-facing PDR form, Configure, Personal Data Rights \(PDR\), Privacy Management, Governance, Risk, and Compliance]
---

# Configure the data subject types for a jurisdiction

Specify which data subject types the external-facing Personal Data Rights \(PDR\) form offers in each location, so the form presents only the data subject types that local regulation supports.

## Before you begin

Verify that a jurisdiction record is configured to map data subject types to it. For steps, see [Configure jurisdictions for the external-facing Personal Data Rights form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/privacy-workspace/config-pdr-location.md).

Role required: sn\_grc\_pdr.pdr\_admin

## About this task

A data subject type identifies the relationship that the requester has with your organization, such as customer, ex-employee, or third-party individual. The data subject types that the public form lists depend on the location that the requester selects. Add a data subject type mapping under each location to control this list.

## Procedure

1.  Navigate to **All** &gt; **Personal Data Rights** &gt; **External form configuration**.

2.  Open the active external form configuration record.

3.  From the PDR external facing form location configs related list, open the jurisdiction record to which you want to map data subject types.

4.  In the PDR external facing form data subject maps related list, select **New**.

5.  In the **Data subject types** field, select the data subject types that the external-facing form should offer for this location.

    You can add more than one data subject type to a single mapping.

6.  To activate the data subject type mapping, select the **Active** option.

7.  Select **Submit**.

    A new data subject type mapping appears in the PDR external facing form data subject maps related list.


## Result

Requesters raising a PDR request from this jurisdiction now see only the data subject types that you have mapped here.

## What to do next

-   Activate the location configuration where you added these data subject types. See [Configure jurisdictions for the external-facing Personal Data Rights form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/privacy-workspace/config-pdr-location.md).
-   Map request types to each active data subject type. See [Map request types to configured data subjects for a jurisdiction](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/privacy-workspace/map-request-type-to-ds.md).

**Parent Topic:**[External-facing Personal Data Rights form configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/privacy-workspace/configure-pdr-ext-form.md)

