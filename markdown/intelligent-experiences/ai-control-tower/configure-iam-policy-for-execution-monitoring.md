---
title: Configure an IAM policy for execution monitoring
description: Configuring IAM policy action permissions necessary for execution monitoring and integration user access on AWS to read Cloudwatch logs usage data.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/ai-control-tower/configure-iam-policy-for-execution-monitoring.html
release: brazil
product: AI Control Tower
classification: ai-control-tower
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
keywords: [Now Assist, generative AI]
breadcrumb: [Configure AWS console, Hyperscaler connection with AWS, Using AI Control Tower to create hyperscaler connections, Using AI Control Tower \(legacy\), AI Control Tower \(legacy\), Establishing AI governance, Enable AI Experiences]
---

# Configure an IAM policy for execution monitoring

Configuring IAM policy action permissions necessary for execution monitoring and integration user access on AWS to read Cloudwatch logs usage data.

## Before you begin

Role required: Admin

Cloud watch logs:

-   StartQuery
-   GetQueryResults

**Note:** To exclude specific resources from AI Control Tower, you can restrict them from the resources region. Select 'all' to include all CloudWatch logs data in AI Control Tower.

```
{ 

    "Version": "2012-10-17", 

    "Statement": [ 

        { 

            "Sid": "VisualEditor0", 

            "Effect": "Allow", 

            "Action": [ 

                "logs:GetQueryResults", 

                "logs:StartQuery" 

            ], 

            "Resource": "*" 

        } 

    ] 

}
```

For more information about creating an user in IAM and providing the required access, see [Understanding and Getting Your Security Credentials](https://docs.aws.amazon.com/general/latest/gr/aws-sec-cred-types.html) page on the [AWS Documentation](https://docs.aws.amazon.com/index.html) site.

## What to do next

Configure CloudTrail and CloudWatch in the AWS Console.

