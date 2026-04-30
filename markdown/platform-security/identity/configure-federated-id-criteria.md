---
title: Accessing Federated ID Criteria
description: Access Federated ID Criteria to know about the ID fields used to generated Federated ID.
locale: en-US
release: yokohama
product: Identity
classification: identity
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Global Identity, Identity]
---

# Accessing Federated ID Criteria

Access Federated ID Criteria to know about the ID fields used to generated Federated ID.

## Before you begin

Role required: iamsync\_admin

## Procedure

1.  Navigate to **All** &gt; **Manage Federated ID** &gt; **Federated ID Criteria**.

2.  The Federated ID Criterias page, displays the record with the following details:

    -   Type Name: **User**
    -   Table Name: **User \[sys\_user\]**
    -   ID Fields: **user\_name \(User ID\), email** \(default fields that are used for Federated ID generation\).
    -   Status: **Completed** \(Federated ID generation status\). Available Status: **Ready**, **Running**, **Completed**, **Error**.
    **Note:**

    -   User name is required for generating Federated IDs.
    -   User name and email are used to generate Federated IDs by default.
    ![Federated ID Criterias page](../images/federated-id.png)

    **Note:** Only the ID fields can be updated to generate a new Federated ID for the existing records. To know more, see [Updating ID fields](updating-id-fields.md).


