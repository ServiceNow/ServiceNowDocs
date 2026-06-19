---
title: Create a PDR external-facing form configuration record
description: Create the parent external form configuration record that anchors all location, data subject type, and request type rules for the external-facing Personal Data Rights \(PDR\) form.
locale: en-us
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/privacy-workspace/config-pdr-ext-form-record.html
release: australia
product: Privacy Workspace
classification: privacy-workspace
topic_type: task
last_updated: "2026-05-14"
reading_time_minutes: 1
keywords: [PDR external form configuration, configure public form]
breadcrumb: [Configure external-facing PDR form, Configure, Personal Data Rights \(PDR\), Privacy Management, Governance, Risk, and Compliance]
---

# Create a PDR external-facing form configuration record

Create the parent external form configuration record that anchors all location, data subject type, and request type rules for the external-facing Personal Data Rights \(PDR\) form.

## Before you begin

Role required: sn\_grc\_pdr.pdr\_admin

## About this task

The external-facing PDR form is the public form where data subjects and authorized agents submit privacy requests without logging in. Before you can set location-specific rules, you create a single parent external form configuration record. This record holds form-wide content, such as title, sub-title, per-step guidance, and default URLs, and acts as the source for all jurisdiction-specific configuration. One active record drives one form, so changes propagate predictably.

Only one external form configuration record can be active at a time. The public form uses the active record to drive its content, and the locations and request types that follow.

## Procedure

1.  Navigate to **All** &gt; **Personal Data Rights** &gt; **External form configuration**.

2.  If an external form configuration record is already active, deactivate it.

    1.  Open the existing record.

    2.  Clear the **Active** option.

    3.  Select **Update**.

3.  Select **New**.

4.  On the form, fill in the fields.

    For field descriptions, see [External-facing form configuration fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/privacy-workspace/pdr-ext-form-new-record-form.md).

5.  To activate this record, select the **Active** option.

6.  Select **Submit**.

    The record appears in the external form configuration list.


## What to do next

Open the new active record and use the PDR external facing form location configs related list to map at least one jurisdiction. See [Configure jurisdictions for the external-facing Personal Data Rights form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/privacy-workspace/config-pdr-location.md).

-   **[External-facing form configuration fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/privacy-workspace/pdr-ext-form-new-record-form.md)**  
An external facing Personal Data Rights \(PDR\) form configuration record holds the form-wide content that the requester sees across regions.

**Parent Topic:**[External-facing Personal Data Rights form configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/privacy-workspace/configure-pdr-ext-form.md)

