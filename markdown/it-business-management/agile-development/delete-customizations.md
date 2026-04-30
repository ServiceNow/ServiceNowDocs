---
title: Delete customizations before upgrading to Agile Development 2.0
description: Take complete advantage of enhanced functionality by deleting all your customizations before upgrading to Agile Development 2.0.
locale: en-US
release: xanadu
product: Agile Development
classification: agile-development
topic_type: task
last_updated: "2025-10-23"
reading_time_minutes: 1
breadcrumb: [Migration from Agile Development 1.0 to Agile Development 2.0, Configure, Agile Development 2.0, Strategic Portfolio Management]
---

# Delete customizations before upgrading to Agile Development 2.0

Take complete advantage of enhanced functionality by deleting all your customizations before upgrading to Agile Development 2.0.

## Before you begin

Role required: admin

## About this task

**Important:** Agile Development 1.0 and its features such as Sprint burndown chart and release burndown chart are deprecated and no longer available. [Agile Development 2.0](../reference/agile-landing-page.md) provides the latest experience for supporting your Agile work methodology.

## Procedure

1.  In the Navigation filter, enter `sys_properties.list`.

    The entire list of properties in the System Properties \[sys\_properties\] table appears.

2.  Click **New**.

3.  On the form, fill in the fields as follows:

    |Field|Value|
    |-----|-----|
    |Name|com.snc.sdlc.scrum.pp.delete\_customer\_updates|
    |Description|Delete customizations in the Agile Development application from the Customer Update \[sys\_update\_xml\] table.|
    |Type|true\|false|
    |Value|true|

4.  Click **Submit**.

    All customizations would be deleted and the property also would be automatically deleted.


## What to do next

If the Agile Development 2.0 plugin \(com.snc.sdlc.agile.2.0\) has been installed before deleting the customizations, refresh the plugin by reinstalling it.

**Parent Topic:**[Migration from Agile Development 1.0 to Agile Development 2.0](../concept/migrate-agile.md)

**Related topics**  


[Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=xanadu&pubname=xanadu-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US)

