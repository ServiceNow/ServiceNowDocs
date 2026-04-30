---
title: Set Entity based record access rules
description: Use entity-based record access rules to secure records and enable continuous monitoring. These rules automatically apply restrictions to new or modified records, ensuring access settings stay enforced without manual updates. When entities or processing activities change, the system updates access controls automatically.
locale: en-US
release: xanadu
product: Privacy Workspace
classification: privacy-workspace
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure access control, Access control through organizational structure, Use, Privacy Management, Governance, Risk, and Compliance]
---

# Set Entity based record access rules

Use entity-based record access rules to secure records and enable continuous monitoring. These rules automatically apply restrictions to new or modified records, ensuring access settings stay enforced without manual updates. When entities or processing activities change, the system updates access controls automatically.

## Before you begin

Role required: sn\_privacy.admin

## About this task

This task explains how to activate entity-based record access rules for continuous monitoring in ServiceNow. By enabling these rules for specific record types, you ensure that access restrictions are applied automatically to new or updated records, reducing manual intervention and maintaining compliance.

## Procedure

1.  Navigate to **All** &gt; **Entity Based Access Configurations** &gt; **Entity based record access rules**.

2.  In the Entity based record access rules list, do the following:

    1.  Check whether sn\_privacy\_privacy\_task and sn\_privacy\_processing\_activity are active.

    2.  If they are not active, select the record type \(sn\_privacy\_privacy\_task and sn\_privacy\_processing\_activity\).

    3.  In the configuration page, select **Apply entity based access restriction on new records** and then select **Update**.

    The sn\_privacy\_privacy\_task and sn\_privacy\_processing\_activity record types turn active.


## Result

EBA rules are automatically applied to records whenever changes occur in the entity structure.

**Parent Topic:**[Configure access control](../configure-access-control-by-legal-entity.md)

