---
title: Create inbound and outbound Amazon Connect contact flows
description: Create the inbound and outbound Amazon Connect contact flows to set up IVR \(Interactive Voice Response\).
locale: en-US
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Configure AWS account, Configuring Conversational IVR with Amazon Connect, Conversational IVR with Amazon Connect, Integrating Virtual Agent with Voice channels, Integrate VA with other channels, Virtual Agent, Conversational Interfaces]
---

# Create inbound and outbound Amazon Connect contact flows

Create the inbound and outbound Amazon Connect contact flows to set up IVR \(Interactive Voice Response\).

## Before you begin

Role required: admin

## Procedure

1.  Log in to your AWS account and select **Contact Flows**.

    1.  Select the region where the Lambda function/LexBot was created.

        For more information see, [Create an Amazon S3 bucket](create-amazon-s3-bucket.md).

        **Note:** Ensure that the region that you selected matches across the Amazon Connect setup.

    2.  In the Amazon Lex section, search and select your bot \(for example: SN\_CI\_CC\_LexBot\) in the **Bot** drop-down, select **SN\_CI\_CC\_LexBot\_Prod\_Alias** file from the **Alias** drop-down, and click **Add Amazon Lex Bot**.

    3.  In the AWS Lambda section, search for your Lambda function \(for example: SN\_CI\_CC\_Process\_Request\) from the drop-down and click **Add Lambda Function**.

    4.  Navigate to the Approved Origins section, click **Add Domain** to add your ServiceNow instance URL and click **Add Domain**.

        **Note:** Do not select the **Enable Contact flow logs** check box under the Contact flow logs section.

2.  Log in to your Amazon Connect Instance as an Administrator.

    1.  Hover over the **Routing** ![Routing icon.](../images/routing-icon.png) icon on the left navigation bar and select **Prompts**.

    2.  Click **Create new prompt**, upload a prompt file of your choice with `.wav` file extension, and click **Create**.

        **Note:** Ensure that the `.wav` audio file is no more than 10 seconds for optimal results.

    3.  Hover over the **Routing** ![Routing icon.](../images/routing-icon.png) icon on the left navigation bar and select **Contact flows**.

    4.  Click the drop-down next to Create contact flow button and select **Create customer queue flow**.

    5.  On the Contact flow form, click the drop-down next to the Save button and select **Import flow \(beta\)**.

    6.  On the Import flow \(beta\) pop-up screen, select a contact flow JSON file of your choice \(for example: SN\_CI\_CC\_Inbound\_Customer\_Queue\_Flow\) and click **Import**.

    7.  After the JSON is uploaded, locate and click the **Loop prompts** tile.

    8.  On the Loop prompts pop-up, select an audio file of your choice with the `.wav` extension \(for example: SN\_CI\_CC\_Inbound\_Prompt.wav\) from the Audio recording drop-down and click **Save**.

        **Note:** Ensure that the `.wav` audio file which you upload, does not exceed more than five-minutes duration.

    9.  Click **Save** to save the Contact flow and click **Publish** to publish the Contact flow.

    10. Navigate to **Routing** &gt; **Contact flows**, click **Create contact flow** and import the SN\_CI\_CC\_Inbound\_Contact\_Flow JSON file that you downloaded from the [KB article](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1430643).

    11. Locate and click the **Set customer queue flow** tile.

    12. In the Set customer queue flow pop-up, select the customer queue flow from the drop-down \(for example: SN\_CI\_CC\_Inbound\_Customer\_Queue\_Flow\) and click **Save**.

    13. Locate and click the **Invoke AWS Lambda function** tile.

    14. In the Invoke AWS Lambda function pop-up, select the SN\_CI\_CC\_Process\_Request lambda function file from the drop-down, that you have already added at Step 1, C, and click **Save**.

    15. Locate and click the **Get customer input** tile.

    16. In the Get customer input pop-up, navigate to the Lex bot section and select the SN\_CI\_CC\_LexBot file from the Name drop-down and SN\_CI\_CC\_LexBot\_Prod\_Alias file from the Alias drop-down and click **Save**.

    17. Click the **Play Prompt** tile next to the **Set Working Queue** tile.

    18. In the Audio prompt drop-down, select the `.wav` file of your choice and click **Save.**

    19. Click **Save** to save the Contact flow and click **Publish** to publish the Contact flow.

    20. Navigate to **Channels** &gt; **Phone numbers** and click **Claim a number**.

    21. On the Claim Phone number form, select either the **Toll free** Country or the **DID \(Direct Inward Dialing\)** Prefix and select the number.

    22. Provide a description of your choice in the **Description** field, select SN\_CI\_CC\_Inbound\_Contact\_Flow from the **Contact flow / IVR** drop-down, and click **Save**.

        You can edit the number description and also associate it with a new contact flow on the Manage Phone numbers page.

        After the number is published, customers can make a call and start conversations with the Virtual Agent.

    For more information about creating a Contact Flow, see [Amazon Contact flow documentation](https://docs.aws.amazon.com/connect/latest/adminguide/create-contact-flow.html).

    For more information about creating Prompts, see [Create prompts](https://docs.aws.amazon.com/connect/latest/adminguide/prompts.html) in Amazon Connect documentation.


## What to do next

Invoke an automated caller interaction with bots to fulfill the caller's request within the ServiceNow instance. For more information, see [Configure a contact flow for an automated caller interaction](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/establish-automated-bot-interactions.md).

**Parent Topic:**[Configuring your AWS account for use with Conversational IVR](../concept/configure-aws-account.md)

