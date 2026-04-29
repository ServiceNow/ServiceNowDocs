---
title: Components installed with Conversation Insights
description: Installation of the Conversation Insights application also installs the Conversation Insights \[sn\_aci\_insights\] table.
locale: en-US
release: australia
product: Conversational Intelligence
classification: conversational-intelligence
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Conversation Insights reference, Conversation Insights, Enable AI experiences]
---

# Components installed with Conversation Insights

Installation of the Conversation Insights application also installs the Conversation Insights \[sn\_aci\_insights\] table.

## Tables installed with Conversation Insights

The installation of Conversation Insights installs the Conversation Insights \[sn\_aci\_insights\] table. The data retention period for the Conversation Insights table is two years.

|Column|Description|
|------|-----------|
|Human Agent CSAT|Estimated Inferred customer satisfaction \(CSAT\) score based on the human agent's responses. The value range is 1–5 with 1 meaning that the user is extremely dissatisfied and 5 meaning that the user is extremely satisfied with the interaction.|
|Effort Score|A score of time and energy that the user had to put in during the interaction. The values are on a 3-point scale of low, medium, and high.|
|AI agent CSAT|Estimated CSAT score based on the AI agent's responses. The value range is 1–5 with 1 meaning that the user is extremely dissatisfied and 5 meaning that the user is extremely satisfied with the interaction.|
|Frustration|Estimated CSAT score that indicates whether the user expressed frustration during the interaction. The values are Yes or No.|
|Empathy|Estimated CSAT score that indicates empathy shown toward the user during the interaction. The values are on a 3-point scale of low, medium, and high.|
|Session CSAT|Estimated CSAT score calculated based on the overall session interactions of a user. The value range is 1–5 with 1 meaning that the user is extremely dissatisfied and 5 meaning that the user is extremely satisfied with the interaction.|
|Next Steps|Estimated CSAT score that indicates whether the agent recapped the outcome and provided clear instructions on what the user should do next. The values are on a 3-point scale of low, medium, and high.|
|CSAT processed|Boolean flag indicating whether CSAT data has been processed for the interaction record.|
|Transfer and Escalation|Estimated CSAT score that indicates whether the conversation was transferred or escalated to a human agent. The values are Yes or No.|
|Closed At|Timestamp showing when the conversation was closed.|
|Conversation|Refers to the associated conversation record in the Conversation \[sys\_cs\_conversation\] table.|
|Resolved|Estimated CSAT score that indicates whether the issue was resolved. The values are Yes or No.|
|Confusion|Estimated CSAT score that indicates whether the user expressed confusion or the agent didn’t understand the user's intent. The values are Yes or No.|

**Parent Topic:**[Conversation Insights reference](conversation-insights-reference.md)

