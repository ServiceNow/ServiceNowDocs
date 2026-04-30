---
title: Test check dialog box fields
description: The dialog box fields when testing a check definition.
locale: en-US
release: yokohama
product: Agent Client Collector
classification: agent-client-collector
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Agent Client Collector check definition page, Agent Client Collector Framework reference, Agent Client Collector Framework, Agent Client Collector, IT Operations Management]
---

# Test check dialog box fields

The dialog box fields when testing a check definition.

<table id="table_isr_nd4_mxb"><thead><tr><th>

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

Select the CI on which to run the check. The available options are those CIs which meet both of the following criteria:-   Belong to the group specified in the **Check group** field.
-   Belong to an agent with **Up** status.

If the **Check group** field is empty, the value defaults to **cmdb\_ci\_computer**.

</td></tr><tr><td>

Credentials

</td><td>

Select the credentials of the user whom you want the agent to connect with.This field appears only if you have configured secure check parameters on the **Check Secure Parameter Definitions** tab in the Check Definition.

</td></tr><tr><td>

Proxy Agent

</td><td>

Select a proxy agent to be associated with the check.This field appears only when working with a check instance and when one of the options has been selected on the **Proxy Settings** tab in the instance's policy.

</td></tr></tbody>
</table>**Parent Topic:**[Agent Client Collector check definition page](check-definition-form.md)

