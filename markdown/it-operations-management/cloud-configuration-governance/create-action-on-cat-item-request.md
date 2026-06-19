---
title: Create an action for an 'on Catalog item request start/end' policy
description: The on Catalog item request start trigger fires after the user opens a request form. The on Catalog item request end trigger fires after a user submits a request form. A policy that is triggered by the on Catalog item request start or on Catalog item request end trigger can run a script or execute a subflow.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/cloud-configuration-governance/create-action-on-cat-item-request.html
release: zurich
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Create a cloud policy, Policies for Cloud Provisioning, Cloud Admin Portal, Cloud Provisioning and Governance administration guide, Cloud Provisioning and Governance, ITOM Cloud Accelerate, IT Operations Management]
---

# Create an action for an 'on Catalog item request start/end' policy

The on Catalog item request start trigger fires after the user opens a request form. The on Catalog item request end trigger fires after a user submits a request form. A policy that is triggered by the on Catalog item request start or on Catalog item request end trigger can run a script or execute a subflow.

## Before you begin

-   Role required: sn\_cmp.cloud\_governor or admin
-   Optional: [Create one or more cloud policy groups](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/cloud-configuration-governance/create-cloud-policy-group.md).
-   [Configure a cloud policy rule](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/cloud-configuration-governance/configure-cloud-policy-rule.md) and associated conditions.

## Procedure

1.  In the Cloud Admin Portal, navigate to **Govern** &gt; **Policies**.

2.  Open a cloud policy and set the policy to the **Draft** state if needed.

3.  Open the rule that should perform the action and then click **New** on the Policy Rule Actions related list.

4.  On the popup, click **Create** for the type of action to perform, enter a unique and meaningful **Action Name**, and then fill in the form for the action.

    \[Omitted image "action-on-cat-item-startstop.png"\] Alt text: Create Action popup

<table id="table_nbq_j2h_sfb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Action Script Category

</td><td>

Select a category.

</td></tr><tr><td>

Action Script Name

</td><td>

Specify a unique and meaningful name for the script.

</td></tr><tr><td>

Action Script

</td><td>

Create the script in the text box.See [Create a policy action script](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown) for details.

</td></tr></tbody>
</table>    \[Omitted image "action-wf-on-cat-item-end.png"\] Alt text: Selecting a workflow as the policy action

    |Field|Description|
    |-----|-----------|
    |Action Name|Specify a unique and meaningful name for the action that starts the subflow.|
    |Subflow|Select the subflow to execute.|


**Parent Topic:**[Create a cloud policy](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/cloud-configuration-governance/create-cloud-policy.md)

