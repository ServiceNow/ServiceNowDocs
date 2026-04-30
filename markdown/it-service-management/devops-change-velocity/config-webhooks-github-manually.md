---
title: Configure webhooks in GitHub manually
description: Configure webhooks in GitHub to send sync notifications to the DevOps Change Velocity application.
locale: en-US
release: yokohama
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [GitHub, Integrate, DevOps Change Velocity, IT Service Management]
---

# Configure webhooks in GitHub manually

Configure webhooks in GitHub to send sync notifications to the DevOps Change Velocity application.

## Before you begin

Role required: sn\_devops.admin or sn\_devops.tool\_owner in DevOps Change Velocity, GitHub admin

## About this task

You can also access manual configuration from the GitHub tool record in DevOps Change Velocity.

## Procedure

1.  In GitHub, navigate to **Settings** &gt; **Webhooks** and add a webhook.

2.  In DevOps Change Velocity, choose **Configure manually** when configuring the tool instance to send data.

    ![GitHub configure manually](../image/github-plybk-02.png)

3.  In DevOps Change Velocity, copy the **Webhook URL** field from the ServiceNow instance connection details for GitHub.

    **Note:** Select **Copy** in the appropriate field to copy the value to your clipboard. The field label changes to **Copied**, but you can copy multiple times.

    ![GitHub manually configure webhooks](../image/github-manual-webhooks-2.png)

4.  Modify the copied Webhook URL to reflect your tool details, and paste the URL in GitHub.

    For example:

    `https://myinstance.service-now.com/api/sn_devops/v2/devops/tool/{code | plan | artifact | orchestration | test | softwarequality }?toolId=23410545938c71d0db5bfe686cba1036`

    1.  Select one of the tool capabilities `{code | plan | artifact | orchestration | test | softwarequality }` to match your tool.

        For example:

        `https://myinstance.service-now.com/api/sn_devops/v2/devops/tool/orchestration?toolId=23410545938c71d0db5bfe686cba1036`

    2.  Copy the modified Webhook URL to the **Payload URL** field of the new webhook in GitHub.

5.  In DevOps Change Velocity, copy the **Secret token** field from the ServiceNow instance connection details for GitHub, and paste in the **Secret** field of the new webhook in GitHub.

    |From DevOps Change Velocity field|To GitHub field|
    |---------------------------------|---------------|
    |Webhook URL \(modified\)|Payload URL|
    |Secret token|Secret|

    ![GitHub configure webhooks manually](../image/github-manual-webhooks.png)


**Parent Topic:**[GitHub integration with DevOps Change Velocity](../concept/github-integration-dev-ops.md)

