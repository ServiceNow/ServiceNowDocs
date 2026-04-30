---
title: Integrate Advanced Work Assignment AWA Voice routing
description: Provide customers the ability to use AWA as the routing engine for ServiceNow Voice on Amazon Connect.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Integrating with applications, ServiceNow Voice, Manage people and work capabilities, Extend ServiceNow AI Platform capabilities]
---

# Integrate Advanced Work Assignment AWA Voice routing

Provide customers the ability to use AWA as the routing engine for ServiceNow Voice on Amazon Connect.

## Before you begin

ServiceNow Voice for Amazon Connect offers two call routing options:

-   Amazon Connect native Voice routing
-   Advanced Work Assignment AWA Voice routing

When using the AWA Voice routing, calls are held in the Amazon Connect queue until the AWA queue settings determine their routing. This allows flexible call management using either the built-in Amazon Connect routing or the more advanced AWA routing capabilities.

Role required: sn\_cti\_amzn\_cct.admin

## Procedure

1.  Navigate to **Amazon Connect Integration** &gt; **View Instances**.

2.  Select the instance you want to configure.

3.  Click the **Setup Guide** related link.

4.  Go to the **Import Contact Flows** section of the setup guide.

5.  To enable Advanced Work Assignment \(AWA\) Voice routing, check the checkbox under the **AWA Voice Routing** heading.

    Complete the steps specified in the setup guide:

    1.  Complete [AWS Lambda](https://www.servicenow.com/docs/access?context=aws-lambda-spoke&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US) and OAuth credential setup.

    2.  Download the recommended hold music using the link in the setup guide \(you can choose your own hold music, but it cannot be longer than 5 seconds\).

    3.  See the [AWS documentation](https://docs.aws.amazon.com/connect/latest/adminguide/prompts.html#howto-prompts) to upload the hold music.

6.  Set up AWA queue to route Amazon Connect phone calls.

    To setup AWA, see [Get started with Advanced Work Assignment](https://www.servicenow.com/docs/access?context=implement-awa&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US).


## What to do next

For more information about integrating ServiceNow® Voice with Amazon Connect, see [Integrate ServiceNow Voice with Amazon Connect](../task/integrate-ccc-amazonconnect.md).

**Parent Topic:**[Integrating Voice with other applications](integrate-ccc-other-apps.md)

