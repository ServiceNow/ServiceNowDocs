---
title: Discovering assets through Connectors
description: Connectors integrate AI Control Tower with external platforms so that AI assets created and managed outside ServiceNow are automatically discoverable.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/discovering-connectors.html
release: zurich
topic_type: concept
last_updated: "2026-07-29"
reading_time_minutes: 2
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Discover and manage AI assets, AI Control Tower, Enable AI experiences]
---

# Discovering assets through Connectors

Connectors integrate AI Control Tower with external platforms so that AI assets created and managed outside ServiceNow are automatically discoverable.

## How connectors discover AI assets

When you create an AI connection using a connector, AI Control Tower performs the following:

-   Authenticates with the external platform using the credentials you provide — typically an access key, service account, or OAuth token depending on the platform.
-   Discovers AI assets on the external platform, such as deployed models, agents, knowledge bases, and pipelines.
-   Imports the discovered assets into the AI asset inventory in AI Control Tower, where they can be governed, evaluated, and managed alongside natively created assets.
-   Keeps the inventory updated by re-running discovery on a scheduled import job, so new or changed assets on the external platform are reflected in AI Control Tower.

## Key Benefits

-   Eliminate Blind Spots: Aggregate fragmented AI assets for holistic visibility and control.
-   Accelerate Governance: Centralize compliance, security, and operational efficiency.
-   Drive Innovation: Enable responsible, scalable, and auditable AI ecosystems where governance and innovation coexist.

## Why AI connections

-   Fragmented AI ecosystems create governance and compliance risks.
-   Enterprises need real-time visibility into AI usage, including shadow AI to ensure security, compliance, and operational efficiency.
-   AI discovery empowers organizations to accelerate innovation while reducing risk.

## AI connection Challenges &amp; Solution

-   Enterprise AI adoption is growing rapidly, yet many organizations face challenges with fragmented visibility across internal developments, vendor offerings, and cloud deployments.
-   The AI connection in AI Control Tower automatically detects AI assets on the ServiceNow AI Platform, AWS Bedrock, Azure Machine Learning Services, and Azure Cognitive Services.
-   It also detects assets on Copilot Studio and GCP Vertex AI, then adds them to the ServiceNow Configuration Management Database for unified governance.
-   This capability helps organizations achieve comprehensive visibility of their AI assets while supporting the expansion of initiatives across hybrid cloud environments.

## Business impact of AI connections

-   **Complete AI visibility** — Discover and track all externally deployed AI assets across platforms such as Amazon, Google, and Microsoft in a single inventory.
-   **Consistent governance** — External assets are subject to the same evaluation rules, lifecycle states, and policy controls as natively created assets.
-   **Reduced manual effort** — Scheduled import jobs keep the inventory current automatically, removing the need for manual tracking.
-   **Audit and compliance readiness** — All discovered assets are tracked in a system of record with evaluation history, supporting regulatory and audit requirements.
-   **Scalable oversight** — A single AI connection can discover assets across hundreds of accounts or environments, so governance scales with AI adoption without increasing team workload.
-   **Usage-informed decisions** — Connectors that pull usage data alongside asset metadata help governance teams identify high-usage, dormant, or high-risk assets and prioritize accordingly.

