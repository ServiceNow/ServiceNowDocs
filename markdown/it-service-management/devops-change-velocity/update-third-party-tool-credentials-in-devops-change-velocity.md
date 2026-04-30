---
title: Update third-party tool credentials in DevOps Change Velocity
description: If your tool credential has changed, you must update the credentials in your ServiceNow instance to avoid getting disconnected.
locale: en-US
release: xanadu
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Integrate, DevOps Change Velocity, IT Service Management]
---

# Update third-party tool credentials in DevOps Change Velocity

If your tool credential has changed, you must update the credentials in your ServiceNow instance to avoid getting disconnected.

## Before you begin

Role required: sn\_devops.admin

## Procedure

1.  Update your tool credentials using one of the following methods.

<table id="choicetable_bvm_p5l_f5b"><thead><tr><th align="left" id="d45161e66">

Option

</th><th align="left" id="d45161e69">

Steps

</th></tr></thead><tbody><tr><td id="d45161e75">

**From Workspace**

</td><td>

1.  Navigate to **Workspaces &gt; DevOps Change Workspace &gt; Tools &gt; &lt;tool type&gt;**.
2.  Select the tool for which you want to update your credentials.
3.  In the tool record, select **More Actions\(![More Actions icon](../../itsm-workspace/image/more-actions-icon.png) \) &gt; Update credentials**.
4.  Select the **Credential type**.

    -   If the credential type is **Basic Auth**, enter the new password or access token.
    -   If the credential type is **OAuth**, enter the new credential.
**Note:** This step is only applicable for tools which support OAuth 2.0 based authentication.

5.  Enter the updated credentials in the corresponding field.

**Note:** You can change your password/token, username, or authentication type.

6.  Select **Check permissions** to verify if the required permissions are available.

**Note:** If you are connecting to GitHub, for OAuth 2.0 and GitHub App credential, the GitHub app slug name is required to check permissions. If it is not provided, tool credentials will be updated without checking permissions.

7.  Select **Update credentials** to update the credentials. The tool will be in the disconnected state.
8.  Select **Connect** to establish the connection.


</td></tr><tr><td id="d45161e159">

**From Classic**

</td><td>

1.  Navigate to **All &gt; DevOps &gt; Tools &gt; &lt;tool type&gt;**.
2.  Select the tool for which you want to update your credentials.
3.  From the Tool connections related list, select the credential record.
4.  Enter the updated credentials in the corresponding field, and select **Save**. The tool will be in the disconnected state.
5.  Select **Connect** to establish the connection.


</td></tr></tbody>
</table>
-   **[Notifications on tool credential expiration](../concept/notifications-for-tool-credential-expiry.md)**  
Notifications are sent to tool users on expiration of tool credentials to alert them. Notifications are also sent proactively before the expiration of tool credentials for GitHub tools created with basic authentication. This enables tool users with the sn\_devops.tool\_owner or sn\_devops.admin roles to update the tool credentials and prevent any loss of data.

**Parent Topic:**[Integrating DevOps Change Velocity with third party tools](../concept/integrating-devops-change-with-third-party-tools.md)

