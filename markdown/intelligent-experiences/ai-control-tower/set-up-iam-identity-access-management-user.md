---
title: Configure IAM user
description: Configuring the IAM user in the AWS console.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/ai-control-tower/set-up-iam-identity-access-management-user.html
release: brazil
product: AI Control Tower
classification: ai-control-tower
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
keywords: [Now Assist, generative AI]
breadcrumb: [Configure AWS console, Hyperscaler connection with AWS, Using AI Control Tower to create hyperscaler connections, Using AI Control Tower \(legacy\), AI Control Tower \(legacy\), Establishing AI governance, Enable AI Experiences]
---

# Configure IAM user

Configuring the IAM user in the AWS console.

## Before you begin

Role required: AWS Admin

## Procedure

1.  Log in to [https://console.aws.amazon.com](https://console.aws.amazon.com/)

2.  Navigate to **IAM**&gt;**Access management**&gt;**Users**.

3.  Select **Create user** and configure the user with the policies mentioned in the following section.

    The IAM user is created.

4.  Open the user and create an access key for a third party service.

5.  Copy the **Access key ID** \(AWS Specific\) and the **Secret access key** \(AWS Specific\) to a text file.

    You can only show the secret access key once, but you can delete and create keys when necessary.


## What to do next

The IAM user must configure policies for Agent discovery and Execution monitoring.

1.  [Configure an IAM for Agent discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/ai-control-tower/configure-iam-for-agent-discovery.md)
2.  [Configure an IAM policy for execution monitoring](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/ai-control-tower/configure-iam-policy-for-execution-monitoring.md)

