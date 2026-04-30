---
title: Setting up Slack as a contact method
description: You configure Slack to enable users to receive Slack notifications for escalations. To offer Slack as a contact method for shift members, you install the IntegrationHub spoke for Slack.
locale: en-US
release: yokohama
product: On-Call Scheduling
classification: on-call-scheduling
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Configure, On-Call Scheduling, IT Service Management]
---

# Setting up Slack as a contact method

You configure Slack to enable users to receive Slack notifications for escalations. To offer Slack as a contact method for shift members, you install the IntegrationHub spoke for Slack.

## Configuring Slack for On-Call Scheduling

The Slack spoke automates On-Call Scheduling notifications and responds to them. The following configurations support On-Call Scheduling notifications:

## Outbound Configurations

-   **Slack &gt; Outbound Configurations &gt; On-Call: Assign by Acknowledgement**

    Generates a general escalation message. Modify the record to customize the message template.

    ![Outbound Assign by Acknowledgement subflow](../image/slack-outbound-assign-by-ack-oncall.png "Outbound Assign by Acknowledgement subflow")

-   **Slack &gt; Outbound Configurations &gt; On-Call: Assign by Acknowledgement Catch All**

    Generates a catch-all escalation message. Modify this record to customize the message template.


![Outbound Assign by Acknowledgement Catch All subflow](../image/slack-outbound-catch-all-oncall.png "Outbound Assign by Acknowledgement Catch All subflow")

## Inbound Decisions

-   **Slack &gt; Inbound Decisions &gt; On-Call: Assign by Acknowledgement Decision**

    Defines inbound configuration for general response handling for Accept or Reject escalation messages. Use **action\_id** as the key to map outbound configuration and inbound decisions for general escalations. The answer points to the subflow that is executed when the user clicks **Accept** or **Reject**. Modify the record to change the response handling behavior.

    ![Inbound Assign by Acknowledgement Decision subflow](../image/slack-decision-oncall.png "Inbound Assign by Acknowledgement Decision subflow")

-   **Slack &gt; Inbound Decisions &gt; On-Call: Assign by Acknowledgement Catch All Decision**

    Inbound configuration for catch-all response handling for escalation for Accept or Reject messages. Use **action\_id** as the key to map outbound configuration and inbound decisions for catch-all situations. The answer points to the subflow that is executed when the user clicks **Accept** or **Reject**. Modify the record to change response handling behavior.

    ![Assign by Acknowledgement Catch All Decision subflow](../image/slack-catch-all-decision-oncall.png "Assign by Acknowledgement Catch All Decision subflow")


## Subflows

![Subflow designer](../image/slack-subflows-tab.png "Subflow designer")

-   **On-Call Assign by Acknowledgement**

    This subflow handles incoming responses from Slack and then acts. For example, assign a task to a user and return an acknowledgement message. In case of rejection, the subflow logs the response and moves the escalation to the next escalatee.

-   **Insert Slack Response**

    This action creates a record in the \[sn\_slack\_ah\_v2\_inbound\] table for incoming Slack responses. You can reference the response by workflow based on **context\_id**.

-   **On-Call Response Controller**

    This action performs appropriate operations when the user clicks **Accept** or **Reject** from Slack. It invokes the utility methods to perform actions from the OnCallSlackUtils script include.


**Parent Topic:**[Configuring On-Call Scheduling](../../user-administration/concept/configuration.md)

