---
title: Set choice action for reference field imports
description: The LDAP transform map determines how fields in the Import Set table map to fields in existing tables such as Incident or User.
locale: en-US
release: zurich
product: LDAP integration
classification: ldap-integration
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Import and map data, LDAP integration, Authentication, Access Management]
---

# Set choice action for reference field imports

The LDAP transform map determines how fields in the Import Set table map to fields in existing tables such as Incident or User.

## Before you begin

Role required: admin

## About this task

If the LDAP transform map updates a field in the import set table, the integration automatically creates a new record whenever there is a new record in the LDAP data. If the LDAP transform map updates a reference field storing data from another table, the administrator can choose to create, ignore, or reject new LDAP records.

For example, if the integration receives a new department record that does not match any existing department, you may want to update all of the other LDAP record fields without creating a new department record in the instance. The transform map allows you to set the record creation options for each reference field.

## Procedure

1.  Navigate to **All** &gt; **System LDAP** &gt; **Transform Maps**.

2.  In the Field Maps related list, select one of the following actions from the **Choice action** field:

    -   **create** – creates a new reference field record if a matching record does not exist.
    -   **ignore** – ignores new records in the reference field and completes processing of all other fields in the transform map.
    -   **reject** – stops the transform for the entire record.
    **Note:** The field map only displays the **Choice action** field for reference fields.


