---
title: Configuring Federated ID Criteria
description: Access and configure Federated ID Criteria to see the ID fields selected to generate the Federated ID unique identifier. The default setting is User ID and email.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/identity/configure-federated-id-criteria.html
release: brazil
product: Identity
classification: identity
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Global Identity, Identity]
---

# Configuring Federated ID Criteria

Access and configure Federated ID Criteria to see the ID fields selected to generate the Federated ID unique identifier. The default setting is User ID and email.

## Before you begin

Role required: iamsync\_admin

## Procedure

1.  Navigate to **All** &gt; **Manage Federated ID** &gt; **Federated ID Criteria**.

    The **Federated ID Criteria** page displays Role and User record.

2.  Select the record, the following details are displayed:

    -   Type Name: **User**
    -   Table Name: **User \[sys\_user\]**
    -   ID Fields: **user\_name \(User ID\), email** \(default\). Any fields listed as **Selected** are those fields that can be used for Federated ID generation.
    -   ID Fields: **user\_name \(User ID\), email** \(default\). Any fields listed as **Selected** are those fields that can be used for Federated ID generation. You can change these fields, as long as the selection includes at least one unique field.
    -   Status: **Completed** \(Federated ID generation status\). Available Status: **Ready**, **Running**, **Completed**, **Error**.
    **Note:**

    -   The ID fields must include at least one unique field. User ID is no longer mandatory — it qualifies as a unique field, but you can select any other unique field instead.
    -   Only a field marked unique in the dictionary or a field with a single-column unique database index can be selected as a unique field.
    -   User ID and email are used to generate Federated IDs by default.
    \[Omitted image "federated-id.png"\] Alt text: Federated ID Criterias page

    **Note:** You can only change ID fields when generating new Federated IDs for the existing records. To know more, see [Updating ID fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/identity/updating-id-fields.md).


