---
title: Accessing Federated ID Criteria
description: Access Federated ID Criteria to see the ID fields selected to generate the Federated ID unique identifier. The default setting is User ID and email.
locale: en-US
release: australia
product: Identity
classification: identity
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Global Identity, Identity]
---

# Accessing Federated ID Criteria

Access Federated ID Criteria to see the ID fields selected to generate the Federated ID unique identifier. The default setting is User ID and email.

## Before you begin

Role required: iamsync\_admin

## Procedure

1.  Navigate to **All** &gt; **Manage Federated ID** &gt; **Federated ID Criteria**.

2.  The **Federated ID Criteria** page displays the record with the following details:

    -   Type Name: **User**
    -   Table Name: **User \[sys\_user\]**
    -   ID Fields: **user\_name \(User ID\), email** \(default\). Any fields listed below **Selected** are fields used for Federated ID generation.
    -   Status: **Completed** \(Federated ID generation status\). Available Status: **Ready**, **Running**, **Completed**, **Error**.
    **Note:**

    -   User ID is required for generating Federated IDs.
    -   User ID and email are used to generate Federated IDs by default.
    ![Federated ID Criterias page](../images/federated-id.png)

    **Note:** You can only change ID fields when generating new Federated IDs for the existing records. To know more, see [Updating ID fields](updating-id-fields.md).


