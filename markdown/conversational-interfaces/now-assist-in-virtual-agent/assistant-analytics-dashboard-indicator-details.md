---
title: Assistant analytics dashboard indicator details
description: View the data and calculations behind an indicator that is presented in the form of a visualization on the Assistant analytics dashboard.
locale: en-US
release: australia
product: Now Assist in Virtual Agent
classification: now-assist-in-virtual-agent
topic_type: concept
last_updated: "2025-12-10"
reading_time_minutes: 12
breadcrumb: [Now Assist in Virtual Agent reference, Now Assist in Virtual Agent, Conversational Interfaces]
---

# Assistant analytics dashboard indicator details

View the data and calculations behind an indicator that is presented in the form of a visualization on the Assistant analytics dashboard.

Assistant analytics indicators contain the following details: indicator type, data source, calculation, available breakdowns, unit, and precision.

These indicators collect data at a daily frequency. Data is only available for dates before the current date. If you want to see results from the current day, you must wait until the next day.

## Overview page indicator details

|Visualization|Indicator name|Indicator type|Indicator source table|Calculation|Available breakdowns|Data collection frequency|Unit|Precision|
|-------------|--------------|--------------|----------------------|-----------|--------------------|-------------------------|----|---------|
|Cumulative AI-assisted actions|AI-Assisted Actions in Conversations|Automated|Gen AI Log Metadata\[sys\_gen\_ai\_log\_metadata\]|Count of Gen AI log actions|By Conversation Channels, Assistant|Daily|\#|0|
|Average Distinct Users|Daily Conversation Consumers|Automated|Conversation\[sys\_cs\_conversation\]|Count of unique users|By Assistant, Context Profiles, Conversation Channels, Conversation State|Daily|\#|0|
|Assist Usage Volume|Conversation Assist Usage Volume|Automated|Gen AI Log Metadata\[sys\_gen\_ai\_log\_metadata\]|Daily count of Gen AI log assists|By Generative AI Feature, Conversation Channels, Assistant|Daily|\#|0|
|Overall Average Conversation CSAT|Average Period Inferred CSAT \(Session\)|Formula|sn\_na\_analytics\_insights table|\[\[Aggregate Daily Inferred CSAT \(Session\)\]\]/\[\[Conversation Insights \(Processed\)\]\]|By Empathy, Effort, Confusion, Frustration, Escalation, Assistant, Conversation Channels|Daily|\#|2|
|Total Assist Usage|Conversation Assist Usage Volume|Automated|Gen AI Log Metadata\[sys\_gen\_ai\_log\_metadata\]|Count of Gen AI log assists|By Generative AI Feature, Conversation Channels, Assistant|Daily|\#|0|

## Usage page indicator details

|Visualization|Indicator name|Indicator type|Indicator source table|Calculation|Available breakdowns|Data collection frequency|Unit|Precision|
|-------------|--------------|--------------|----------------------|-----------|--------------------|-------------------------|----|---------|
|Total Conversations by Assistant|Assistant Conversations|Automated|Conversation\[sys\_cs\_conversation\]|Count of conversations|By Context Profiles, Conversation Channels, Conversation State, Assistant|Daily|\#|0|
|Total Conversations by Channel|Assistant Conversations|Automated|Conversation\[sys\_cs\_conversation\]|Count of conversations|By Context Profiles, Conversation Channels, Conversation State, Assistant|Daily|\#|0|
|Result Types Offered|Now Assist in Virtual Agent Results returned|Automated|CI Analytics\[sys\_ci\_analytics\]|Count of Now Assist in Virtual Agent search results returned|By Now Assist in Virtual Agent Result Type, Assistant|Daily|\#|0|
|Conversation State Flow|Assistant Conversations|Automated|Conversation\[sys\_cs\_conversation\]|Count of conversations in each of conversation states: Open, Canceled, Faulted, Completed.|By Context Profiles, Conversation Channels, Conversation State, Assistant|Daily|\#|0|

## Adoption and Engagement page indicator details

<table id="table_i5y_jzw_4hc"><thead><tr><th>

Visualization

</th><th>

Indicator name

</th><th>

Indicator type

</th><th>

Indicator source table

</th><th>

Calculation

</th><th>

Available breakdowns

</th><th>

Data collection frequency

</th><th>

Unit

</th><th>

Precision

</th></tr></thead><tbody><tr><td>

Average Active Users

</td><td>

Daily Conversation Consumers

</td><td>

Automated

</td><td>

Conversation\[sys\_cs\_conversation\]

</td><td>

Count of unique users \(consumer\) where Model Type = LLM and Consumer is not empty and Conversation Type = Interactive

</td><td>

By Assistant, Context Profiles, Conversation Channels, Conversation State

</td><td>

Daily

</td><td>

\#

</td><td>

0

</td></tr><tr><td>

New Users

</td><td>

AI Engagement : New Users

</td><td>

Automated

</td><td>

Conversation\[sys\_cs\_conversation\]

</td><td>

Count of new users \(consumer\) where Model Type = LLM and Consumer is not empty and Conversation Type = Interactive

</td><td>

Conversation Channels, Assistant

</td><td>

Daily

</td><td>

\#

</td><td>

0

</td></tr><tr><td>

Avg Conversations per User

</td><td>

Average Conversations per User

</td><td>

Formula

</td><td>

None

</td><td>

\[\[Assistant Conversations\]\]/\[\[Daily Conversation Consumers\]\]

</td><td>

Assistant, Conversation Channels

</td><td>

Daily

</td><td>

\#

</td><td>

0

</td></tr><tr><td>

Active Assistants

</td><td>

Active Assistants

</td><td>

Automated

</td><td>

Now Assist Deployment\[sys\_now\_assist\_deployment\]

</td><td>

Count of assistants

</td><td>

None

</td><td>

Daily

</td><td>

\#

</td><td>

0

</td></tr><tr><td>

Conversation Volume Trend

</td><td>

Assistant Conversations

</td><td>

Automated

</td><td>

Conversation\[sys\_cs\_conversation\]

</td><td>

Count of conversations where Model Type = LLM and Conversation Type = Interactive

</td><td>

By Context Profiles, Conversation Channels, Conversation State, Assistant

</td><td>

Daily

</td><td>

\#

</td><td>

0

</td></tr><tr><td>

Assist to Execution Trend

</td><td>

-   Conversation Assist Usage Volume
-   AI-Assisted Actions in Conversations
-   Assist to Action Ratio

</td><td>

Formula

</td><td>

None

</td><td>

\[\[Conversation Assist Usage Volume\]\]/\[\[AI-Assisted Actions in Conversations\]\]

</td><td>

By Assistant, Conversation Channels

</td><td>

Daily

</td><td>

\#

</td><td>

0

</td></tr><tr><td>

Conversations per Channel

</td><td>

Assistant Conversations

</td><td>

Automated

</td><td>

Conversation\[sys\_cs\_conversation\]

</td><td>

Count of conversations where Model Type = LLM and Conversation Type = Interactive

</td><td>

By Context Profiles, Conversation Channels, Conversation State, Assistant

</td><td>

Daily

</td><td>

\#

</td><td>

0

</td></tr><tr><td>

New User Growth

</td><td>

AI Engagement : New Users

</td><td>

Automated

</td><td>

Conversation\[sys\_cs\_conversation\]

</td><td>

Count of new users where Model Type = LLM and Consumer is not empty and Conversation Type = Interactive

</td><td>

By Conversation Channels, Assistant

</td><td>

Daily

</td><td>

\#

</td><td>

0

</td></tr></tbody>
</table>## Sentiment page indicator details

<table id="table_fhb_kzw_4hc"><thead><tr><th>

Visualization

</th><th>

Indicator name

</th><th>

Indicator type

</th><th>

Indicator source table

</th><th>

Calculation

</th><th>

Available breakdowns

</th><th>

Data collection frequency

</th><th>

Unit

</th><th>

Precision

</th></tr></thead><tbody><tr><td>

Overall Sentiment

</td><td>

Average Daily Inferred CSAT \(Session\)

</td><td>

Automated

</td><td>

Conversation Insights\[sn\_aci\_insights\]

</td><td>

Average CSAT where CSAT processed = true and Conversation Conversation Type = Interactive and Conversation Model Type = LLM

</td><td>

By Confusion, Effort, Empathy, Escalation, Frustration, Assistant, Conversation Channels

</td><td>

Daily

</td><td>

\#

</td><td>

2

</td></tr><tr><td>

Conversations Analyzed

</td><td>

Conversation Insights \(Processed\)

</td><td>

Automated

</td><td>

Conversation Insights\[sn\_aci\_insights\]

</td><td>

Count of conversations where CSAT processed = true and Conversation Conversation Type = Interactive and Conversation Model Type = LLM

</td><td>

By Confusion, Effort, Empathy, Escalation, Frustration, Assistant, Conversation Channels, Next Steps, Resolution State

</td><td>

Daily

</td><td>

\#

</td><td>

0

</td></tr><tr><td>

High Empathy Rate

</td><td>

High Empathy Rate - Conversation Insights

</td><td>

Formula

</td><td>

None

</td><td>

\(\[\[Conversation Insights \(Processed\) &gt; Empathy = High\]\]/\[\[Conversation Insights \(Processed\)\]\]\) \* 100

</td><td>

By Conversation Channels, Confusion, Effort, Empathy, Escalation, Frustration, Assistant

</td><td>

Daily

</td><td>

%

</td><td>

0

</td></tr><tr><td>

Conversations with Negative Emotions

</td><td>

Percentage of Conversations with Negative Emotions

</td><td>

Formula

</td><td>

None

</td><td>

\(\[\[Conversation Insights \(Negative Emotions\)\]\]/\[\[Conversation Insights \(Processed\)\]\]\)\*100

</td><td>

Conversation Channels, Assistant

</td><td>

Daily

</td><td>

%

</td><td>

2

</td></tr><tr><td>

Average Inferred CSAT Over Time

</td><td>

Average Daily Inferred CSAT \(Session\)

</td><td>

Automated

</td><td>

Conversation Insights\[sn\_aci\_insights\]

</td><td>

Average CSAT where CSAT processed = true and Conversation Conversation Type = Interactive and Conversation Model Type = LLM and Session CSAT is not empty

</td><td>

By Confusion, Effort, Conversation Channels, Empathy, Escalation, Frustration, Assistant

</td><td>

Daily

</td><td>

\#

</td><td>

2

</td></tr><tr><td>

Transfers and Escalations Over Time

</td><td>

Conversation Insights \(Processed\)

</td><td>

Automated

</td><td>

Conversation Insights\[sn\_aci\_insights\]

</td><td>

Count of conversations where CSAT processed = true and Conversation Conversation Type = Interactive and Conversation Model Type = LLM

</td><td>

By Confusion, Effort, Empathy, Escalation, Frustration, Assistant, Conversation Channels, Next Steps, Resolution State

</td><td>

Daily

</td><td>

\#

</td><td>

0

</td></tr><tr><td>

Average Inferred CSAT \(Virtual Agent\)

</td><td>

Average Daily Inferred CSAT \(Virtual Agent\)

</td><td>

Automated

</td><td>

Conversation Insights\[sn\_aci\_insights\]

</td><td>

Average CSAT \(Virtual agent\) where CSAT processed = true and Conversation Conversation Type = Interactive and Conversation Model Type = LLM and AI agent CSAT is not empty

</td><td>

By Confusion, Effort, Empathy, Conversation Channels, Escalation, Frustration, Assistant

</td><td>

Daily

</td><td>

\#

</td><td>

2

</td></tr><tr><td>

Average Inferred CSAT \(Live Agent\)

</td><td>

Average Daily Inferred CSAT \(Live Agent\)

</td><td>

Automated

</td><td>

Conversation Insights\[sn\_aci\_insights\]

</td><td>

Average CSAT \(live agent\) where CSAT processed = true and Conversation Conversation Type = Interactive and Conversation Model Type = LLM and Human agent CSAT is not empty

</td><td>

By Confusion, Effort, Empathy, Conversation Channels, Escalation, Frustration, Assistant

</td><td>

Daily

</td><td>

\#

</td><td>

2

</td></tr><tr><td>

Average Inferred CSAT \(Session\)

</td><td>

Average Daily Inferred CSAT \(Session\)

</td><td>

Automated

</td><td>

Conversation Insights\[sn\_aci\_insights\]

</td><td>

Average CSAT where CSAT processed = true and Conversation Conversation Type = Interactive and Conversation Model Type = LLM and Session CSAT is not empty

</td><td>

By Confusion, Effort, Conversation Channels, Empathy, Escalation, Frustration, Assistant

</td><td>

Daily

</td><td>

\#

</td><td>

2

</td></tr><tr><td>

Assistant Recommended Next Steps

</td><td>

Conversation Insights \(Processed\)

</td><td>

Automated

</td><td>

Conversation Insights\[sn\_aci\_insights\]

</td><td>

Count of conversations where CSAT processed = true and Conversation Conversation Type = Interactive and Conversation Model Type = LLM

</td><td>

By Confusion, Effort, Empathy, Escalation, Frustration, Assistant, Conversation Channels, Next Steps, Resolution State

</td><td>

Daily

</td><td>

\#

</td><td>

0

</td></tr><tr><td>

Conversation Insight Inferred Resolution State

</td><td>

Conversation Insights \(Processed\)

</td><td>

Automated

</td><td>

Conversation Insights\[sn\_aci\_insights\]

</td><td>

Count of conversations where CSAT processed = true and Conversation Conversation Type = Interactive and Conversation Model Type = LLM

</td><td>

By Confusion, Effort, Empathy, Escalation, Frustration, Assistant, Conversation Channels, Next Steps, Resolution State

</td><td>

Daily

</td><td>

\#

</td><td>

0

</td></tr><tr><td>

Empathy Levels Distribution Over Time

</td><td>

Conversation Insights \(Processed\)

</td><td>

Automated

</td><td>

Conversation Insights\[sn\_aci\_insights\]

</td><td>

Count of conversations where CSAT processed = true and Conversation Conversation Type = Interactive and Conversation Model Type = LLM

</td><td>

By Confusion, Effort, Empathy, Escalation, Frustration, Assistant, Conversation Channels, Next Steps, Resolution State

</td><td>

Daily

</td><td>

\#

</td><td>

0

</td></tr><tr><td>

Negative Emotion Feedback Over Time

</td><td>

Conversation Insights \(Processed\)

</td><td>

Automated

</td><td>

Conversation Insights\[sn\_aci\_insights\]

</td><td>

Frustration: Count of conversations where CSAT processed = true and Conversation Conversation Type = Interactive and Conversation Model Type = LLM and Frustrations is Yes

 Confusion: Count of conversations where CSAT processed = true and Conversation Conversation Type = Interactive and Conversation Model Type = LLM and Confusion is Yes

</td><td>

By Confusion, Effort, Empathy, Escalation, Frustration, Assistant, Conversation Channels, Next Steps, Resolution State

</td><td>

Daily

</td><td>

\#

</td><td>

0

</td></tr></tbody>
</table>## Self-Solve Performance page indicator details

**Note:** The records in the Deflection Log \[sys\_cs\_deflection\_log\] table are retained for a period of 60 days.

|Visualization|Indicator name|Indicator type|Indicator source table|Calculation|Available breakdowns|Data collection frequency|Unit|Precision|
|-------------|--------------|--------------|----------------------|-----------|--------------------|-------------------------|----|---------|
|Total Deflection Events|Deflection Logs|Automated|Deflection Log\[sys\_cs\_deflection\_log\]|Count of events where Conversation is not empty and Conversation Conversation Type = Interactive and Conversation Model Type = LLM|Assistant, Conversation Channels, Deflection Types, Deflection State|Daily|\#|0|
|Total Deflections|Deflection Logs : Resolved|Automated|Deflection Log\[sys\_cs\_deflection\_log\]|Count of events where State = Resolved and Conversation is not empty and Conversation Conversation Type = Interactive and Conversation Model Type = LLM and Conversation Live Agent Transfer Time is empty|Assistant, Conversation Channels|Daily|\#|0|
|Total Live Agent Transfers|Total Live Agent Transfers|Automated|Conversation\[sys\_cs\_conversation\]|Count of conversations where Model Type = LLM and Conversation Type = Interactive and Live Agent Transfer Time is not empty|Assistant, Conversation Channels|Daily|\#|0|
|Deflection Rate|Deflection Rate|Formula|Deflection Log \[sys\_cs\_deflection\_log\]|\(\[Number of deflection records Resolved\]/\[Number of deflection records\]\)\*100|Assistant, Conversation Channels|Daily|%|2|
|Deflection Rate Over Time|Deflection Rate|Formula|Deflection Log \[sys\_cs\_deflection\_log\]|\(\[Number of deflection records Resolved\]/\[Number of deflection records\]\)\*100|Assistant, Conversation Channels|Daily|%|2|
|Deflection Outcome Distribution|Deflection Logs|Automated|Deflection Log \[sys\_cs\_deflection\_log\]|Count of events where Conversation is not empty and Conversation Conversation Type = Interactive and Conversation Model Type = LLM|Assistant, Conversation Channels, Deflection Types, Deflection State|Daily|\#|0|
|Deflection Types Offered|Deflection Logs|Automated|Deflection Log \[sys\_cs\_deflection\_log\]|Count of events where Conversation is not empty and Conversation Conversation Type = Interactive and Conversation Model Type = LLM|Assistant, Conversation Channels, Deflection Types, Deflection State|Daily|\#|0|
|Effort Score|Effort Score|Automated|Conversation Insights\[sn\_aci\_insights\]|Count of conversations where CSAT processed = true and Conversation Conversation Type = Interactive and Conversation Model Type = LLM and Effort Score in \(High, Medium, Low\)|Assistant, Conversation Channels, Effort|Daily|\#|0|

## Assists page indicator details

|Visualization|Indicator name|Indicator type|Indicator source table|Calculation|Available breakdowns|Data collection frequency|Unit|Precision|
|-------------|--------------|--------------|----------------------|-----------|--------------------|-------------------------|----|---------|
|Sum of all Conversational Assists|Conversation Assist Usage Volume|Automated|Gen AI Log Metadata\[sys\_gen\_ai\_log\_metadata\]|Count of Gen AI log assists|By Generative AI Feature, Conversation Channels, Assistant|Daily|\#|0|
|Assist Consumption|Conversation Assist Usage Volume|Automated|Gen AI Log Metadata\[sys\_gen\_ai\_log\_metadata\]|Count of Gen AI log assists by assistant|By Generative AI Feature, Conversation Channels, Assistant|Daily|\#|0|
|Executions per Assistant|AI-Assisted Actions in Conversations|Automated|Gen AI Log Metadata\[sys\_gen\_ai\_log\_metadata\]|Count of Gen AI log actions by assistant|By Conversation Channels, Assistant|Daily|\#|0|
|Trending sum of all Assists|Conversation Assist Usage Volume|Automated|Gen AI Log Metadata\[sys\_gen\_ai\_log\_metadata\]|Sum of Gen AI log assists|By By Generative AI Feature, Conversation Channels, Assistant|Daily|\#|0|
|Top 10 Most Used AI Features|Generative AI Usage Log|Pivot Table|Generative AI Usage Log \[sys\_gen\_ai\_usage\_log\]|None|None|Daily|\#|0|

## Voice page indicator details

|Visualization|Indicator name|Indicator type|Indicator source table|Calculation|Available breakdowns|Frequency|Unit|Precision|
|-------------|--------------|--------------|----------------------|-----------|--------------------|---------|----|---------|
|Percent voice conversations deflected|None|None|None|Percentage of voice conversations where Resolved = Yes|None|Daily|%|1|
|Total deflected conversations over time|Now Assist Analytics Assistant Ims|Automated|Now Assist Analytics Assistant Ims \[sn\_na\_analytics\_conv\_ims\]|Count of voice conversations where Resolved = Yes| |Daily|\#|0|
|Total conversations|Now Assist Analytics Assistant Ims|Automated|Now Assist Analytics Assistant Ims \[sn\_na\_analytics\_conv\_ims\]|Count of conversations where Assistant Type = Voice| |Daily|\#|0|
|Total conversations over time|Now Assist Analytics Assistant Ims|Automated|Now Assist Analytics Assistant Ims \[sn\_na\_analytics\_conv\_ims\]|Count of all voice calls|None|Daily|\#|0|
|AI Voice Agents in use|Now Assist Analytics Insights|Automated|Now Assist Analytics Insights \[sn\_na\_analytics\_insights\]|Count of AI agents where Assistant Type = Voice|None|Daily|\#|0|
|AI Voice Agents in use over time|Now Assist Analytics Insights|Automated|Now Assist Analytics Insights \[sn\_na\_analytics\_insights\]|Count of AI agents where Assistant Type = Voice|None|Daily|\#|0|
|Conversations transferred to a live agent|Now Assist Analytics Assistant Ims|Automated|Now Assist Analytics Assistant Ims \[sn\_na\_analytics\_conv\_ims\]|Count of voice calls where Agent chat=true|None|Daily|\#|0|
|Number of tickets created|Now Assist Analytics Ims Related Record|Automated|Now Assist Analytics Ims Related Record \[sn\_na\_analytics\_conv\_ims\_related\_record\]|Count of Interaction Related Records where Agent chat = false and Interaction Virtual agent = true and Interaction Type = Phone and Interaction AI Voice = true|None|Daily|\#|0|
|Conversations disconnected|Now Assist Analytics Assistant Ims|Automated|Now Assist Analytics Assistant Ims \[sn\_na\_analytics\_conv\_ims\]|Count of voice calls where State=Closed Abandoned|None|Daily|\#|0|
|Immediate live agent transfers|None|None|Single score|Count of conversations where live agent transfer = yes and call duration &lt; 30 secs|None|Daily|\#|0|
|Inferred customer satisfaction \(CSAT\): average score \(out of 5\)|Now Assist Analytics Insights|sn\_na\_analytics\_insights table|Now Assist Analytics Insights \[sn\_na\_analytics\_insights\]|Average of session CSAT|None|Daily|\#|2|
|Average voice conversation duration|Now Assist Analytics Assistant Ims|Formula|Now Assist Analytics Assistant Ims \[sn\_na\_analytics\_conv\_ims\]|\[\[AI Agent- Summed duration of calls\]\] / \[\[AI Agents- Total Calls\]\]|None|Daily|Minutes|0|
| |Response Time|
|50th percentile response time|None|None|Single score|Response time in seconds where 50% responses are completed|None|Daily|Seconds|1|
|90th percentile response time|None|None|Single score|Response time in seconds where 90% responses are completed|None|Daily|Seconds|1|
|99th percentile response time|None|None|Single score|Response time in seconds where 99% responses are completed|None|Daily|Seconds|1|
| |Tool Insights \(Executions by tool type\)|
|Scripts|Now Assist Analytics Tool Execution|Automated|Now Assist Analytics Tool Execution \[sn\_na\_analytics\_tool\_execution\]|Count of tool executions where Assistant Type = Voice and Tool Type = Script|None|Daily|\#|0|
|Flow actions|Now Assist Analytics Tool Execution|Automated|Now Assist Analytics Tool Execution \[sn\_na\_analytics\_tool\_execution\]|Count of tool executions where Assistant Type = Voice and Tool Type = Flow action|None|Daily|\#|0|
|Subflows|Now Assist Analytics Tool Execution|Automated|Now Assist Analytics Tool Execution \[sn\_na\_analytics\_tool\_execution\]|Count of tool executions where Assistant Type = Voice and Tool Type = Subflow|None|Daily|\#|0|
|RAG-based search|Now Assist Analytics Tool Execution|Automated|Now Assist Analytics Tool Execution \[sn\_na\_analytics\_tool\_execution\]|Count of tool executions where Assistant Type = Voice and Tool Type = Search Retriever|None|Daily|\#|0|
|50th percentile response time|None|None|Single score|Tool execution time in seconds where 50% executions are completed|None|Daily|Seconds|1|
|90th percentile response time|None|None|Single score|Tool execution time in seconds where 90% executions are completed|None|Daily|Seconds|1|
|99th percentile response time|None|None|Single score|Tool execution time in seconds where 99% executions are completed|None|Daily|Seconds|1|
|Use of AI agents|
|Voice AI agent summary|Agent Conversations|Automated|Now Assist Analytics Insights \[sn\_na\_analytics\_insights\]|Count of agents where Assistant Type = Voice and Resolved in \(Yes, No\)\)|None|Daily|\#|0|

