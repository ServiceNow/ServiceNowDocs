---
title: Universal Task for external users
description: Enable external users to have access to the tasks assigned through Universal Task.
locale: en-US
release: xanadu
product: Universal Task
classification: universal-task
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Using Universal Task, Universal Task, Employee Service Management]
---

# Universal Task for external users

Enable external users to have access to the tasks assigned through Universal Task.

Users that aren’t yet part of your organization are external users \(snc\_external\). For example, new-hires who didn’t yet start working for the company.

The following points must be considered to enable Universal Task for the external users.

-   The Explicit Role \(com.glide.explicit\_roles\) plugin must be installed to assign external and internal roles to the users. For more information, see .
-   When creating a Universal Task, all pre-defined task types like Upload Documents, Mark When Complete, Checklist, and Collect Employee Input are available for external users except for Submit Catalog Item. If you try to create a Submit Catalog Item, you will get an error.
-   All the Universal Task widgets, tables, and ACLs are enabled for both internal and external roles.
-   The portal and pages where the Universal Task is embedded must also be supported for the external users. For example,
    -   Employee Service Center where the widgets are added.
    -   The **To-Do** tab of the Employee Service Center.
    -   The hrm\_todos\_page where the Universal Task is displayed.

**Parent Topic:**[Using Universal Task](use-universal-task.md)

