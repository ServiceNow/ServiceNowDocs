---
title: Reclaiming user subscriptions
description: You can reclaim unused SaaS and SSO subscriptions to reduce your total software costs.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-asset-management/saas-license-management/reclaiming-user-subscriptions-saas.html
release: australia
product: SaaS License Management
classification: saas-license-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [SaaS License Management, Software Asset Management, IT Asset Management]
---

# Reclaiming user subscriptions

You can reclaim unused SaaS and SSO subscriptions to reduce your total software costs.

The process of reclaiming a user subscription is similar to reclaiming a software license in ServiceNow® Software Asset Management. You can reclaim user subscriptions in both the Software Asset Management Core UI and the Software Asset Workspace.

When you’re reclaiming a user subscription, you can determine the status of the associated removal candidate using the following removal candidate states.

<table id="table_xrr_gfs_dbb"><thead><tr><th>

State

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Attention Required

</td><td>

The removal candidate requires attention.The state is set to **Attention Required** when the **User** field is empty on an automatic removal candidate that has the **Notify User** option enabled. After the **User** field is populated, the state automatically changes to **Ready**.

 The state can also be set to **Attention Required** when a reclamation fails. After you resolve the error, the state automatically changes to **Ready**.

</td></tr><tr><td>

Ready

</td><td>

The removal candidate is ready for reclamation. Select **Reclaim** to advance the reclamation workflow.

</td></tr><tr><td>

Awaiting User

</td><td>

The user has been sent an email notification to approve or deny the removal request. This state is applicable only if the **Notify User** option is enabled on the removal candidate.

</td></tr><tr><td>

Awaiting Approval

</td><td>

The user must approve or deny the removal request. If the user wants to keep the subscription, the manager then becomes responsible for approving or declining the removal. This state is applicable only if the **Notify User** option is enabled on the removal candidate.

</td></tr><tr><td>

Awaiting Revocation

</td><td>

The removal candidate is awaiting reclamation.You can manually reclaim the user subscription in the removal candidate by selecting **Close Complete**. Alternatively, you can reclaim the user subscription through the **SAM — Updating Existing Reclamation Candidates** weekly scheduled job. When the scheduled job runs, removal candidates that are in the **Awaiting Revocation** state and have an empty **User subscription** field are automatically updated to the **Closed Complete** state.

 If the **User subscription** field is empty for a removal candidate that is in any other state, the reclamation workflow is canceled and the state automatically changes to **Closed Skipped**.

 The state of a removal candidate with restricted software is automatically set to **Awaiting Revocation**. The justification is set to **Restricted Software**.

</td></tr><tr><td>

Closed Complete

</td><td>

The user subscription has been reclaimed.

</td></tr><tr><td>

Closed Skipped

</td><td>

The user subscription hasn’t been reclaimed by the removal candidate.

</td></tr><tr><td>

Closed Canceled

</td><td>

The user subscription hasn’t been reclaimed by the removal candidate because user activity is detected.

</td></tr></tbody>
</table>-   **[Reclaim user subscriptions in Software Asset Management classic](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/saas-license-management/reclaim-user-subscription-saas-classic.md)**  
Reclaim unused SaaS and SSO subscriptions in the Software Asset Management classic application.
-   **[Reclaim user subscriptions in the Software Asset Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/saas-license-management/reclaim-user-subscription-saas-workspace.md)**  
Reclaim unused SaaS and SSO subscriptions in the Software Asset Workspace.

**Parent Topic:**[SaaS License Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/saas-license-management/sam-subscription-management.md)

**Related topics**  


[Request SaaS License Management]()

[SaaS License Management setup for large companies]()

[SaaS Overview dashboard]()

[Integrate with SaaS applications]()

[Integrate with SSO providers]()

[Playbook for SaaS integrations]()

[Viewing your SaaS and SSO subscriptions]()

[Review a software reclamation rule]()

[Create a child alias to set up multiple integration profiles]()

[Create a child alias to set up multiple Cisco Webex integration profiles]()

[Create a child alias to set up multiple Confluence Cloud integration profiles]()

[Create a child alias to set up multiple Jira integration profiles]()

[Associate a user with subscription records]()

[Disconnect SSO apps]()

[Delete an integration profile]()

[Subscription identifiers for SaaS and SSO applications]()

[Subscription exclusions for SaaS and SSO applications]()

[Reclamation rules for SaaS and SSO applications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/software-asset-management/reclamation-rules.md)

