---
title: Configure an IAM for Agent discovery
description: Configuring IAM policy action permissions necessary for Agent discovery and integration user access on AWS to read bedrock agentic data.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/ai-control-tower/configure-iam-for-agent-discovery.html
release: brazil
product: AI Control Tower
classification: ai-control-tower
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
keywords: [Now Assist, generative AI]
breadcrumb: [Configure AWS console, Hyperscaler connection with AWS, Using AI Control Tower to create hyperscaler connections, Using AI Control Tower \(legacy\), AI Control Tower \(legacy\), Establishing AI governance, Enable AI Experiences]
---

# Configure an IAM for Agent discovery

Configuring IAM policy action permissions necessary for Agent discovery and integration user access on AWS to read bedrock agentic data.

## Before you begin

Role required: Admin

AWS provides the minimum given policies by default:

-   AmazonBedrockReadOnly
-   CloudWatchReadOnlyAccess

The minimum policy action permissions needed for the integration user on AWS to read bedrock agentic data:

-   ListAgents
-   GetAgent
-   ListAgentActionsGroups
-   ListAgentVersions
-   GetInferenceProfile
-   GetFoundationModel
-   ListAgentCollaborators
-   GetAgentAlias

**Note:**

To exclude specific resources from AI Control Tower, you can restrict them from the resources region. Select 'all' to include all AWS bedrock agentic resources data into AI Control Tower.

```
{ 

    "Version": "2012-10-17", 

    "Statement": [ 

        { 

            "Sid": "VisualEditor0", 

            "Effect": "Allow", 

            "Action": [ 

                "bedrock:ListAgents", 

                "bedrock:ListAgentVersions", 

                "bedrock:ListAgentCollaborators", 

                "bedrock:ListAgentActionGroups", 

                "bedrock:GetInferenceProfile", 

                "bedrock:GetFoundationModel", 

                "bedrock:GetAgent" 

            ], 

            "Resource": "*" 

        } 

    ] 

} 
```

## What to do next

Configure an IAM policy for Execution monitoring.

