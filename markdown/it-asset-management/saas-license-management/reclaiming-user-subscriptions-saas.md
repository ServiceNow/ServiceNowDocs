---
title: Reclaiming user subscriptions
description: You can reclaim unused SaaS and SSO subscriptions to reduce your total software costs.
locale: en-US
release: xanadu
product: SaaS License Management
classification: saas-license-management
topic_type: concept
last_updated: "2025-07-07"
reading_time_minutes: 9
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
</table>**Warning:** Make sure that users don't lose access to their files when their account is reclaimed. Users can't stop their account from being reclaimed unless the **Notify user** check box is selected on the reclamation rule.

-   Reclaiming an Adobe Cloud subscription removes the user's access to the application and the files that they have created.
-   Reclaiming an Adobe Workfront account removes the user's access to your Workfront application. The user is no longer allowed to sign in.
-   Reclaiming an Aha! account deactivates the account so that you can't log in to the Aha! portal.
-   Reclaiming an Asana account deletes the user account. The user can no longer access the Asana projects or workspaces. Content that was created by the user remains accessible to other users and the Admin can reassign the tasks from the Asana dashboard.
-   Reclaiming a Box account deletes the account. All the files are moved into a folder in the Box admin account that authenticated the integration.
-   Reclaiming a Calendly account removes the account from your organization.
-   Reclaiming a Cisco Webex subscription removes the user's access to the specific product. The user can still access all other Cisco Webex products and the free licenses assigned.
-   Reclaiming a Confluence Cloud account removes the user from all associated Confluence groups. Although the user can no longer access the Confluence site, all content that was created by the user remains accessible to other users.
-   Reclaiming a Dropbox account deletes the account. All the files are moved into a folder in the Dropbox admin account that authenticated the integration. The name of the created folder is the deleted user's email address.
-   Reclaiming a Docusign account deletes the account. The Docusign admin can access the user's files through the Docusign admin portal.
-   Reclaiming a Google Workspace account deletes the account. All the files are moved from the Google Drive into a folder in the Google Workspace admin account that authenticated the integration. The name of the created folder is the deleted user's email address. All email messages are deleted when the account is reclaimed. To transfer email messages, use the Google data migration service before reclaiming the account.
-   Reclaiming a GitHub Enterprise Server account suspends the account. All issues, comments, repositories, gists, and other data that the user created is preserved.

    Reclaiming a GitHub Enterprise Cloud account removes the account from all enterprise organizations. If you restore a user membership within three months of reclamation, the user's access to the private forks of your organization repositories is restored.

-   Reclaiming a product license from a GoTo user account removes the user's access to that product. Without a license, users can’t sign in to the product. If you reclaim all product licenses from a user account, the account is automatically suspended. Suspended users remain on the account but can't sign in to any products.
-   Reclaiming a Jira account removes the user from all the associated Jira groups. Although the user can no longer access the Jira site, all content that was created by the user remains accessible to other users.
-   Reclaiming a Looker account removes the user's access to Looker. Without an active account, the user can’t sign in to the Looker portal. The user’s usage history and personal content is retained.
-   Reclaiming a Microsoft 365 subscription removes the user's access to the application, associated plans, and services. If a user has access to an application through a group membership, reclaiming the subscription removes the user from the group and revoke access to the subscription and its associated plans.
-   Reclaiming a Microsoft Azure AD SSO application subscription removes the user's access to the application. If a user has access to an application through a group membership, you can't remove the group membership through reclamation. To reclaim the subscription, remove the user from the group in the Azure AD portal and then select **Close Complete**.
-   Reclaiming a Miro account removes the user's access to Miro. Without an active account, the user can’t sign in to the Miro portal.
-   Reclaiming an Okta SSO application subscription removes the user's access to the application. If a user has access to an application through a group membership, you can't remove the group membership through reclamation. To reclaim the subscription, remove the user from the group in the Okta Developer Console and then set the reclamation candidate state to **Close Complete**.
-   Reclaiming a PagerDuty account deletes the account.
-   Reclaiming a Rally account removes the user's access to Rally. Without an active account, the user can’t sign in to the Rally portal.
-   Reclaiming a Salesforce CRM account deactivates the user.
-   Reclaiming a Salesforce Marketing Cloud account deactivates the user.
-   Reclaiming an SAP SuccessFactors account deactivates the account.
-   Reclaiming a Slack account deactivates the user. Although messages and files are saved, the user is removed from all channels and signed out of your workspaces on all devices. The user isn’t allowed to sign back in.
-   Reclaiming a SmartRecruiters account removes access to the application. For example, you might want to reclaim the accounts of users who aren’t actively using the application or who have left the organization.
-   Reclaiming a Smartsheet account removes the user from your organization account. The user downgrades to a free collaborator with read-only access to the reports, sheets, sights, workspaces, and shared templates that haven’t been transferred to other users.
-   Reclaiming a Tableau Cloud account removes the user from all groups and their site role is changed to unlicensed. However, the user remains on the site unless they only have subscriptions and no other assets, in which case they’re removed from the site.
-   Reclaiming a Trello account removes your access to enterprise content or features. You can log in to Trello but can't access the boards and cards you logged in to before.
-   Reclaiming a Workplace from Facebook subscription removes the user's access to Workplace. Once the account is deactivated, the user can’t log in. But the posts, comments, and messages the user made would still be available.
-   Reclaiming a Zendesk account removes the user's access to your Zendesk application. The user is no longer allowed to sign in.
-   Reclaiming a Zoom account downgrades the account to Zoom Basic. All recorded meetings that were saved to the cloud are deleted. Locally saved recordings aren't affected.

-   **[Reclaim user subscriptions in Software Asset Management classic](../task/reclaim-user-subscription-saas-classic.md)**  
Reclaim unused SaaS and SSO subscriptions in the Software Asset Management classic application.
-   **[Reclaim user subscriptions in the Software Asset Workspace](../task/reclaim-user-subscription-saas-workspace.md)**  
Reclaim unused SaaS and SSO subscriptions in the Software Asset Workspace.

**Parent Topic:**[SaaS License Management](sam-subscription-management.md)

**Related topics**  


[Request SaaS License Management](../task/request-saas-license-management.md)

[SaaS Overview dashboard](saas-overview-dashboard.md)

[Playbook for SaaS integrations](playbook-saas-integrations.md)

[Integrate with SaaS applications](create-integration-profile.md)

[Integrate with SSO providers](saas-sso-integration.md)

[Create a child alias to set up multiple integration profiles](../task/create-child-alias-saas.md)

[Viewing your SaaS and SSO subscriptions](usage-summary-saas.md)

[SaaS License Connections](saas-license-connections.md)

[Review a software reclamation rule](../task/add-reclamation-rule-sub.md)

[Disconnect SSO apps](../task/disconnect-azure-ad-apps.md)

[Delete an integration profile](delete-saas-integration.md)

[Subscription identifiers for SaaS and SSO applications](subscription-identifiers.md#)

