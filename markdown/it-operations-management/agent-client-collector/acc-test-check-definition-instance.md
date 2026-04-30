---
title: Test a check definition or check instance
description: When working with a check definition or check instance, you can test the check against its assigned agent to ensure that the check is configured properly.
locale: en-US
release: zurich
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Create and edit checks, Collecting data from your system devices, ACC deployment - shared between servers and endpoints, Agent Client Collector, IT Operations Management]
---

# Test a check definition or check instance

When working with a check definition or check instance, you can test the check against its assigned agent to ensure that the check is configured properly.

## Before you begin

Role required: agent\_client\_collector\_admin

## Procedure

1.  Navigate to **All** &gt; **Agent Client Collector** &gt; **Check Definitions**.

2.  Select a check definition from the list.

    **Note:** When running a Test Check in a check instance:

    1.  Navigate to **Agent Client Collector** &gt; **Policies**.
    2.  Select a policy.
    3.  Select a check instance in the policy.
    Continue with the following steps in this procedure.

3.  In the **Related Links** section, click **Test Check**.

    The **Test Check** dialog box appears.

    ![Test Check dialog box](../image/ACC-test-check-dialog.png)

4.  Configure the fields in the dialog box.

<table id="table_z3w_rsd_3cc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Check Definition

</td><td>

Displays the name of the selected check definition.

</td></tr><tr><td>

CI

</td><td>

Select the CI on which to run the check. The available options are those CIs which meet both of the following criteria: -   Belong to the group specified in the **Check group** field.
-   Belong to an agent with **Up** status.
If the **Check group** field is empty, the value defaults to **cmdb\_ci\_computer**.

</td></tr><tr><td>

Credentials

</td><td>

Select the credentials of the user whom you want the agent to connect with.This field appears only if you have configured secure check parameters on the **Check Secure Parameter Definitions** tab in the Check Definition.

</td></tr><tr><td>

Proxy agent

</td><td>

Select a proxy agent to be associated with the check.This field appears only when working with a check instance and when one of the options has been selected on the **Proxy Settings** tab in the instance's policy.

</td></tr></tbody>
</table>
