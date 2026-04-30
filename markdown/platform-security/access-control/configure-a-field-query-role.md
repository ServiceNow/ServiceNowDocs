---
title: Configure a Field Query Role
description: Learn how to enable and configure a Field Query Role attribute.
locale: en-US
release: zurich
product: Access Control
classification: access-control
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Field Query Roles and Restrictions, Access Management]
---

# Configure a Field Query Role

Learn how to enable and configure a Field Query Role attribute.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Tables**.

2.  Select a **Table**.

3.  Select a **Column Label** to view its **Dictionary** entry.

4.  Select the **Attributes** tab.

5.  **Tip:** If you do not have the **Field Query Roles** field, select **New** to create one

    Select the **Field Query Roles** attribute.

6.  Enter the roles required to view this table column in the **Value**

7.  Select **Update**


## Result

The table column can only be queried by the roles defined in the **Field Query Roles** attribute. If a user without the defined roles queries the table column they will be denied access to the operation.

