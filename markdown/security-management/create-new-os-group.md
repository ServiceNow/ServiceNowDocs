---
title: Create an operating system group
description: Operating system groups are used to map an operating system to specific process types and scripts in Security Incident Response workflows. The scripts define how running processes for the defined operating system groups are retrieved. New operating systems can be added as needed.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Security Operations common functionality, Security Operations]
---

# Create an operating system group

Operating system groups are used to map an operating system to specific process types and scripts in Security Incident Response workflows. The scripts define how running processes for the defined operating system groups are retrieved. New operating systems can be added as needed.

## Before you begin

Role required: sn\_sec\_cmn.admin

## Procedure

1.  Navigate to **All** &gt; **Security Operations** &gt; **Utilities** &gt; **Operating System Groups**.

    The base system includes scripts for three operating systems:

    -   BSD-based OS
    -   POSIX-based OS
    -   Windows OS
2.  Select **New**.

    ![Operating system groups](../image/os-groups.png)

3.  Fill in the fields, as needed.

    |Field|Description|
    |-----|-----------|
    |Name|The name of the operating system group.|
    |Description|A description for the operating system group.|
    |Table|The affected table.|
    |Active|Select this check box to activate the operating system group.|
    |Use filter group|Select this check box to use a filter group for locating matching records in the selected table.|
    |Filter group|Select the filter group for locating matching records in the selected table. This field displays only if you selected the **Use filter group** check box.|
    |Condition|The condition builder fields display only if you did not select the **Use filter group** check box.|

4.  Select and hold \(or right-click\) in the form header and select **Save**.

    The Operating System Related Scripts related list opens.

    ![Operating System Related Scripts](../image/os-related-scripts.png)

5.  Select **New**.

6.  Select scripts that correspond with the workflows you're using to get running processes, services, and/or network statistics.

7.  Select **Submit**.


**Parent Topic:**[Security Operations common functionality](../concept/sec-ops-common-functionality.md)

**Related topics**  


[bundle-platcap.mid-server-script-attach]

