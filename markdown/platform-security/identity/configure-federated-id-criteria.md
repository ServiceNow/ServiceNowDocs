---
title: Access Federated ID Criteria
description: Access Federated ID Criteria to learn about the ID fields used to generate Federated ID.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-security/identity/configure-federated-id-criteria.html
release: zurich
product: Identity
classification: identity
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Global Identity, Identity]
---

# Access Federated ID Criteria

Access Federated ID Criteria to learn about the ID fields used to generate Federated ID.

## Before you begin

Role required: iamsync\_admin

## Procedure

1.  Navigate to **All** &gt; **Manage Federated ID** &gt; **Federated ID Criteria**.

2.  Review the record details on the Federated ID Criteria page:

    -   Type Name: **User**
    -   Table Name: **User \[sys\_user\]**
    -   ID Fields: **user\_name \(User ID\), email** \(default fields that are used for Federated ID generation\).
    -   Status: **Completed** \(Federated ID generation status\). Available Status: **Ready**, **Running**, **Completed**, **Error**.
    **Note:**

    -   User name is required for generating Federated IDs.
    -   User name and email are used to generate Federated IDs by default.
    \[Omitted image "federated-id.png"\] Alt text: Federated ID Criteria page

    **Note:** Only the ID fields can be updated to generate a new Federated ID for the existing records. To learn more, see [Update ID fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/identity/updating-id-fields.md).


