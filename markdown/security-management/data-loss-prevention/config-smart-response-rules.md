---
title: Configure Smart Response Rules
description: Configure the Symantec smart response rule\(s\) to perform response actions on the ingested Symantec DLP incidents.
locale: en-US
release: xanadu
product: Data Loss Prevention
classification: data-loss-prevention
topic_type: task
last_updated: "2024-08-12"
reading_time_minutes: 1
breadcrumb: [Symantec Integration for Data Loss Prevention Incident Response, DLP integrations, Data Loss Prevention Incident Response, Security Operations]
---

# Configure Smart Response Rules

Configure the Symantec smart response rule\(s\) to perform response actions on the ingested Symantec DLP incidents.

## Before you begin

Role required: sn\_dlir.admin

## About this task

Verify that the Symantec user that you are configuring for ServiceNow Symantec DLP integration must have those Smart Response Rules selected under the **Roles configuration** page. For more information, see **Actions** section available on [Configuring Roles](https://techdocs.broadcom.com/us/en/symantec-security-software/information-security/data-loss-prevention/16-0-1/Manage-the-Enforce-Server/managing-users-and-rules/configuring-roles-id-sf0b0167317a-d297e3139.html) document.

For the fetched smart response rule\(s\), DLP admin can create the Incident Response Option Rule\(s\) and Response Option Mappings to configure the response action\(s\) to be performed on ingested Symantec DLP Incidents.

## Procedure

1.  Navigate to **All** &gt; **Symantec DLP Integration** &gt; **Smart Response Rules**.

    You will see all the available smart response options for each configured integration configuration. For more information see, [Install and configure the Symantec DLP integration for Data Loss Prevention](install-configure-symantec-dlp-integration.md) and follow the procedure explained on how to configure Symantec integration: configuration source if this was not configured.

2.  Click on any of the Smart Response Rules to open its form view.

    Follow [Create incident response option rules](../../data-loss-prevention/task/configure-end-user-action.md) to create Incident Response Option Rules and Response Option Mappings to display this smart response rule on Respond modal of DLP workspace.

3.  Create the approval rules for the Smart Response Rule using the **Approval Rules** tab in the related list or by following the procedure explained in the Configure Approval Rules section.

    Approval Rules for each Smart Response Rules will be visible in the Approval Rules related list.

4.  After creating the Incident Response Option Rule\(s\), you can see the record in the related list of the Smart Response Rule record.

5.  Use the **Refresh Smart Response Rule** button in the list view to manually update the source.

    The smart response rules will add, update, or delete automatically each day for every source.


**Parent Topic:**[Symantec Integration for Data Loss Prevention Incident Response](../concept/symantec-dlp-integration.md)

