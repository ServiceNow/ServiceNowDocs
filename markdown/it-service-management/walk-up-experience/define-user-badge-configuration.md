---
title: Define a user badge configuration
description: Define the table from where the user ID and Badge ID mapping information is retrieved.
locale: en-US
release: xanadu
product: Walk-Up Experience
classification: walk-up-experience
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Walk-up Experience Badge Reader Integration setup and configuration, Badge Reader Integration for Walk-up Experience, Configure, Walk-up Experience, IT Service Management]
---

# Define a user badge configuration

Define the table from where the user ID and Badge ID mapping information is retrieved.

## Before you begin

Role required: badge\_admin

## About this task

The user ID and badge ID mapping configuration is used to retrieve the user ID of the user from the badge ID when requesters scan their badges to the badge reader for check-in into a location. You can define multiple configurations for mapping.

## Procedure

1.  Navigate to **All** &gt; **Badge Reader Integration** &gt; **User Badge Configuration**.

2.  Click **New**.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name of the configuration.|
    |Table Name|The table that has the mapping information on the user ID and badge ID. Select this table from the list.|
    |User Field|User ID of the requester.|
    |Badge Field|The entity to which the user badge is linked. Select this entity from the list.|
    |Facility Code Field|Unique facility or site code that is encoded into each card. The code identifies the organization.|
    |Active|Option to activate the configuration. This option is selected by default.|

4.  Click **Submit**.


## Result

The mapping configuration is created. You can select this mapping configuration in the Badge Reader form to retrieve the user ID from the badge ID based on this mapping configuration.

**Parent Topic:**[Walk-up Experience Badge Reader Integration setup and configuration](../concept/walkup-badge-read-integ-config.md)

