---
title: Automate ticket updates and closure based on SIR incident status
description: The Secureworks CTP ticket ingestion integration has a bi-directional interface that allows for both tickets to create security incidents, as well as an ability to update the tickets once the security incident is created and/or closed with relevant incident details such as security incident number, assignment group, security incident URL, and so on.
locale: en-US
release: xanadu
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Create a profile for Secureworks CTP ticket ingestion integration, Secureworks CTP Ticket Ingestion Integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Automate ticket updates and closure based on SIR incident status

The Secureworks CTP ticket ingestion integration has a bi-directional interface that allows for both tickets to create security incidents, as well as an ability to update the tickets once the security incident is created and/or closed with relevant incident details such as security incident number, assignment group, security incident URL, and so on.

## Before you begin

Role required: sn\_si.admin

## Procedure

1.  If the Additional Options page on the progress bar is not displayed, select **Additional Options**.

2.  Complete the configuration for updating tickets when the security incident is created.

<table id="choicetable_bsh_yxn_kjb"><thead><tr><th align="left" id="d423589e66">

Option or Field

</th><th align="left" id="d423589e69">

Description

</th></tr></thead><tbody><tr><td id="d423589e75">

**Update SIR worknotes with Secureworks worklogs**

</td><td>

Select this option to enable the Secureworks worklogs and SIR work notes synchronization feature. This allows you to track updates made to the ticket in Secureworks CTP after the security incident is created.

 **Note:**

-   If the Secureworks worklogs field has been mapped to the SIR Worknotes field, the Secureworks worklogs are retrieved till the security incident is created.
-   If the synchronization feature is enabled, only worklogs created or updated after a security incident has been created are retrieved.


</td></tr><tr><td id="d423589e103">

**Update Secureworks tickets upon SIR Incident Creation**

</td><td>

Select this option to update the Secureworks CTP ticket and add additional comments when a security incident is created from the ticket. This can occur for both the initial triggering tickets that create the security incident, as well as aggregated tickets.

</td></tr><tr><td id="d423589e115">

**Initial comments posted back to Secureworks ticket**

</td><td>

When a security incident is created, the ticket is automatically updated in Secureworks CTP with comments. You can modify the default text and use the $\{field name\}$ format to add or modify any fields available in the security incident form.

</td></tr><tr><td id="d423589e127">

**Close Secureworks tickets upon SIR Incident Closure**

</td><td>

Select this option if you want to use the automated ticket closure option. This can occur for both the initial triggering tickets that create the security incident, as well as aggregated tickets. When a security incident is closed, the corresponding ticket is automatically closed in Secureworks CTP along with the same close code as the security incident and the default closure comments specified in the profile. **Note:** You cannot use this option to update the Master Ticket status.

</td></tr><tr><td id="d423589e143">

**Closure comments posted back to Secureworks ticket**

</td><td>

The default closure comments are displayed here. You can edit the default text and use the $\{field name\}$ format to add or modify any fields available in the security incident form.

</td></tr></tbody>
</table>3.  Click **Finish** to complete the configuration and move the profile to the **Waiting** state.

    A confirmation dialog is displayed. You have successfully set up the profile. Activate this profile to pull tickets from the Secureworks CTP portal based on your scheduling.


