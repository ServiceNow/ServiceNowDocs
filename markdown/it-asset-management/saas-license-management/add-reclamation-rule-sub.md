---
title: Review a software reclamation rule
description: Use reclamation rules to cancel user subscriptions that have limited to no activity.
locale: en-US
release: xanadu
product: SaaS License Management
classification: saas-license-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [SaaS License Management, Software Asset Management, IT Asset Management]
---

# Review a software reclamation rule

Use reclamation rules to cancel user subscriptions that have limited to no activity.

## Before you begin

Role required: sam\_admin

## About this task

When you create a direct integration profile or connect an SSO application, a reclamation rule is automatically created for the software. It's important that you review the reclamation rule to verify that it meets your specifications. For more information about the reclamation rules for each application, see [Reclamation rules](../reference/reclamation-rules.md) and [Reclamation rules for Microsoft 365 integration](../reference/m365-reclamation-rules.md).

For SSO subscriptions, the reclamation rule checks for user logins.

## Procedure

1.  Navigate to **All** &gt; **Software Asset** &gt; **Administration** &gt; **Reclamation Rules** and select the reclamation rule that corresponds to your integration profile.

2.  On the form, fill in the fields.

<table id="table_o23_2fh_nfb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name for the reclamation rule.

</td></tr><tr><td>

Applies to

</td><td>

Item type that the reclamation rule applies to.

</td></tr><tr><td>

Include usage from additional discovery sources

</td><td>

This field appears only when you are reviewing the Microsoft 365 reclamation rule. For more information, see [.](../reference/m365-reclamation-rules.md)

 When selected, the usage for Microsoft Access and Publisher is considered from additional discovery solutions such as Microsoft SCCM or ACC-V for E3 to E1 optimization.

</td></tr><tr><td>

Notify user

</td><td>

Option for notifying users via email that their accounts will be reclaimed unless they respond with a request to keep the accounts. If a user wants to keep a license, it becomes the responsibility of the manager to approve or reject the removal of the license.

</td></tr><tr><td>

Days before auto-reclamation

</td><td>

If no response is received from the user within the specified number of days, the account is reclaimed.**Note:** This field appears when **Notify user** is selected.

</td></tr><tr><td class="sub-head" colspan="2">

Subscription Usage Condition

</td></tr><tr><td>

Last activity threshold

</td><td>

Time limit for no meaningful activity before a user account is added to the list of reclamation candidates. The default value is 60 days for direct integrations and 30 days for SSO applications.

</td></tr></tbody>
</table>3.  Select **Update**.


## What to do next

View the reclamation candidates that are identified by your reclamation rule and start reclaiming user subscriptions.

**Parent Topic:**[SaaS License Management](../concept/sam-subscription-management.md)

**Related topics**  


[Request SaaS License Management](request-saas-license-management.md)

[SaaS Overview dashboard](../concept/saas-overview-dashboard.md)

[Playbook for SaaS integrations](../concept/playbook-saas-integrations.md)

[Integrate with SaaS applications](../concept/create-integration-profile.md)

[Integrate with SSO providers](../concept/saas-sso-integration.md)

[Create a child alias to set up multiple integration profiles](create-child-alias-saas.md)

[Viewing your SaaS and SSO subscriptions](../concept/usage-summary-saas.md)

[SaaS License Connections](../concept/saas-license-connections.md)

[Reclaiming user subscriptions](../concept/reclaiming-user-subscriptions-saas.md)

[Disconnect SSO apps](disconnect-azure-ad-apps.md)

[Delete an integration profile](../concept/delete-saas-integration.md)

[Subscription identifiers for SaaS and SSO applications](../concept/subscription-identifiers.md#)

[Reclamation rules for Microsoft 365 integration](../reference/m365-reclamation-rules.md)

