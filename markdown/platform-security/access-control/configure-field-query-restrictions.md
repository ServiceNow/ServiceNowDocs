---
title: Configure Field Query Restrictions
description: Learn how to configure a Field Query Restriction
locale: en-US
release: xanadu
product: Access Control
classification: access-control
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Field Query Roles and Restrictions, Access Management]
---

# Configure Field Query Restrictions

Learn how to configure a Field Query Restriction

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Tables**.

2.  Select a **Table**.

3.  Select a **Column Label** to view its **Dictionary** entry.

4.  Select the **Attributes** tab.

5.  **Tip:** If you do not have the **Field Query Restrict Record Access** field, select **New** to create one

    Select the **Field Query Restrict Record Access** attribute.

6.  Enter `true` in the **Value** field to restrict record access to only users who can who can view the field, otherwise enter `false`.

7.  Select **Update**


## Result

The table column will restrict the results of any queries. Restricted users will be informed how many results a query returned, but no further information.

