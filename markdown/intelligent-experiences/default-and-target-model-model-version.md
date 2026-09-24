---
title: Default and target model version
description: Model version is the large language model version a skill uses to route requests to process users' queries. Default model version is where all the requests route to by default. This is pre-set by ServiceNow. A target model version is chosen to route your requests to a different version at run-time, rather than using the default version.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/default-and-target-model-model-version.html
release: brazil
topic_type: reference
last_updated: "2026-09-16"
reading_time_minutes: 1
breadcrumb: [Now Assist reference, AI Admin Hub, Generative AI skills, Enable AI Experiences]
---

# Default and target model version

Model version is the large language model version a skill uses to route requests to process users' queries. Default model version is where all the requests route to by default. This is pre-set by ServiceNow®. A target model version is chosen to route your requests to a different version at run-time, rather than using the default version.

## Updating the target model version at the instance level

**Note:**

-   Model versions in the following states aren't available for selection: deprecated, retired, in review, rejected.
-   Confirm that the model name you enter exactly matches the name configured in your external provider's console. A mismatch may cause the provider configuration to fail.
-   Confirm that network access to the provider endpoint is allowed by your instance's proxy or firewall rules.

A default mapping of default and target model version is pre-configured. If you update the target model version for a selected default model version, all the associated skills with this version mapping at the current instance level, get impacted.

\[Omitted image "version-management-instance-ref.png"\] Alt text: Updating target model version at the instance level

## Updating the target model version at the skill level

If you update the target model version for a selected default model version at the skill level, the mapping is updated for that skill only. Customizing the model version for skills overrides the instance-level model version currently assigned to each provider. This action is typically reserved for specific situations.

**Parent Topic:**[Now Assist reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/now-assist-reference-landing.md)

