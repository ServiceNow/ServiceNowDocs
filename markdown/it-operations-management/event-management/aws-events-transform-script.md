---
title: Integrate AWS platform as a data source
description: Integrate Amazon Web Services \(AWS\) with Event Management. To add AWS platform as a data source, configuration is required in the AWS platform.
locale: en-US
release: zurich
product: Event Management
classification: event-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Integrate with push connectors, Configure a push connector, Configure Event Management connectors, Event Management Integrations, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Integrate AWS platform as a data source

Integrate Amazon Web Services \(AWS\) with Event Management. To add AWS platform as a data source, configuration is required in the AWS platform.

## Before you begin

Ensure that the Event Management Connectors \(sn\_em\_connector\) plugin is installed on the ServiceNow AI Platform instance.

Download the Event Management Connectors plugin from the ServiceNow Store.

Role required: evt\_mgmt\_admin

## About this task

When an AWS platform alarm arrives, Event Management:

-   Extracts information from the original AWS platform alarm to populate the required event fields and inserts the event into the database.
-   Captures the content in the **additional\_info** field.

The AWS platform push connector is located in **Event Management** &gt; **Integrations** &gt; **Push Connectors**. In the Push Connectors page, click **AWS Events Push Connector**.

**Note:** The AWS push connector that is provided in the base system handles AWS CloudWatch alarms only and not CloudWatch events created through event rules. To handle Simple Notification Service \(SNS\) alarms that are other than AWS CloudWatch, create a new push connector or customize the AWS push connector.

Starting from the Xanadu release, the OOTB \(Out-Of-The-Box\) event rules provided with the connector, which you have not previously used \(i.e., neither activated, deactivated, nor modified\), will now have the **Apply additional matching rules** check box set to true. Previously, this check box was disabled. This change allows you to execute more event rules or automation using the same filter conditions for the events.

**Note:** This feature applies only to active event rules.

## Procedure

1.  In the AWS platform console, select **Simple Notification Service** .

    If an SNS topic does not exist, create one.

2.  Under the SNS topic, create a new subscription.

    1.  Take **Topic ARN** from the topic that you created.

        The Amazon Resource Name \(ARN\) is necessary for binding an Event Management alert to a CI.

    2.  Set **Protocol** to: **https**.

    3.  In the ServiceNow instance, create a user account or identify an existing ServiceNow user for this integration.

        Also ensure the relevant ServiceNow sys\_user is assigned the evt\_mgmt\_integration role. To ensure proper authentication, use the least privileged user with the evt\_mgmt\_integration role, rather than a high privileged user.

    4.  Set **Endpoint** to: `https://<username>:<password>@<instance-name>.service-now.com/api/sn_em_connector/em/inbound_event?source=aws`

    If AWS platform multi-factor authentication \(MFA\) is enabled, when signing in to the AWS platform website, you're prompted for the user name and password, as well as an authentication code from the AWS platform MFA device of the user.

3.  Wait until the subscription changes from `Pending` to `Confirmed` and the subscription ARN is populated.

    This can take a few minutes.

4.  Create alarms in AWS platform to send to Event Management and link the alarms to the SNS topic that you created.

    Raw message delivery must not be enabled in AWS alarm. These following event rules are provided with the base system:

<table id="table_zmk_1xv_tz"><thead><tr><th>

Event rule

</th><th>

Description

</th></tr></thead><tbody><tr><td>

AWS host binding

</td><td>

Bind AWS platform alarms, on either the host or virtual machine \(VM\), to the host Hardware CI.

</td></tr><tr><td>

AWS - General

</td><td>

Bind AWS platform alarms on the Load Balancer \(LB\) to the Cloud Load Balancer CI, Amazon Relational Database Service \(RDS\) to the Cloud Database CI, and Host or Virtual Machine \(VM\) to the Virtual Machine Instance CI.**Note:** To bind events from the Host or Virtual Machine to the Virtual Machine Instance CI, disable the AWS host binding rule.

</td></tr></tbody>
</table>    **Note:** For the push connector to handle the incoming event, you must sent a request header **x-amz-sns-message-type** with value **Notification**.

    This example shows a JSON string for AWS VM binding:

    ```
    {
    "Type" : "<type>",
    "MessageId" : "<message ID #>",
    "TopicArn" : "<topic arn>",
    "Subject" : "ALARM: \"<alarm type>\" in <location>",
    "Message" : "{\"AlarmName\":\"<alarm name>\",\"AlarmDescription\":<alarm description>,\"AWSAccountId\":\"<account ID #>\",\"NewStateValue\":\"ALARM\",\"NewStateReason\":\"Threshold Crossed: <threshold and datapoint which it crossed>.\",\"StateChangeTime\":\"<date and time>\",\"Region\":\"<location>\",\"OldStateValue\":\"OK\",\"Trigger\":{\"MetricName\":\"CPUUtilization\",\"Namespace\":\"<namespace>\",\"Statistic\":\"<statistic name>\",\"Unit\":null,\"Dimensions\":[{\"name\":\"InstanceId\",\"value\":\"<dimension value>\"}],\"Period\":<period number>,\"EvaluationPeriods\":<number of evaluation periods>,\"ComparisonOperator\":\"GreaterThanOrEqualToThreshold\",\"Threshold\":<threshold number>}}",
    "Timestamp" : "<date and time>",
    "SignatureVersion" : "<version number>",
    "Signature" : "<signature>",
    "SigningCertURL" : "<URL>",
    "UnsubscribeURL" : "<URL>"
    }
    ```

5.  To enable multiple member accounts to forward CloudWatch or EventBridge events to a centralized account, where a single SNS topic delivers them to the ServiceNow Event Ingestion endpoint, you need to make configuration on AWS side.

    To configure it, see [https://repost.aws/knowledge-center/cloudwatch-cross-account-sns](https://repost.aws/knowledge-center/cloudwatch-cross-account-sns). This design simplifies integration, avoids duplicating SNS topics across accounts, and provides a single entry point for all monitoring events flowing into ServiceNow.


-   **[Integrate AWS with REST API key token](integrate-aws-api-key.md)**  
Integrate using an API key to establish secure communication and automate data exchange via REST API. This simplifies integration, enabling seamless access to services and enhancing operational efficiency.

**Parent Topic:**[Integrate with push connectors](configure-listener-transform-script.md)

**Related topics**  


[Event field format for event collection](../concept/c_EMIntegrateRequirementEvent.md)

[Integrate with push connectors](configure-listener-transform-script.md)

