---
title: Configure Microsoft Azure Conditional Access for Microsoft Teams tenant
description: You must configure conditional access in Microsoft Azure to restrict users from accessing the production applications. Conditional access helps you from accidentally overriding your production integration with a custom or personal instance integration.
locale: en-US
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure VA for Teams, Conversational Integration with Microsoft Teams, Integrate VA with messaging apps, Integrate VA with other channels, Virtual Agent, Conversational Interfaces]
---

# Configure Microsoft Azure Conditional Access for Microsoft Teams tenant

You must configure conditional access in Microsoft Azure to restrict users from accessing the production applications. Conditional access helps you from accidentally overriding your production integration with a custom or personal instance integration.

## Before you begin

Roles required: virtual\_agent\_admin and user with Azure admin access.

## Procedure

1.  Log in to [Microsoft Azure portal](https://portal.azure.com/).

2.  Search for **Azure AD Conditional Access**.

3.  Navigate to **New Policy** &gt; **Create New Policy** and provide the policy a name.&lt;p&gt;

    ![The new conditional policy form prompts you for a name, user assignments, cloud apps or actions, conditions, and access controls.](../images/new-acl-policy.png)

4.  Under Users or Workload identities, select **0 users or workload identities selected**.

    A **What does this policy apply to?** pop-up is displayed.

5.  Under Include, select **All users**.

    ![Select All users on the pop-up to include all registered users.](../images/include-users-acl.png)

    **Note:** Selecting All users will include the users in the restriction policy.

6.  Under Exclude, select **Users and groups** to exclude admin users who have access to override the tenant.

    ![Exclude users to allow access.](../images/exclude-users-acl.png)

7.  Under Select excluded users, select **0 users and groups selected** to select an admin user and select **Select**.

8.  Under Cloud apps or actions, choose which assets to protect.

    For example, the NowBot or whatever the name of the ServiceNow bot is in Azure.

9.  Under Grant, select **0 controls selected** and select **Block access**.

10. In the Enable policy section, select **On** to turn on the Report-only function.

11. Select **Create**.

    After the ACL \(Access Control List\) is configured, it takes about 15 minutes fr the synchronization.


## Result

After the policy is created and the synchronization is complete, it restricts any user except the admins from overriding the tenant accidentally.

![Result of configuring conditional access for Microsoft Teams tenants. The policy is restricted for users other than admins.](../images/acl-restriction.png)

**Note:** The restriction does not affect the restricted users from using the Microsoft Teams or the Now Virtual Agent.

**Parent Topic:**[Configure Virtual Agent for Microsoft Teams](configure-va-msteams-settings.md)

