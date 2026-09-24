---
title: Exploring Federated ID
description: The ServiceNow Identity system uniquely identifies users across multiple instances and assigns each resolved user a unique Federated ID for consistent identification.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/identity/federated-id.html
release: brazil
product: Identity
classification: identity
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 3
breadcrumb: [Global Identity, Identity]
---

# Exploring Federated ID

The ServiceNow Identity system uniquely identifies users across multiple instances and assigns each resolved user a unique Federated ID for consistent identification.

With Federated ID, you can accurately calculate the number of unique users across instances, which is useful for licensing and user management. You can generate Federated ID for Role and User on ServiceNow.

To identify and match users and roles across instances, the ServiceNow Identity system generates a Federated ID from the fields configured as the ID Fields for a table, using a hashing function, and stores the value in the `federated_id` column of the `sys_user` table. By default, the User ID and Email fields are used. You can change the fields used for generation to meet your requirements.

**Note:** A Federated ID criteria must include at least one unique field. The unique field verifies that the generated Federated ID stays unique for each record on the selected table.

## Selecting ID Fields

By default, Federated ID generation lets you choose the fields used to generate Federated IDs, subject to these rules:

-   The User ID \(`user_name`\) field is no longer mandatory. You can select any unique field from the `sys_user` table as the required unique field. The User ID field itself qualifies as a unique field, so you can still use it if you want.
-   At least one unique field must be selected. You can select more than one unique field.
-   You can add secondary, non-unique fields from the `sys_user` table, and add, remove, or change them at any time. Secondary fields don't satisfy the unique field requirement on their own — for example, valid selections include \(User ID, Email\) or \(a unique field, Email\).
-   A Federated ID is generated for a record only if at least one of its selected unique fields has a value. If you selected several unique fields, the record needs a value in just one of them. If all the selected unique fields are empty, no Federated ID is generated for that record \(the Federated ID is null\).

User ID and Email are used to generate Federated IDs by default. To change the fields used for generation, see [Update the ID fields for Federated ID generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/identity/updating-id-fields.md). The `iamsync_admin` role is required to update the configuration.

\[Omitted image "federated-id-sys.png"\] Alt text: Federated ID in sys\_user table

## Which fields qualify as a unique field

A field qualifies as a unique field only when its uniqueness is enforced on a single column. The following table shows which field types can be selected as the unique field.

|Field type|Can be used as a unique field|
|----------|-----------------------------|
|Field marked unique in the dictionary|Yes|
|Field with a single-column unique database index|Yes|
|Field with a database index that isn't unique|No|
|Field that is unique only as part of a composite \(multi-column\) unique index|No|
|Non-unique field|No|

## Validation

-   If you save a criteria without a unique field, the save is blocked and the error **At least one unique field is required for Federated Id generation.** is displayed. The Federated ID Criteria form also shows a message guiding you to include at least one unique field.
-   Before a Federated ID generation run begins, the system confirms that a unique field is configured. If a unique field is missing, the run is safely skipped instead of failing repeatedly.

**Note:** When the unique field data is empty, Fed ID is not generated.

## Changing the ID Fields

You can change the unique field to a different unique field at any time.

**Important:** Changing any ID Field — unique or secondary — regenerates the Federated IDs for all existing records on the table. Because downstream systems may rely on existing Federated ID values, changing the fields can break those integrations.

The Federated ID Generation \(`com.glide.identity.globalid`\) plugin is auto-installed on all instances. Once the plugin is installed, the schema changes are as follows:

-   A column `federated_id` in the sys\_user table is created.
-   A table, `iamsync_type`, is auto-populated with the default configuration for the sys\_user table.

