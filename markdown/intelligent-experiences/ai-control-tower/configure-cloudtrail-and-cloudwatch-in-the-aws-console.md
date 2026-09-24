---
title: Configure CloudTrail and CloudWatch in the AWS Console
description: Configure CloudTrail to store execution logs of your bedrock agents activities and configure CloudWatch to monitor your trail logs and notify you when specific activity occurs.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/ai-control-tower/configure-cloudtrail-and-cloudwatch-in-the-aws-console.html
release: brazil
product: AI Control Tower
classification: ai-control-tower
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
keywords: [Now Assist, generative AI]
breadcrumb: [Configure AWS console, Hyperscaler connection with AWS, Using AI Control Tower to create hyperscaler connections, Using AI Control Tower \(legacy\), AI Control Tower \(legacy\), Establishing AI governance, Enable AI Experiences]
---

# Configure CloudTrail and CloudWatch in the AWS Console

Configure CloudTrail to store execution logs of your bedrock agents activities and configure CloudWatch to monitor your trail logs and notify you when specific activity occurs.

## Before you begin

Role required: AWS Admin

## Procedure

1.  Log in to [https://console.aws.amazon.com](https://console.aws.amazon.com)

2.  Select **CloudTrail** from the AWS Console home.

3.  Select **Trails** under section **Lake** on the left pane the AWS Console.

    The Choose trail attributes page is displayed to create a trail.

4.  Enter a display name for your trail in the **Trail name** field.

5.  To store the logs of the trail, you can select **Create new S3 bucket** or **Use existing S3 bucket**.

6.  Select **New** check box under customer managed by AWS KMS \(Key management system\) key and enter the AWS KMS alias.

    Verify the KMS key and newly created S3 bucket must be in the same region.

7.  To configure CloudWatch, ensure to select **Enabled** check box under the **CloudWatch Logs** section.

8.  Select the **New** check box and enter the **Log group name**.

9.  Select **Next**.

    The Choose log events page is displayed.

10. Select the **Data events** check box and clear the **Management events** check box under **Event type**.

11. Select **Add data event type**.

12. Select the **Resource type** and keep the **log selector template** as **log all events** for all the resource types.

    List of Resource types

    -   Bedrock session
    -   Bedrock async invoke
    -   Bedrock Invoke Inline-Agent
    -   Bedrock knowledge base
    -   Bedrock model
    -   Bedrock flow alias
    -   Bedrock agent alias
13. Select **Next**.

    The Review and create page get displayed. You can verify all the data event types.

14. Select **Create trail**.


## Result

The CloudTrail and CloudWatch are configured in the AWS Console. The CloudTrail is accessible from CloudWatch.

