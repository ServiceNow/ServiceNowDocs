---
title: Discrepancies when using different AI search tools
description: Different AI search tools may return different answers for the same or similar searches. This difference in results is expected. It occurs because each large language model \(LLM\) uses a different approach to find results and generate answers that match your search.
locale: en-US
release: australia
product: ServiceNow Large Language Model \(Now LLM\)
classification: servicenow-large-language-model-now-llm
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Large language models on the ServiceNow AI Platform, Enable AI experiences]
---

# Discrepancies when using different AI search tools

Different AI search tools may return different answers for the same or similar searches. This difference in results is expected. It occurs because each large language model \(LLM\) uses a different approach to find results and generate answers that match your search.

## Overview of how LLMs create responses

Large Language Models don’t retrieve answers from a single source. Instead, they generate responses by predicting the next most likely word, one at a time, based on patterns they’ve learned from the data they were trained on.

Because of that, several factors can make the answers vary each time. The factors include:

-   Probability
-   Multiple good answers
-   Context sensitivity
-   LLM variation

Answer generation involves probability, context, and variation. Therefore, responses to the same question can differ slightly each time it is asked, and from provider to provider.

For more information on differences in ServiceNow AI results, see Search result disparities between AI Search and Now Assist search features.

## Now LLM Service response vs. Azure response

![image.nowllm-vs-azure]

**Parent Topic:**[Large language models on the ServiceNow AI Platform](exploring-large-language-models.md)

