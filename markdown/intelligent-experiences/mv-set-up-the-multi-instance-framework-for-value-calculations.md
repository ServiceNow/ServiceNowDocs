---
title: Set up Multi-Instance Framework for value calculations
description: Connect a sub-production instance to a production instance through the Multi-Instance Framework \(MIF\) so that the AI Control Tower can run value calculations across Creator skills.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/mv-set-up-the-multi-instance-framework-for-value-calculations.html
release: brazil
topic_type: task
last_updated: "2026-10-09"
reading_time_minutes: 1
breadcrumb: [Value, Configure, Measure AI system, Measure AI systems, AI Control Tower, Establishing AI governance, Enable AI Experiences]
---

# Set up Multi-Instance Framework for value calculations

Connect a sub-production instance to a production instance through the Multi-Instance Framework \(MIF\) so that the AI Control Tower can run value calculations across Creator skills.

## Before you begin

You must have access to both the sub-production and the production instances.

Role required: sn\_ai\_governance.ai\_steward

## About this task

Use the Multi-Instance Framework to register a sub-production instance under a production instance so that value calculations run against the correct managed instances.

## Procedure

1.  In the sub-production instance, navigate to the Manager Instances \[sn\_mif\_managed\_by\_instance\] table and create a record.

    |Field|Value|
    |-----|-----|
    |**Application**|AI Control Tower Core|
    |**Manager Instance**|Your production instance|

2.  Monitor the **Approval** field until it changes to **Auto-Approved**.

3.  In the production instance, open the **AI Control Tower** workspace.

4.  Go to **Configurations**.

5.  On the **Multi-instance setup** tab, complete the following substeps to add your sub-production instance.

    1.  Select **Add instances**.

    2.  Select your sub-production instance.

    3.  Select **Save**.


## Result

The sub-production instance is registered with the production instance. The AI Control Tower can run value calculations across the following data:

-   Creator metrics data for all creator skills
-   Results obtained from testing Value Templates for AI systems in the sub-production environment.

**Related topics**  


[Multi-Instance Framework for AI value data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/mv-multi-instance-framework-for-ai-value-data.md)

