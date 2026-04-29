---
title: Healthcare and Life Sciences Service Management Core properties
description: There are several advanced Healthcare and Life Sciences Service Management Core properties that you can configure for features used in Healthcare and Life Sciences applications.
locale: en-US
release: australia
product: Healthcare and Life Sciences Service Management Core
classification: healthcare-and-life-sciences-service-management-core
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Reference, Healthcare and Life Sciences Service Management Core, Healthcare and Life Sciences Service Management, Healthcare and Life Sciences]
---

# Healthcare and Life Sciences Service Management Core properties

There are several advanced Healthcare and Life Sciences Service Management Core properties that you can configure for features used in Healthcare and Life Sciences applications.

These properties are available for Healthcare and Life Sciences Service Management Core.

**Note:** To open the System Properties \[sys\_properties\] table, enter `sys_properties.list` in the navigation filter.

<table id="table_rdv_m43_tqb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Comma separated list of all to-do task tables visible on a patient portal

 sn\_hcls.to.do.tasks.list

</td><td>

Enter a list of task table names that are displayed as to-do items on a patient portal. For multiple entries, separate the task table names with commas.

-   Type: string
-   Default value: sn\_doc\_task,sn\_hcls\_insurance\_info\_task
-   Location: System Property \[sys\_properties\] table
-   Learn more: [Specify a to-do item for patients](../task/hcls-config-to-do-items.md)

</td></tr><tr><td>

Enables self registration on Healthcare patient Portal

 sn\_hcls.enable\_self\_registration

</td><td>

Set the property to `True` to enable the self-registration feature in the Patient Portal.

-   Type: true \| false
-   Default value: true
-   Location: System Property \[sys\_properties\] table
-   Learn more: [Configure the self-registration feature on the Patient Portal](../concept/hcls-self-registration.md)

</td></tr><tr><td>

Patient portal FAQ category ID

 sn\_hcls.psp.patient\_portal\_faq\_category\_id

</td><td>

Sys id of the default ‘Frequently asked questions’ knowledge category \(table kb\_category\) section of HCLS Patient portal.

 Replacing this would allow someone to replace the FAQs they wish to display on HCLS patient portal.

 -   Type: string
-   Default value: 2bee428777400110ac9cd0cb8d5a9998
-   Location: System Property \[sys\_properties\] table

</td></tr><tr><td>

Patient Portal enable REM conversion

 glide.service\_portal.resize\_text.patientportal.enable\_rem\_conversion

</td><td>

Variable specifically for service portal. Setting this to true enables service portal text to be resized up to 200% using browser settings.

 -   Type: true \| false
-   Default value: true
-   Location: System Property \[sys\_properties\] table

</td></tr></tbody>
</table>**Parent Topic:**[Healthcare and Life Sciences Service Management Core reference](hcls-serv-mgmt-core-reference.md)

