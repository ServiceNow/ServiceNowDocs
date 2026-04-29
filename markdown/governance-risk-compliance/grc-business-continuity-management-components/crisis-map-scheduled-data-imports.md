---
title: Configure scheduled data imports for crisis map
description: Manage your subscriptions to threat feeds from internal or external sources by configuring scheduled data imports.
locale: en-US
release: australia
product: GRC: Business Continuity Management Components
classification: grc-business-continuity-management-components
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure search for places in crisis map, Setting up the crisis map, Crisis Management map, Using BCM Classic Workspace, Manage, Business Continuity Management, Governance, Risk, and Compliance]
---

# Configure scheduled data imports for crisis map

Manage your subscriptions to threat feeds from internal or external sources by configuring scheduled data imports.

## Before you begin

Role required: System administrator

You must set up the Google maps for enabling the crisis map functionality. For more information, see [Set up Google Maps API](https://www.servicenow.com/docs/access?context=set-up-google-maps-api&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US).

## About this task

Threat feeds provide a situational awareness of potential or current threats to an organization's security. Threat alerts can be weather alerts, pandemic alerts, geopolitical situations, or internal events like security incidents and system outages.

## Procedure

1.  Navigate to **Threat and Alert Data Feeds** &gt; **Administration** &gt; **Scheduled Imports**.

    Following two scheduled data imports exist within the base system.

    |Name|Data source|
    |----|-----------|
    |GDAC Feed Source|GDAC Feeds|
    |Weather.gov Severe Alerts Scheduled Import|Weather Gov Alerts|

2.  To add a new scheduled data import, click **New**.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name of the scheduled import. Normally the source is the name.|
    |Data source|Internal or external source of the threat and alert data used for import.|
    |Run as|User who has the permission to import the threat alerts.|
    |Active|Option for enabling the alert as active.|
    |Application|Read-only field. The field helps distinguish items relevant to the crisis map.|
    |Run|Frequency at which the data is imported.|
    |Conditional|Option to indicate if a conditional script is required for the threat alert import.|
    |Concurrent Import|Option for allowing concurrent imports.|
    |Execute pre-import script|Option for enabling the execution of a pre-import script.|
    |Execute post-import script|Option for enabling the execution of a post-import script.|

4.  Click **Submit**.


