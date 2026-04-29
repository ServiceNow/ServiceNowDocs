---
title: Configure entity-based record access rules
description: Configure entity-based record access rules on record types to apply access restrictions to new records automatically.
locale: en-US
release: australia
product: GRC Common Functions
classification: grc-common-functions
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Manage Entity Based Access, Entity Based Access, Common GRC features, Governance, Risk, and Compliance]
---

# Configure entity-based record access rules

Configure entity-based record access rules on record types to apply access restrictions to new records automatically.

## Before you begin

Role required:sn\_grc\_ent\_access.admin or sn\_grc\_ent\_access.bulk\_access\_admin

## Procedure

1.  Navigate to **All** &gt; **Entity Based Access Configurations** &gt; **Entity based record access rules**.

2.  Select **New**.

    ![](../image/record-attribute-user-access.png)

3.  From the **Record type** drop-down list, select the type for which you want to configure entity-based record access rules.

    Only the record types on which the entity-based access is enabled are shown for selection.

    **Note:** You can create only one rule for each primary record type.

4.  Select the Is primary check box if this rule should be the primary rule for the selected record type.

5.  Select the **Apply entity-based access restriction** check box to automatically apply access restrictions to newly created records and to existing records affected by hierarchy changes.

6.  In the Record Attribute User Access related list, grant record-level access to users and groups referenced in user or group fields.

    1.  Unlock user fields and select the required users from the available list.

    2.  Unlock user group fields and select the required user groups from the available list.

7.  Select **Submit**.

    The rule is applied only on related records of entities with active entity-based access \(EBA\) configuration.


## Result

The entity-based access restrictions are automatically applied to both primary and secondary record types based on primary record selection and activation of rule for new records.

When record attribute user access is configured, users and groups referenced in user fields or user group fields continue to have record level access even after entity based access restrictions are applied.

**Parent Topic:**[Managing Entity Based Access](../concept/using-entity-based-access.md)

