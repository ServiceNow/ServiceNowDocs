---
title: Configure the AWS Config service to send event notifications to the ServiceNow instance
description: Configure the Amazon Web Services \(AWS\) Config service to send event notifications to the ServiceNow instance for any changes in the lifecycle state of a resource.
locale: en-US
release: australia
product: Discovery
classification: discovery
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [AWS events-driven discovery, Discovery for AWS, Discovery for cloud environment, Discovery, ITOM Visibility, IT Operations Management]
---

# Configure the AWS Config service to send event notifications to the ServiceNow instance

Configure the Amazon Web Services \(AWS\) Config service to send event notifications to the ServiceNow instance for any changes in the lifecycle state of a resource.

## Before you begin

-   Ensure that the Discovery \(com.snc.discovery\) plugin is installed and activated in the instance.
-   Ensure that you have valid AWS subscriptions \(service accounts\) and its associated logical datacenters are discovered.
-   Ensure that the user account password used to subscribe the instance to the Simple Notification Service \(SNS\) does not contain the @ or \# characters.

Roles required:

-   Ensure that an AWS role is available that can access the following services and resources:
    -   SNS
    -   AWS Config service
    -   Resource types for which you want to track the configuration change
-   ServiceNow roles:
    -   discovery\_admin
    -   sn\_cmp.cloud\_event\_integration: The access credentials of a ServiceNow user with the sn\_cmp.cloud\_event\_integration role is required to subscribe the instance to the SNS notifications. For more information, see [Create a user](https://www.servicenow.com/docs/access?context=t_CreateAUser&version=australia&pubname=australia-platform-administration&ft:locale=en-US) and [Assign a role to a user](https://www.servicenow.com/docs/access?context=t_AssignARoleToAUser&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

## About this task

The ServiceNow® event-driven discovery uses the events to update the latest resource information in the Configuration Management Database \(CMDB\). For more information, see [AWS events-driven discovery](../concept/aws-events-driven-discovery.md).

Many of the steps in the topic are performed in the AWS portal. For more information, see the following AWS documents:

-   [Set Up Amazon SNS Notifications](https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/US_SetupSNS.html)
-   [Viewing the AWS Config dashboard](https://docs.aws.amazon.com/config/latest/developerguide/viewing-the-aws-config-dashboard.html)

**Note:**

If you're using domain separation for Cloud Discovery, the events are also domain-separated. Therefore, you can view the details of a processed event only if it belongs to your domain. If an event isn’t associated with any service account, then it’s associated with the global domain.

During event processing, the Cloud Event Scheduler identifies the domain of the service account and assigns to the event. If an error occurs in identifying the domain before processing, the event can sometimes stay unassigned and become visible to all domains. To prevent the failed events visibility to all domains, you can set the **sn\_cmp.error\_events.default\_domain** property to sys\_id of the service-provider domain so that the failed events appears only to the service-provider domain administrator.

## Procedure

1.  Log in to the AWS account.

2.  On the Services page, navigate to **AWS Services** &gt; **Find Services** &gt; **Simple Notification Service**.

3.  Create an Amazon SNS topic.

    The AWS Config service uses the SNS topic to publish the event notifications.

    1.  On the SNS dashboard, navigate to **Topics** &gt; **Create topic**.

    2.  On the form, fill in the fields.

<table id="table_mmk_v31_wvb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Type

</td><td>

Notification topic type.Select the **Standard** topic type.

</td></tr><tr><td>

Name

</td><td>

Name of the SNS topic.

</td></tr><tr><td>

Display name - optional

</td><td>

Display name of the SNS topic.

</td></tr></tbody>
</table>    3.  Select **Create topic**.

4.  Subscribe the instance to the SNS topic.

    After subscribing to the SNS topic, the instance can receive the event notifications from the AWS cloud.

    1.  On the Topic Details page, select **Create subscription**.

    2.  On the form, fill in the fields.

<table id="table_c51_rj1_wvb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Protocol

</td><td>

Communication protocols to use.For the subscription that auto-updates the CMDB, select HTTPS.

**Note:** After creating the HTTPS subscription, you can create a separate subscription that sends emails to a specified person.

</td></tr><tr><td>

Endpoint

</td><td>

URL of the ServiceNow Cloud Events REST API.Ensure that the URL adheres to the following syntax:

```
https://<username>:<user_password>@<instance_URL>/api/now/cloud_event
```

Use the alternate endpoint if there is any expectation of high load from AWS. High load on default endpoint can significantly slow down the instance as default endpoint is also used for other transactions.

Ensure that the URL adheres to the following syntax:

```
https://<username>:<user_password>@<instance_URL>/api/now/cloud_event?sysparm_rest_integration_pool=true
```

</td></tr></tbody>
</table>    3.  Select **Create subscription**.

5.  Enable **AWS** event recording.

    1.  Navigate to **Config** &gt; **Settings**.

    2.  On the Settings page, select **Edit**.

    3.  Select the **Turn on** check box.

    4.  On the Start recording dialog box, select **Confirm**.

    5.  Fill the values on the Edit settings form.

        For a description of the form fields, see [Edit settings form reference](../reference/edit-aws-event-recording-settings-form-reference.md).

    6.  Select **Save**.


## What to do next

After some events are generated, navigate to the [Cloud User Portal](../../cloud-management-v2-user/task/cloudmgt-view-cloud-events.md) to view the events.

