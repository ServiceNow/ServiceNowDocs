---
title: Activate country choices for users
description: Select from additional countries in the Next Experience language and region preferences or a user record.
locale: en-US
release: australia
product: System Localization
classification: system-localization
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuring System Localization, System Localization, Translation and localization, Configure core features, Administer the ServiceNow AI Platform]
---

# Activate country choices for users

Select from additional countries in the Next Experience language and region preferences or a user record.

## Before you begin

Role required: admin

## About this task

By default, you can select from only a limited list of countries in the Next Experience language and region preferences or in a User record. To allow users to select from additional countries, administrators can activate choices for the Country code field on the User \[sys\_user\] table. For more information about the Country user preference, see Configure Next Experience language and region preferences.

## Procedure

1.  In the navigation filter, enter `sys_choice.list`.

2.  From the Choices list, use the condition builder to enter the following condition statement: **\[Table\] \[is\] \[sys\_user\] AND \[Element\] \[is\] \[country\] AND \[Inactive\] \[is\] \[true\]**.

3.  Select **Run**.

4.  Select the Choice record for the country that you want to activate.

5.  From the Choice record, clear the **Inactive** option.

6.  Select **Update**.


**Related topics**  


[Choice table](../reference/r_ChoicesTable.md)

[User administration](../../roles/concept/c_UserAdministration.md)

