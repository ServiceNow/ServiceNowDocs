---
title: Link to Major Security Incident
description: Link security incidents to a major security incident.
locale: en-US
release: yokohama
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Propose, promote, and link incident records, Use, Major Security Incident Management, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Link to Major Security Incident

Link security incidents to a major security incident.

## Before you begin

Role required: sn\_msi.workspace\_admin

## Procedure

1.  Navigate to **All** &gt; **Security Incident** &gt; **Incidents** &gt; **Show All Incidents**.

2.  Select the security incident in the related category that you want to link to the major security incident.

3.  Select the **Additional Actions** icon and select **Link to Major Security Incident**.

4.  Select the major security incident to which you want to link.

    1.  In the dialog box, select the Lookup using list icon.

    2.  Select the major security incident you want to link to.

    3.  Select **OK**.

5.  Select **Propose**.


## Result

The proposal is submitted and the following actions occur:

-   In the security incident record, a verification banner message is displayed and the defined Major Security Incident tag appears next to the **Select security tag** field.

-   In the **Details** tab for the major security incident in Major Security Incident Management, the record number drop-down list includes both incidents.

-   The record appears in the incident record's Major Security Incident related list, with the state listed as Proposed.

-   A message is sent to those in the defined notification list that contains a link to the incident record and the Details tab for the incident.

-   The **Activity** section in the MSIM Workspace shows that the security incident has been added as a child security incident to the major security incident with a link.


**Parent Topic:**[Propose, promote, and link incident records](../../security-incident-response/concept/promoting-sir-to-msim.md)

**Related topics**  


[Propose as a Major Security Incident](propose-as-msi.md)

[Promote to a Major Security Incident](promote-msi.md)

