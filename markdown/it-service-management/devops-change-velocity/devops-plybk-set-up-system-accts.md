---
title: Set up integration user account in DevOps Change Velocity
description: Set up the integration user account to enable integrating with your third-party tools.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/devops-change-velocity/devops-plybk-set-up-system-accts.html
release: australia
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, DevOps Change Velocity, IT Service Management]
---

# Set up integration user account in DevOps Change Velocity

Set up the integration user account to enable integrating with your third-party tools.

## Before you begin

Role required: admin

## About this task

**Important:** This setup is required only when DevOps Config is installed, and for Rally and Split tool integrations. For all other tool integrations or if you’re using only DevOps Change Velocity, you can skip this procedure.

This is a one-time setup. You can set the integration user password either using Workspace or Classic UI.

The DevOps integration user is the ServiceNow system user that your third-party orchestration tools use to send data to DevOps Change Velocity.

The default integration user credential will be applicable for all the tools. However, if you want to set up separate integration user credential per tool connection you can also do the same but ensure that the user account has the sn\_devops.integration role assigned.

## Procedure

1.  Set the integration user password in one of the following ways.

<table id="choicetable_g4v_f5r_gwb"><thead><tr><th align="left" id="d42426e88">

Option

</th><th align="left" id="d42426e91">

Steps

</th></tr></thead><tbody><tr><td id="d42426e97">

**Using workspace**

</td><td>

1.  Navigate to **Workspaces** &gt; **DevOps Change Workspace**.
2.  From the Accounts and users widget on the Home page, select **Set up system accounts**. You’ll be redirected to **Administration &gt; Set up system accounts**.
3.  In the DevOps integration user account section, select **Set new password**.

\[Omitted image "setupsystemaccountwrk1.png"\] Alt text: Setting up new integration user password through workspace.

4.  By default, the DevOps integration user is selected. You can also select another user from the list.

\[Omitted image "setupsystemaccount-2.png"\] Alt text: Selecting a DevOps integration user through workspace.

**Note:** The **Username** field will only list the users that have the sn\_devops.integration role.

5.  Enter a password for the user and select **Set password**.

\[Omitted image "setupsystemaccount-3.png"\] Alt text: Selecting Set password for DevOps integration user account through workspace.

</td></tr><tr><td id="d42426e177">

**Using Classic UI**

</td><td>

Set a password for the DevOps integration user by navigating to **All** &gt; **User Administration** &gt; **Users**. For more information, see [Set password for a user](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/authentication/reset-your-password.md).

</td></tr></tbody>
</table>
## What to do next

-   [Onboard to DevOps Change Velocity using Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/devops-change-velocity/onboarding-using-devops-change-workspace.md)
-   [Start integrating DevOps Change Velocity with third-party tools](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/devops-change-velocity/integrating-devops-change-with-third-party-tools.md).

