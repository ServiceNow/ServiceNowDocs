---
title: Configure Scheduled Data Imports records
description: Configure a Scheduled Data Imports record for the Crisis map application. You can then manage your subscriptions to the threat feeds from an internal or external source in the BCM Configurable Workspace.
locale: en-US
release: australia
product: GRC: Business Continuity Management Components
classification: grc-business-continuity-management-components
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Setup for Crisis map, Configure, Business Continuity Management, Governance, Risk, and Compliance]
---

# Configure Scheduled Data Imports records

Configure a Scheduled Data Imports record for the Crisis map application. You can then manage your subscriptions to the threat feeds from an internal or external source in the BCM Configurable Workspace.

## Before you begin

Role required: admin

You must set up the Google maps for enabling the crisis map functionality. For more information, see [Set up Google Maps API](https://www.servicenow.com/docs/access?context=set-up-google-maps-api&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US).

## About this task

Threat feeds provide a situational awareness of potential or current threats to the security of your organization. Threat alerts can be weather alerts, pandemic alerts, geopolitical situations, or internal events like security incidents and system outages.

## Procedure

1.  Navigate to **Threat and Alert Data Feeds** &gt; **Administration** &gt; **Scheduled Imports**.

    Following two scheduled data imports exist within the base system.

    |Name|Data source|
    |----|-----------|
    |GDAC Feed Source|GDAC Feeds|
    |Weather.gov Severe Alerts Scheduled Import|Weather Gov Alerts|

2.  To add a new scheduled data import record, select **New**.

    The Scheduled Data Import form is displayed.

    ![Scheduled Data Import form.](../image/sch-data-import-form.png)

3.  On the form, fill in the fields.

    For more information on the Scheduled Data Imports form, see [Scheduled Data Imports form](../reference/scheduled-data-imports-form.md).

4.  Select **Submit**.

5.  To execute an existing scheduled data import, select the link to edit the record in the Threat and alert data feeds for Crisis Management application.

    |Step|Description|
    |----|-----------|
    |**Select the check box for Execute pre-import script**|Add the Prescript in the text box.|
    |**Select the check box for Execute post-import script**|Add the Postscript in the text box.|
    |**Select __Execute now__**|Execute the script.|

    The example shows a scheduled data import record where GDAC Feeds is the data source.

    ![Sample scheduled data import record.](../image/sample-sch-import-record.png)

6.  To delete an existing data import record, select **Delete**.

7.  To update an existing data import record, select **Update**.


## Result

The data import record is displayed in the **Scheduled Data Imports** record page.

-   **[Scheduled Data Imports form](../reference/scheduled-data-imports-form.md)**  
Use the Scheduled Data Imports form in the BCM Configurable Workspace to add details about a Scheduled data imports record.

**Parent Topic:**[Setup for Crisis map](../concept/crisis-map-admin-tasks.md)

