---
title: Edit a log policy
description: You can edit published Agent Client Collector log policies. For example, modify a default log policy if your organization always uses a specific non-default log path.
locale: en-US
release: australia
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Agent Client Collector log policies, Agent Client Collector Log Analytics, Agent Client Collector, IT Operations Management]
---

# Edit a log policy

You can edit published Agent Client Collector log policies. For example, modify a default log policy if your organization always uses a specific non-default log path.

## Before you begin

Role required: agent\_client\_collector\_admin

## Procedure

1.  Navigate to **All** &gt; **ACC Log Analytics** &gt; **ACC Log Policies**.

2.  Select a policy for which the **Publish status** is **Published**.

3.  Select **Edit in Sandbox**.

    The policy is now in **Draft view**, and its fields and check instances are editable.

    **Note:** Although the policy is in **Draft view**, its publish status remains **Published**.

4.  On the **Monitored CIs** tab, edit the CIs to which the policy applies as needed.

    1.  Choose the CI type to be monitored.

        -   **Monitored CI type by filter**: Select the monitored CI type. You can narrow down the CIs that will be monitored by using filter conditions.
        -   **Monitored CI type by script**: Specify the monitored CIs by using a script.
        -   **Monitored CI type by CMDB Group**: Specify the monitored CIs by using CMDB group queries.
        For more information about choosing monitored CI types, see [Create a new Agent Client Collector policy](create-edit-policies.md).

    2.  Monitor only CIs that are associated with an Application Service by selecting **Filter Monitored CIs by Application Service**.

        You can specify the Application Services to be monitored by using filter conditions. Agent Client Collector will only retrieve the logs of CIs that are associated with these Application Services.

5.  In the **Check Instances** table, select the log shipper check instance record and edit it.

    For more information, see [Edit log path configurations](accl-edit-log-path.md).

6.  Select **Save** to save the changes you entered into the Sandbox policy fields.

    The policy remains in **Draft view**, and the **Publish status** is **Published\***. The asterisk \(\*\) indicates that the current published version is not the most up to date one, because it contains saved changes that have not yet been published.

7.  Select **Republish** to publish the updates.

    The policy returns to **Published** state and opens as the published policy.

    **Note:** This option appears only after entering updates into the policy fields, for a policy whose **Publish status** is **Published\***.

8.  Determine the active status of the policy by selecting either **Activate** or **Deactivate**.

9.  Select **Delete** to delete both the Published and the draft policies.


