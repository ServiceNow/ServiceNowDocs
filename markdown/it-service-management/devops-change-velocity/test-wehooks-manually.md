---
title: Test webhooks manually
description: For tools including GitLab, Rally, Split.io, Jira, Bitbucket, and Argo CD, you have to test webhooks manually if there is any issue with the connection.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/devops-change-velocity/test-wehooks-manually.html
release: australia
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Manage, DevOps Change Velocity, IT Service Management]
---

# Test webhooks manually

For tools including GitLab, Rally, Split.io, Jira, Bitbucket, and Argo CD, you have to test webhooks manually if there is any issue with the connection.

## GitLab

Role required:

-   GitLab: GitLab admin privileges
-   DevOps Change: sn\_devops.admin or sn\_devops.tool\_owner

To test webhooks manually in GitLab, you must:

1.  Navigate to GitLab and select the project for which you want to test webhooks.
2.  Navigate to **Settings** &gt; **Webhooks**.

    When your project is configured in DevOps Change Velocity, webhooks are created for that project in GitLab. These webhooks are available under **Project Hooks**.

    \[Omitted image "test-wh-man-01.png"\] Alt text: Webhooks in GitLab.

    For each project, two webhooks are created. One is for code events and the other for orchestration events.

3.  To test a webhook, select **Test** and select **Push events** from the list.

    \[Omitted image "test-wh-man-02.png"\] Alt text: Test the webhook.

    **Note:** You can test for other events as well, for example Tag push events.

    -   If the webhook is configured correctly, you’ll receive a success message. For example:

        \[Omitted image "test-wh-man-03.png"\] Alt text: Success message.

    -   If the webhook is configured incorrectly, you’ll receive an error message. For example:

        \[Omitted image "test-wh-man-04.png"\] Alt text: Error message.

        To fix a webhook, you can try the following options:

        -   Reconfigure the webhooks by selecting **Configure** from the project record page in DevOps Change Velocity. This reconfigures all the existing webhooks for the project.
        -   Select **Edit** for the webhook and verify if the **toolId** is correct in the **URL** field. Verify if the **Secret token** is correct.

            You can find the correct values in the tool record page in DevOps Change Velocity.

            \[Omitted image "test-wh-man-05.png"\] Alt text: Check webhook fields.


For detailed information about webhooks in GitLab, see [Webhooks](https://docs.gitlab.com/ee/user/project/integrations/webhooks.html).

## Rally

Role required:

-   Rally: Rally admin privileges
-   DevOps Change: sn\_devops.admin or sn\_devops.tool\_owner

Rally doesn't provide an option to directly test for webhook connectivity. If you're not seeing Rally events in DevOps Change Velocity, you can try the following options:

-   From your Rally instance, navigate to **My Settings** &gt; **System Administration** &gt; **Extensions** &gt; **Webhooks**.

    Check if there’s a corresponding webhook created for your DevOps Change instance, and that it’s **Active**.

    \[Omitted image "test-wh-man-06.png"\] Alt text: Webhooks in Rally.

-   Reconfigure the webhook by selecting **Configure** from the project record page in DevOps Change Velocity. This reconfigures the existing webhook for the project.

For detailed information about webhooks in Rally, see [Manage Webhooks](https://techdocs.broadcom.com/us/en/ca-enterprise-software/valueops/rally/rally-help/administration/configure-your-subscription/manage-webhooks.html#:~:text=Webhooks%20are%20usually%20triggered%20by,to%20invoke%20behavior%20on%20another.).

## Split.io

Role required:

-   Split.io: Split.io admin privileges
-   DevOps Change: sn\_devops.admin or sn\_devops.tool\_owner

Split.io doesn't provide an option to directly test for webhook connectivity. If you're not seeing Split.io events in DevOps Change Velocity, you can try the following options:

-   From your Split.io instance, navigate to **Admin Settings** &gt; **Integration settings** &gt; **Integrations**. Select the **Configured** tab, and select **Edit** for the ServiceNow DevOps application.

    \[Omitted image "test-wh-man-07.png"\] Alt text: Configure ServiceNow DevOps application.

    Check if the ServiceNow DevOps application is configured correctly in Split.io. For details on configuring, see [Enable integration with ServiceNow DevOps in Split tool](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/devops-change-velocity/enable-integration-servicenow-devops-split.md).

-   Check if the status of the ServiceNow DevOps application is **Active**.

    \[Omitted image "test-wh-man-08.png"\] Alt text: ServiceNow DevOps application.

-   Reconfigure the webhook by selecting **Configure** from the tool record page in DevOps Change Velocity. This reconfigures the existing webhook for the Split.io tool.

You can also refer to [ServiceNow integration with Split.io](https://help.split.io/hc/en-us/articles/5524203735181-ServiceNow).

## Jira

Role required:

-   Jira: Jira admin privileges
-   DevOps Change: sn\_devops.admin or sn\_devops.tool\_owner

Jira doesn't provide an option to directly test for webhook connectivity. If you're not seeing Jira events in DevOps Change Velocity, you can try the following options:

-   Navigate to:

    -   For Jira Server navigate to **Administration** &gt; **System** &gt; **WebHooks**.
    -   For Jira Cloud instance, navigate to **Settings** &gt; **System** &gt; **WebHooks**.
    Check if there’s a corresponding webhook created for your DevOps Change instance.

    \[Omitted image "test-wh-man-09.png"\] Alt text: Webhook for DevOps Change.

-   Select **Edit** for the webhook.

    -   Check if the status is **Enabled**.
    -   Check if the **Tool ID** in the **URL** field is correct. The **Tool ID** is the value after **?toolId=**.
    -   Check if the secret token in the **URL** field is correct. Token value is at the end of the URL, after **token=**.
    \[Omitted image "test-wh-man-10.png"\] Alt text: Webhook fields.

    You can find the correct values of the **Tool ID** and **Secret token** in the tool record page in DevOps Change Velocity.

    For detailed information about webhooks in Jira, see [Webhooks](https://developer.atlassian.com/server/jira/platform/webhooks/).

-   Reconfigure the webhook by selecting **Configure** from the tool record page in DevOps Change Velocity. This reconfigures the existing webhook for the Jira tool.

    **Note:**

    If you have connected your Jira tool using OAuth 2.0 based authentication, the webhooks are created for the OAuth 2.0 integration app in Jira when you configure automatically, whereas if you have connected using basic authentication, the webhooks are created for all your projects in Jira. If you choose to configure the webhooks manually for a Jira tool created using OAuth 2.0 based authentication, a duplicate webhook may get created.


## Bitbucket

Role required:

-   Bitbucket: Bitbucket admin privileges
-   DevOps Change: sn\_devops.admin or sn\_devops.tool\_owner

Bitbucket doesn't provide an option to directly test for webhook connectivity. If you're not seeing Bitbucket events in DevOps Change Velocity, you can try the following options:

-   Navigate to Bitbucket and select the repository for which you want to test webhooks. Navigate to **Repository settings** &gt; **Workflow** &gt; **Webhooks**.

    Check if there’s a corresponding webhook created for your DevOps Change instance.

    \[Omitted image "test-wh-man-11.png"\] Alt text: Repository webhooks.

-   Select **Edit** for the webhook.

    -   Check if the status is **Active**.
    -   Check if the **Tool ID** in the **URL** field is correct. The **Tool ID** is the value after **/event/**.
    -   Check if the secret token in the **URL** field is correct. Token value is at the end of the URL, after **token=**.
    You can find the correct values of the **Tool ID** and **Secret token** in the tool record page in DevOps Change Velocity.

    \[Omitted image "test-wh-man-12.png"\] Alt text: Repository settings.

    For detailed information about webhooks in Bitbucket, see [Manage webhooks](https://support.atlassian.com/bitbucket-cloud/docs/manage-webhooks/).

-   Reconfigure the webhook by selecting **Configure** from the tool record page in DevOps Change Velocity. This reconfigures the existing webhook for the Bitbucket tool.

## Argo CD

Role required:

-   Argo CD: Argo CD admin privileges
-   DevOps Change: sn\_devops.admin or sn\_devops.tool\_owner

Argo CD doesn't provide an option to directly test for webhook connectivity. To configure webhooks, see [Configure webhooks in Argo CD manually](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/devops-change-velocity/configure-webhooks-in-argo-cd-manually.md).

**Parent Topic:**[Managing DevOps Change Velocity](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/devops-change-velocity/using-devops-change-velocity.md)

