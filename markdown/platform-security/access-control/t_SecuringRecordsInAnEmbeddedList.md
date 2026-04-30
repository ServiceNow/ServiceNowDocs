---
title: Secure records in an embedded list
description: To apply security to the records in embedded lists, limit editing and deleting records in embedded lists to specific roles.
locale: en-US
release: xanadu
product: Access Control
classification: access-control
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configure an ACL rule, Access Control List Rules, Access Management]
---

# Secure records in an embedded list

To apply security to the records in embedded lists, limit editing and deleting records in embedded lists to specific roles.

## Before you begin

Role required: security\_admin

## Procedure

1.  Navigate to **All** &gt; **System Security** &gt; **Access Control \(ACL\)**.

2.  Open the **Write** or **Delete** record for the appropriate table.

3.  In the Requires Role section of the form, add the roles that have write or delete permission for that table.

4.  Save the changes.

    When records from the associated table appear in an embedded list, the edit and delete options are available only to users with the specified roles.


