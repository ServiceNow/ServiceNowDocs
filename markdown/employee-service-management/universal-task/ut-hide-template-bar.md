---
title: Hide the template bar on the Universal Task form
description: Hide the template bar for the Universal Task form because it does not include Universal Task templates.
locale: en-US
release: australia
product: Universal Task
classification: universal-task
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuring your service, Setting up and configuring Universal Task, Universal Task, Employee Service Management]
---

# Hide the template bar on the Universal Task form

Hide the template bar for the Universal Task form because it does not include Universal Task templates.

## Before you begin

Role required: admin

## Procedure

1.  In the navigation panel, enter `sys_properties_list.do`.

2.  On the System Properties page, click **New**.

    **Note:** Ensure that the application is in Global scope.

3.  On the form, fill in the fields.

    |Field|Value|
    |-----|-----|
    |Name|glide.ui.show\_template\_bar.sn\_uni\_task\_universal\_task|
    |Type|true \| false|
    |Value|false|

4.  Click **Submit**.

5.  To clear the cache of your instance, in your browser, enter `<server_url/cache.do>`.


**Parent Topic:**[Configuring your service for Universal Task](../concept/config-service-for-ut.md)

**Previous topic:**[Display the universal tasks for a request in Now Mobile](ut-mobile-config-tasktab.md)

**Next topic:**[Remove the Universal Task admin role from the admin role](ut-remove-admin-role.md)

