---
title: Configure webhooks from the tool record
description: Configure webhooks from the tool record to send data to DevOps Change Velocity after your tool is connected.
locale: en-US
release: yokohama
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Manage, DevOps Change Velocity, IT Service Management]
---

# Configure webhooks from the tool record

Configure webhooks from the tool record to send data to DevOps Change Velocity after your tool is connected.

## Before you begin

Role required: sn\_devops.admin or sn\_devops.tool\_owner in DevOps Change Velocity, and respective tool's admin access to access and configure webhooks.

## Procedure

1.  Navigate to **All** &gt; **Workspaces &gt; DevOps Change Workspace &gt; Tools**.

2.  Select the required tool to open the tool record.![Configure options in the tool record](../image/configure-tool-record.png)

3.  Select the **Configure** drop-down menu, and select one of the following actions.

    **Note:** You can also select the a Project, Plan, or Repository record and configure the corresponding webhooks for them specifically.

<table id="choicetable_wsy_mkv_w1c"><thead><tr><th align="left" id="d232813e95">

Options

</th><th align="left" id="d232813e98">

Description

</th></tr></thead><tbody><tr><td id="d232813e104">

**Auto configure with existing token**

</td><td>

Configures a webhook with your existing token.

</td></tr><tr><td id="d232813e113">

**Auto configure with new token**

</td><td>

Configures a webhook with a new token.

</td></tr><tr><td id="d232813e122">

**Configure manually**

</td><td>

-   [Configure webhooks in Azure DevOps manually](../concept/configure-test-webhooks.md#)
-   [Configure webhooks in GitHub manually](config-webhooks-github-manually.md)
-   [Configure webhooks in GitLab manually](configure-webhooks-in-gitlab.md)
-   [Configure webhooks in Jira manually](config-webhooks-jira-manually.md)
-   [Configure webhooks in Bitbucket manually](config-webhooks-bitbucket-manually.md)
-   [Configure webhooks in Argo CD manually](configure-webhooks-in-argo-cd-manually.md)
-   [Configure webhooks manually for Jenkins](configure-jenkins-plugin.md#)


</td></tr></tbody>
</table>    Webhooks are configured in your third-party tool's instance to send data to DevOps Change Velocity.


**Parent Topic:**[Managing DevOps Change Velocity](../concept/using-devops-change-velocity.md)

