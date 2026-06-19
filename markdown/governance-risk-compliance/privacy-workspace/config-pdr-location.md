---
title: Configure jurisdictions for the external-facing Personal Data Rights form
description: Configure the jurisdictions, authorized agent option, and per-location URLs for the external-facing Personal Data Rights \(PDR\) form. These settings determine what requesters in each jurisdiction see based on their local privacy rules.
locale: en-us
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/privacy-workspace/config-pdr-location.html
release: australia
product: Privacy Workspace
classification: privacy-workspace
topic_type: task
last_updated: "2026-05-14"
reading_time_minutes: 2
keywords: [PDR location configuration, jurisdictions privacy request]
breadcrumb: [Configure external-facing PDR form, Configure, Personal Data Rights \(PDR\), Privacy Management, Governance, Risk, and Compliance]
---

# Configure jurisdictions for the external-facing Personal Data Rights form

Configure the jurisdictions, authorized agent option, and per-location URLs for the external-facing Personal Data Rights \(PDR\) form. These settings determine what requesters in each jurisdiction see based on their local privacy rules.

## Before you begin

Role required: sn\_grc\_pdr.pdr\_admin

## About this task

Privacy laws vary by jurisdiction. Local rules determine which privacy rights data subjects can exercise, who is allowed to submit a request on their behalf, what disclosures must appear when a request is initiated, and the information the organization can collect at intake to process the request. Location configuration is where you add these rules.

Each location configuration record holds the rules that apply when a requester selects a specific country or state on the public form. You can map one or more jurisdictions to a single location configuration record. For each jurisdiction, you can:

-   Add custom text in the **Introduction** field. For example, disclaimers, applicable privacy laws, or an introduction to the form.
-   Enable an authorized agent to submit a request on behalf of a data subject.
-   Specify location-specific URLs for privacy statement, legal terms, and terms of service.
-   Map the data subject types and request types that should be available for selection for a particular location.

## Procedure

1.  Navigate to **All** &gt; **Personal Data Rights** &gt; **External form configuration**.

2.  Open the active external form configuration record.

    To create an active record, see [Create a PDR external-facing form configuration record](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/privacy-workspace/config-pdr-ext-form-record.md).

3.  On the PDR external-facing form location configs related list, select **New**.

4.  On the form, fill in the fields.

    For field descriptions, see [PDR new jurisdiction configuration form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/privacy-workspace/ext-form-new-jurisdiction.md).

    **Note:** Don't select the **Active** option. Activate the jurisdiction after you add at least one active data subject type to it.

5.  Select **Submit**.

    A new inactive jurisdiction record appears in the PDR external-facing form location configs related list.

6.  Map at least one data subject type to the new jurisdiction record.

    For steps, see [Configure the data subject types for a jurisdiction](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/privacy-workspace/config-pdr-ds-types.md).

7.  Activate the jurisdiction.

    1.  Return to the location configuration record from the PDR external facing form location configs related list.

    2.  Select the **Active** option.

    3.  Select **Update**.


## Result

When a requester selects a jurisdiction on the external-facing form, the form applies the introductory text, authorized agent option, and the location-specific URLs from the corresponding location configuration.

-   **[Personal Data Rights external facing form location configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/privacy-workspace/ext-form-new-jurisdiction.md)**  
Populate a new location configuration record. Field choices determine whether requesters in the mapped jurisdictions see authorized agent paths, what URLs the form links to, and what introductory text appears at the start of the Personal Data Rights \(PDR\) form.

**Parent Topic:**[External-facing Personal Data Rights form configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/privacy-workspace/configure-pdr-ext-form.md)

