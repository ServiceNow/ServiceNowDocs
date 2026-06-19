---
title: Sentiment page in Assistant analytics
description: Analyze user sentiment through customer satisfaction \(inferred CSAT\) score and CSAT factors such as empathy, frustration and confusion, transfers and escalations from conversations with assistants to improve the quality of user interactions.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/conversational-interfaces/now-assist-in-virtual-agent/sentiment-page-in-assistant-analytics.html
release: zurich
product: Now Assist in Virtual Agent
classification: now-assist-in-virtual-agent
topic_type: concept
last_updated: "2025-10-27"
reading_time_minutes: 4
breadcrumb: [Analyzing assistants, Now Assist in Virtual Agent, Conversational Interfaces]
---

# Sentiment page in Assistant analytics

Analyze user sentiment through customer satisfaction \(inferred CSAT\) score and CSAT factors such as empathy, frustration and confusion, transfers and escalations from conversations with assistants to improve the quality of user interactions.

The Sentiment dashboard page aggregates metrics related to user satisfaction, emotional feedback, empathy levels, and conversation outcomes. These metrics enable you to monitor inferred CSAT, track transfers and escalations, analyze empathy distribution, and review negative emotion trends. The insights from these metrics support targeted improvements to assistant behavior, response quality, and overall user experience.

\[Omitted image "NAinVA-assistant-designer-analytics-sentiment.png"\] Alt text: Sentiment dashboard page in Assistant analytics.

The visualizations on the Sentiment page help you with the following.

-   Monitor user satisfaction and sentiment trends to identify strengths and areas for improvement in assistant interactions.
-   Track emotional feedback and empathy levels, enabling you to address frustration, confusion, and other negative emotions.
-   Analyze conversation outcomes and recommended next steps to guide assistant optimization and enhance resolution rates.

-   **Overall Sentiment**

    This area of the dashboard shows the overall average inferred CSAT score for analyzed conversations in the selected date range. The CSAT score is measured on a scale from 0 to 5, where 0 represents the lowest satisfaction and 5 represents the highest. Use this metric to track changes in sentiment over time and evaluate the impact of assistant updates.

    \[Omitted image "NAinVA-assistant-designer-analytics-sentiment-overall.png"\] Alt text: Overall Sentiment.

-   **Conversations Analyzed**

    This area of the dashboard shows the total number of conversations analyzed for sentiment in the selected date range. This number indicates the breadth of data supporting CSAT scores.

    \[Omitted image "NAinVA-assistant-designer-analytics-sentiment-conv-analyze.png"\] Alt text: Conversations Analyzed.

-   **High Empathy Rate**

    This area of the dashboard shows the percentage of conversations where high empathy was detected in assistant responses. It's calculated as \(\(Number of conversations with high empathy\)/\(Total number of conversations analyzed\)\) x 100. High empathy rate is an indication of the assistant's ability to respond with empathy to users queries.

    \[Omitted image "NAinVA-assistant-designer-analytics-sentiment-high-empathy.png"\] Alt text: High Empathy Rate.

-   **Conversations with Negative Emotions**

    This area of the dashboard shows the percentage of conversations where negative emotional feedback in terms of confusion or frustration was detected. It's calculated as \(\(Number of conversations with Frustration or Confusion\)/\(Total number of conversations analyzed\)\) x 100. This metric highlights the prevalence of negative experiences in assistant interactions. Use the metric to monitor and reduce negative emotion rates through targeted assistant improvements.

    \[Omitted image "NAinVA-assistant-designer-analytics-sentiment-conv-neg-emotions.png"\] Alt text: Conversations with Negative Emotions.

-   **Average Inferred CSAT Over Time**

    This area of the dashboard shows daily average of inferred CSAT scores in the selected data range. The CSAT scores are measured on a scale from 0 to 5, where 0 represents the lowest satisfaction and 5 represents the highest. This chart highlights periods of improvement or decline in user sentiment.

    \[Omitted image "NAinVA-assistant-designer-analytics-sentiment-avg-csat.png"\] Alt text: Average Inferred CSAT Over Time.

-   **Transfers and Escalations Over Time**

    This area of the dashboard tracks the number of conversations transferred or escalated to live agent. Hover over the trend line to view the number of conversations transferred or escalated to live agent on a given day. This chart helps you with how often assistants require human intervention.

    \[Omitted image "NAinVA-assistant-designer-analytics-sentiment-transfer-time.png"\] Alt text: Transfers and Escalations Over Time.

-   **Average Inferred CSAT \(Virtual Agent\)**

    This area of the dashboard shows the average Inferred CSAT score for Virtual Agent interactions in the selected period. For conversations involving both Virtual Agent and live agent, this score reflects only the Virtual Agent CSAT. Scored on a 5-point scale, 0 = least satisfied and 5 = most satisfied. Use this metric to benchmark assistant performance and prioritize improvements where satisfaction is lowest.

    \[Omitted image "NAinVA-assistant-designer-analytics-sentiment-avg-csat-virtual-agent.png"\] Alt text: Average Inferred CSAT \(Virtual Agent\).

-   **Average Inferred CSAT \(Live Agent\)**

    This area of the dashboard shows the average Inferred CSAT score for live agent interactions in the selected period. For conversations involving both Virtual Agent and live agent, this score reflects only the live agent CSAT. Scored on a 5-point scale, 0 = least satisfied and 5 = most satisfied. Use this metric to benchmark assistant performance and prioritize improvements where satisfaction is lowest.

    \[Omitted image "NAinVA-assistant-designer-analytics-sentiment-avg-csat-live-agent.png"\] Alt text: Average Inferred CSAT \(Live Agent\).

-   **Average Inferred CSAT \(Session\)**

    This area of the dashboard shows the average Inferred CSAT score for all interactions handled by Virtual Agent or a combination of Virtual Agent and live agent in the selected period. Scored on a 5-point scale, 0 = least satisfied and 5 = most satisfied.

    \[Omitted image "NAinVA-assistant-designer-analytics-sentiment-avg-csat-session.png"\] Alt text: Average Inferred CSAT \(Session\).

-   **Assistant Recommended Next Steps**

    This area of the dashboard shows how clearly the assistant explained what happens next or what the user should do. Low: Conversations where no clear guidance was provided. Medium: Conversations where some guidance was provided. High: Conversations where clear and complete guidance was provided.

    \[Omitted image "NAinVA-assistant-designer-analytics-sentiment-assistant-steps.png"\] Alt text: Assistant Recommended Next Steps.

-   **Conversation Insight Inferred Resolution State**

    This area of the dashboard shows the conversations where the user's issue was resolved. Yes: conversations where the assistant met the user's needs. No: conversations where the assistant didn't meet the user's needs. Unknown: conversations where the resolution state couldn’t be determined.

    \[Omitted image "NAinVA-assistant-designer-analytics-sentiment-conv-state.png"\] Alt text: Conversation Insight Inferred Resolution State.

-   **Empathy Levels Distribution Over Time**

    This area of the dashboard shows the distribution of empathy levels \(High, Medium, Low\) in assistant responses in the selected date range. Use this chart to assess the emotional intelligence of assistant interactions and target improvements.

    \[Omitted image "NAinVA-assistant-designer-analytics-sentiment-empathy-levels.png"\] Alt text: Empathy Levels Distribution Over Time.

-   **Negative Emotion Feedback Over Time**

    This area of the dashboard tracks the feedback related to negative emotions: frustration and confusion in conversations with assistants. This chart helps you identify trends in negative user experiences and take necessary steps to reduce the negative feedback.

    \[Omitted image "NAinVA-assistant-designer-analytics-sentiment-negative-emotion.png"\] Alt text: Negative Emotion Feedback Over Time.


