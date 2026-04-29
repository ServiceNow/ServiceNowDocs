---
title: Check permissions and update credentials for tools — Workspace
description: You can perform permission checks and update credentials like passwords and access tokens for your tools from the tool details page.
locale: en-US
release: australia
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Manage, DevOps Change Velocity, IT Service Management]
---

# Check permissions and update credentials for tools — Workspace

You can perform permission checks and update credentials like passwords and access tokens for your tools from the tool details page.

## Permission checks

You can perform permission checks on connected tools at any time, to verify if the existing credentials have the necessary permissions. This check helps to determine if there are possible impacts or if you must get a token or credential with higher-level permissions for the tool.

**Note:**

SonarQube and Rally doesn't have the option to check for permissions.

1.  From the DevOps Change Workspace, navigate to Tools and select the tool to open the details page.

    The **Permission check result** field shows whether the tool credentials have all the necessary permissions, have partial permissions, or if permissions haven't been checked. The **Last Permission check** field tells you when the permission checks were previously run.

2.  Click **More Actions**.

    -   For Bitbucket, select **Check password permissions**.
    -   For GitHub and GitHub Enterprise with OAuth credentials using the GitHub app, select **Check credential permissions** and then enter the **GitHub app slug name**. Click **Check permissions**.
    -   For others, select **Check credential permissions**.
    You can see the status of the checks depending on your credential permissions. You need sufficient permissions on your credentials for seamless discovery and import.

3.  If permissions aren’t sufficient, it’s recommended to update the credentials with those having higher-level permissions, or update the permissions for the objects on the external tool.

## Update credentials

You can update the tool credentials with credentials having sufficient permissions for seamless discovery and import of data from your tool.

1.  From the DevOps Change Workspace, navigate to Tools and select the tool to open the details page.
2.  Click **More Actions**. Depending on your tool, the options to update your credentials are displayed.

<table id="table_rzp_vrj_bwb"><thead><tr><th>

Tool

</th><th>

Steps

</th></tr></thead><tbody><tr><td>

Bitbucket

</td><td>

1.  Click **Update password**.
2.  Enter the user name and the new password.
3.  Click **Check permissions**.
4.  The permission check results are shown in the Permission check dialog box. If you are satisfied with the permissions for your tool, then update the credentials.


</td></tr><tr><td>

Azure DevOps

</td><td>

1.  Click **Update credentials**.
2.  Select the **Credential type**.
    -   If the credential type is **Basic Auth**, enter the new password or access token.
    -   If the credential type is **OAuth**, enter the new credential.
3.  Click **Check permissions**.
4.  The permission check results are shown in the Permission check dialog box. If you’re satisfied with the permissions for your tool, then update the credentials.

**Note:** Since the DevOps tool maps to an Azure DevOps organization, the **Project Administrators** privilege requires the owner of the PAT to be a member of the organization's **Project Collection Administrators** group.

</td></tr><tr><td>

Jira, Jenkins, JFrog

</td><td>

1.  Click **Update credentials**.
2.  Select the **Credential type**.

    -   If the credential type is **Basic Auth**, enter the new password or access token.
    -   If the credential type is **OAuth**, enter the new credential.
**Note:** OAuth 2.0 credentials are not available for Jenkins and JFrog.

3.  Click **Check permissions**.
4.  The permission check results are shown in the Permission check dialog box. If you’re satisfied with the permissions for your tool, then update the credentials.


</td></tr><tr><td>

GitLab

</td><td>

1.  Click **Update credentials**.
2.  Select the **Credential type**.
    -   If the credential type is **Basic Auth**, enter the new password or access token.
    -   If the credential type is **OAuth**, enter the new credential.
3.  Click **Check permissions**.
4.  The permission check results are shown in the Permission check dialog box. If you’re satisfied with the permissions for your tool, then update the credentials.


</td></tr><tr><td>

GitHub, GitHub Enterprise

</td><td>

1.  Click **Update credentials**.
2.  Select the **Credential type**.
    -   If the credential type is **Basic Auth**, enter the user name and new password or access token.
    -   If the credential type is **OAuth** using the GitHub app, enter the new credential. If you don't want to check for permissions, then click **Update** directly, and the credentials are updated.

To check the permissions, you must enter the **GitHub app slug name**.

    -   If the credential type is OAuth using the OAuth app \(not the GitHub app\) at GitHub end, enter the new credential.
3.  Click **Check permissions**.
4.  The permission check results are shown in the Permission check dialog box. If you're satisfied with the permissions for your tool, then update the credentials.


</td></tr><tr><td>

Argo CD, SonarQube, Rally

</td><td>

These tools don't check for permissions. To update credentials:1.  Click **Update credentials**.
2.  Enter the user name and new password or access token.
3.  Click **Update** to update the credentials.


</td></tr></tbody>
</table>    Permission checks are run on the new credentials. Once permissions check is completed, you can proceed with updating the credentials. If you want to abort the update, click **Cancel**.


-   **[Permissions required for DevOps tools](tool-req-permission.md)**  
Permissions required in your third-party tool to connect to DevOps Change Velocity.

**Parent Topic:**[Managing DevOps Change Velocity](../concept/using-devops-change-velocity.md)

