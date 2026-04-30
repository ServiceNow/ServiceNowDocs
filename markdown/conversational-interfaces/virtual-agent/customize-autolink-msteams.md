---
title: Customize auto-linking for Conversational Integration with Microsoft Teams
description: Customize auto-linking for user profiles by defining the email Id of the user in any custom table rather than just the User \[sys\_user\] table.
locale: en-US
release: yokohama
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configure Virtual Agent for Microsoft Teams, Integrating Virtual Agent with Microsoft Teams, Integrating Virtual Agent with messaging apps, Integrating Virtual Agent with other channels, Virtual Agent, Conversational Interfaces]
---

# Customize auto-linking for Conversational Integration with Microsoft Teams

Customize auto-linking for user profiles by defining the email Id of the user in any custom table rather than just the User \[sys\_user\] table.

## Before you begin

-   Make the User \[sys\_user\] table extensible.
-   Create a custom table with custom email fields extending the User \[sys\_user\] table.
-   Ensure that the scope of the custom table is Microsoft Teams, or else, create a cross scope privilege.
-   Populate the system property in the **table\_name.column\_name** format.

Role required: admin

## About this task

The auto-linking process searches the user table for the email ID and if found, links the user to the profile automatically. You can also customize the auto-linking process by defining the email Id for auto/pre-linking in any custom table rather than the current User \[sys\_user\] table.​ You can customize the auto-linking process of user profiles by using the **sn\_va\_teams.auto\_link\_email\_attribute** system property that defines the column from which the email ID of the user must be read for auto-linking.

**Note:**

-   By default, the value of the system property is empty. If it is set to &lt;empty&gt;, then the email Id for the user is fetched from the \[sys\_user\] table.
-   If the value of the system property is specified in the format of **table\_name.column\_name** \(both table\_name and column\_name must be the physical names from their respective name fields\), then the value is read from the column name specified. For example, **sn\_va\_teams\_extendeduser.u\_custom\_mail**.

## Procedure

1.  In the navigation filter, enter `sys_properties.list`.

    The entire list of properties in the System Properties \[sys\_properties\] table is displayed.

2.  Search and open the **sn\_va\_teams.auto\_link\_email\_attribute** system property.

3.  Provide a value in the format of **table\_name.column\_name** and save the record.

    Once the record is saved, you can initiate the conversation with the bot.


**Parent Topic:**[Configure Virtual Agent for Microsoft Teams](configure-va-msteams-settings.md)

