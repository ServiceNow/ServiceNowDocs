---
title: Multi-Instance Framework for AI value data
description: The Multi-Instance Framework \(MIF\) synchronizes AI value data from a sub-production instance to a production instance only for Creator skills. In this setup, the AI Control Tower calculates value for Creator skills using data from development and testing environments.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/mv-multi-instance-framework-for-ai-value-data.html
release: brazil
topic_type: concept
last_updated: "2026-09-25"
reading_time_minutes: 1
keywords: [multi-instance framework, MIF, AI value, sub-production instance]
breadcrumb: [Value, Explore, Measure AI system, Measure AI systems, AI Control Tower, Establishing AI governance, Enable AI Experiences]
---

# Multi-Instance Framework for AI value data

The Multi-Instance Framework \(MIF\) synchronizes AI value data from a sub-production instance to a production instance only for Creator skills. In this setup, the AI Control Tower calculates value for Creator skills using data from development and testing environments.

For creator skills deployed in a sub-production instance, you can evaluate how the value is determined for an AI system by running a metric within its value template. The results are synced to the production instance for the value calculation.

To facilitate this process, MIF connects the sub-production instance to the production instance, which functions as the manager instance. MIF then synchronizes value data for Creator skills to the production instance.

**Note:**

MIF supports value calculation on sub-production instances only for Creator skills. Value calculation on sub-production instances isn't available for any other skills.

## Value data that MIF syncs

MIF syncs the following value data from the sub-production instance to the production instance:

-   Creator metrics data for all creator skills
-   Results from testing value templates for AI systems in the sub-production environment

**Related topics**  


[Set up Multi-Instance Framework for value calculations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/mv-set-up-the-multi-instance-framework-for-value-calculations.md)

