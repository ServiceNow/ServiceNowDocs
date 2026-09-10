---
title: Configure AWS Config event notifications
description: Configure the Amazon Web Services \(AWS\) Config service to send event notifications to the ServiceNow instance for any changes in the lifecycle state of a resource.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/discovery/aws-config-service-cloud-mgt.html
release: australia
product: Discovery
classification: discovery
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 6
breadcrumb: [AWS events-driven discovery, Discovery for AWS, Discovery for cloud environment, Discovery, ITOM Visibility, IT Operations Management]
---

# Configure AWS Config event notifications

Configure the Amazon Web Services \(AWS\) Config service to send event notifications to the ServiceNow instance for any changes in the lifecycle state of a resource.

## Before you begin

-   Ensure that the Discovery \(com.snc.discovery\) plugin is installed and activated in the instance.
-   Ensure that you have valid AWS subscriptions \(service accounts\) and its associated logical datacenters are discovered.
-   Ensure that the user account password used to subscribe the instance to the Simple Notification Service \(SNS\) does not contain the @ or \# characters.
-   Ensure that the AWS Config recorder is properly configured with continuous recording enabled to prevent events from being nested with a "detail" JSON node.

Roles required:

-   Ensure that an AWS role is available that can access the following services and resources:
    -   SNS
    -   AWS Config service
    -   Resource types for which you want to track the configuration change
-   ServiceNow roles:
    -   discovery\_admin
    -   sn\_cmp.cloud\_event\_integration: The access credentials of a ServiceNow user with the sn\_cmp.cloud\_event\_integration role is required to subscribe the instance to the SNS notifications. For more information, see [Create a user](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/t_CreateAUser.md) and [Assign a role to a user](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/t_AssignARoleToAUser.md).

## About this task

ServiceNow® event-driven discovery uses the events to update the latest resource information in the Configuration Management Database \(CMDB\). For more information, see [AWS events-driven discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery/aws-events-driven-discovery.md).

Many of the steps in the topic are performed in the AWS portal. For more information, see the following AWS documents:

-   [Set Up Amazon SNS Notifications](https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/US_SetupSNS.html)
-   [Viewing the AWS Config dashboard](https://docs.aws.amazon.com/config/latest/developerguide/viewing-the-aws-config-dashboard.html)

**Note:**

If you're using domain separation for Cloud Discovery, the events are also domain-separated. Therefore, you can view the details of a processed event only if it belongs to your domain. If an event isn’t associated with any service account, then it’s associated with the global domain.

During event processing, the Cloud Event Scheduler identifies the domain of the service account and assigns to the event. If an error occurs in identifying the domain before processing, the event can sometimes stay unassigned and become visible to all domains. To restrict failed event visibility, set the **sn\_cmp.error\_events.default\_domain** property to the sys\_id of the service-provider domain. Failed events then appear only to the service-provider domain administrator.

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

**Important:** Do not select FIFO. FIFO topics only support the SQS subscription protocol. Standard is required because the ServiceNow subscription uses HTTPS.

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

        For more information, see [Creating an Amazon SNS topic](https://docs.aws.amazon.com/sns/latest/dg/sns-create-topic.html).

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

        For more information, see [Subscribing to an Amazon SNS topic](https://docs.aws.amazon.com/sns/latest/dg/sns-create-subscribe-endpoint-to-topic.html).

5.  Configure AWS Config data and delivery channel settings.

    1.  Navigate to **AWS Config** &gt; **Settings**.

    2.  In the Data and delivery section, select **Edit**.

    3.  On the Edit data and delivery channel settings form, fill in the fields.

<table id="table_data_delivery"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Data retention period

</td><td>

Length of time to retain AWS Config data.Select **Retain AWS Config data for 7 years** or set a custom retention period.

</td></tr><tr><td>

Amazon S3 bucket

</td><td>

S3 bucket for storing configuration history and snapshots.Select one of the following options:

-   **Create a bucket**
-   **Choose a bucket from your account**
-   **Choose a bucket from another account**


</td></tr><tr><td>

Amazon SNS topic

</td><td>

SNS topic for streaming configuration changes and notifications.Select the **Stream configuration changes and notifications to an Amazon SNS topic** check box.

Select **Choose a topic from your account** and select the SNS topic created in [3](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery/aws-config-service-cloud-mgt.md).

</td></tr></tbody>
</table>    4.  Select **Save**.

        For more information, see [Updating the delivery channel](https://docs.aws.amazon.com/config/latest/developerguide/update-dc-console.html).

6.  Configure AWS Config recorder settings.

    1.  On the Settings page, in the Recorder section, select **Edit**.

    2.  On the Edit customer managed recorder settings form, fill in the fields.

<table id="table_recorder"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Enable recording

</td><td>

Turns the recorder on or off.Select the **Enable recording** check box.

</td></tr><tr><td>

Recording strategy

</td><td>

Determines which resource types to record.Select one of the following options:

-   **All resource types with customizable overrides**: Records all current and future supported resource types in the Region. You can override the recording frequency for specific resource types or exclude specific resource types entirely.
-   **Specific resource types**: Records only the resource types you specify.


</td></tr><tr><td>

Recording frequency

</td><td>

How often to record configuration changes.Select one of the following options:

-   **Continuous recording**: Records configuration changes whenever a change occurs. **This option is required for proper event processing in ServiceNow.**
-   **Daily recording**: Records configuration data once per day if a change occurred.


</td></tr><tr><td>

Override settings

</td><td>

Optional overrides for specific resource types.You can override the recording frequency for specific resource types or exclude specific resource types from recording. You can add up to 100 frequency overrides and 596 exclusions.

</td></tr><tr><td>

IAM role for AWS Config

</td><td>

IAM role that AWS Config uses to access other AWS services.Select one of the following options:

-   **Use an existing AWS Config service-linked role**: Uses a predefined role that includes the permissions AWS Config requires.
-   **Choose a role from your account**: Uses a pre-existing IAM role from your account.


</td></tr></tbody>
</table>    3.  Select **Save**.

        For more information, see [Managing the configuration recorder](https://docs.aws.amazon.com/config/latest/developerguide/stop-start-recorder.html).

    **Warning:**

    Ensure that the recorder settings are configured correctly with continuous recording enabled. If the AWS Config recorder is not properly configured, AWS Config events may be nested with a "detail" JSON node, which prevents ServiceNow from processing the events.


**Symptom:** Events from AWS Config are not being inserted into the ServiceNow instance.

**Cause:** The AWS Config recorder is not properly configured. Without correct recorder settings, event information from AWS is nested with a "detail" JSON node, and the ServiceNow event processing logic cannot detect the events.

**Resolution:** Verify the recorder settings on the AWS Config Settings page. Ensure that:

-   The **Enable recording** check box is selected.
-   The recording frequency is set to **Continuous recording**.
-   The SNS topic is correctly configured in the data and delivery channel settings.

## What to do next

After some events are generated, navigate to the [Cloud User Portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/cloud-configuration-governance/cloudmgt-view-cloud-events.md) to view the events.

