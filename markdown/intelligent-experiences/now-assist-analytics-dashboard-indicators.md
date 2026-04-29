---
title: Now Assist Analytics dashboard indicator details
description: Indicator details help you understand the data and calculations behind an indicator that is presented in the form of a visualization on the dashboard.
locale: en-US
release: australia
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 10
keywords: [Now Assist Analytics, indicators, Platform Analytics Administration, GenAI, Generative AI]
breadcrumb: [Now Assist Analytics reference, Analyzing Now Assist performance, Exploring Now Assist Admin, Now Assist, Enable AI experiences]
---

# Now Assist Analytics dashboard indicator details

Indicator details help you understand the data and calculations behind an indicator that is presented in the form of a visualization on the dashboard.

Now Assist Analytics indicators contain the following details: indicator type, data source, calculation, available breakdowns, unit, and so on.

To access these indicators, navigate to **Platform Analytics Administration** &gt; **Indicators**. You must have the Now Assist Analytics Admin \[sn\_na\_analytics\_admin\] role to access the indicators.

These indicators collect data at a daily frequency. Data is only available for dates before the current date. If you want to see results from the current day, you must wait until the next day.

**Note:** The Generative AI Usage Log \[sys\_gen\_ai\_usage\_log\] table is maint-only.

## Usage and adoption indicator details

|Visualization|Indicator type|Indicator source table|Calculation|Available breakdowns|Frequency|Unit|Precision|
|-------------|--------------|----------------------|-----------|--------------------|---------|----|---------|
|Total Now Assist actions|Automated|Generative AI Usage Log\[sys\_gen\_ai\_usage\_log\]|Count of all actions|By Gen AI Feature, By Generative AI Skill Execution Modality, By Skill Family, By Skills Config, By Skills Config, By Workflow|Daily|\#|0|
|Daily Now Assist actions|Automated|Generative AI Usage Log\[sys\_gen\_ai\_usage\_log\]|Count of daily actions|By Gen AI Feature, By Generative AI Skill Execution Modality, By Skill Family, By Skills Config, By Skills Config, By Workflow|Daily|\#|0|
|Average daily unique users engaging with Now Assist|Automated|Generative AI Usage Log\[sys\_gen\_ai\_usage\_log\]|Average of daily unique users|By Gen AI Feature, By Skills Config, By Skill Family, By Generative AI Skill Execution Modality|Daily|\#|0|
|Daily unique users engaging with Now Assist|Automated|Generative AI Usage Log\[sys\_gen\_ai\_usage\_log\]|Count of daily unique users|By Gen AI Feature, By Skills Config, By Skill Family, By Generative AI Skill Execution Modality|Daily|\#|0|
|Skill group distribution|Automated|Generative AI Usage Log\[sys\_gen\_ai\_usage\_log\]|Count of daily skill executions grouped By Gen AI Feature, By Generative AI Skill Execution Modality, By Skill Family, By Skills Config, By Skills Config|By Gen AI Feature, By Generative AI Skill Execution Modality, By Skill Family, By Skills Config, By Skills Config, By Workflow|Daily|\#|0|
|Daily usage comparison by workflow|Automated|Generative AI Usage Log\[sys\_gen\_ai\_usage\_log\]|Count of actions grouped by workflows|By Gen AI Feature, By Generative AI Skill Execution Modality, By Skill Family, By Skills Config, By Skills Config, By Workflow|Daily|\#|0|
|Skill engagement trend|Automated|Generative AI Usage Log\[sys\_gen\_ai\_usage\_log\]|Count of actions grouped by skill|By Gen AI Feature, By Generative AI Skill Execution Modality, By Skill Family, By Skills Config, By Skills Config, By Workflow|Daily|\#|0|
|Departments with highest usage|Automated|Generative AI Usage Log\[sys\_gen\_ai\_usage\_log\]|Count of actions grouped by user department and sorted by descending order|By Department, By Skills Config|Daily|\#|0|
|Now Assist actions comparison by user department|Automated|Generative AI Usage Log\[sys\_gen\_ai\_usage\_log\]|Count of actions grouped by user department|By Department, By Skills Config|Daily|\#|0|
|Feedback details|Automated|Gen AI Log Metadata\[sys\_gen\_ai\_log\_metadata\]|Count of actions grouped by Skill Family|By Skill Family, By Skills Config|Daily|\#|0|
|Automated|Gen AI Log Metadata\[sys\_gen\_ai\_log\_metadata\]|Count of actions with feedback grouped by Skill Family|By Feedback, By Skill Family, By Skills Config|Daily|\#|0|
|Formula|Gen AI Log Metadata\[sys\_gen\_ai\_log\_metadata\]|\(Count of actions with feedback/Total count of actions\) x 100 grouped by Skill Family|By Skill Family, By Skills Config|Daily|%|2|
|Automated|Gen AI Log Metadata\[sys\_gen\_ai\_log\_metadata\]|Count of actions where By Feedback is Accepted grouped by Skill Family|By Skill Family, By Skills Config, By Feedback|Daily|\#|0|
|Formula|Gen AI Log Metadata\[sys\_gen\_ai\_log\_metadata\]|\(Count of actions where By Feedback is Accepted/Total count of actions with feedback\) x 100 grouped by Skill Family|By Skills Config, By Skill Family|Daily|%|2|
|Error details|Automated|Gen AI Log Metadata\[sys\_gen\_ai\_log\_metadata\]|Count of actions grouped by Skill Family|By Skill Family, By Skills Config|Daily|\#|0|
|Automated|Gen AI Log Metadata\[sys\_gen\_ai\_log\_metadata\]|Count of actions with error status grouped by Skill Family|By Gen AI Log Metadata Status , By Skill Family, By Skills Config|Daily|\#|0|
|Formula|Gen AI Log Metadata\[sys\_gen\_ai\_log\_metadata\]|\(Count of actions with error status/Total count of generative AI metadata records\) x 100 grouped by Skill Family|By Skill Family, By Skills Config|Daily|%|2|

## Skill performance indicator details

|Visualization|Indicator type|Indicator source table|Calculation|Available breakdowns|Frequency|Unit|Precision|
|-------------|--------------|----------------------|-----------|--------------------|---------|----|---------|
|Skill engagement trend|Automated|Generative AI Usage Log\[sys\_gen\_ai\_usage\_log\]|Count of skill executions grouped by skill|By Gen AI Feature, By Generative AI Skill Execution Modality, By Skill Family, By Skills Config, By Workflow|Daily|\#|0|
|Number of actions|Automated|Generative AI Usage Log\[sys\_gen\_ai\_usage\_log\]|Count of all skill executions|By Gen AI Feature, By Generative AI Skill Execution Modality, By Skill Family, By Skills Config, By Workflow|Daily|\#|0|
|Total daily active users|Automated|Generative AI Usage Log\[sys\_gen\_ai\_usage\_log\]|Count of daily unique users|By Gen AI Feature, By Skills Config, By Skill Family, By Generative AI Skill Execution Modality|Daily|\#|0|
|Total daily active users by skills|Automated|Generative AI Usage Log\[sys\_gen\_ai\_usage\_log\]|Count of daily unique users grouped by Skills Config|By Gen AI Feature, By Skills Config, By Skill Family, By Generative AI Skill Execution Modality|Daily|\#|0|

## Skill details indicator details

|Visualization|Indicator type|Indicator source table|Calculation|Available breakdowns|Frequency|Unit|Precision|
|-------------|--------------|----------------------|-----------|--------------------|---------|----|---------|
|Skill engagement trend|Automated|Generative AI Usage Log\[sys\_gen\_ai\_usage\_log\]|Count of skill executions grouped by Skills Config|By Gen AI Feature, By Generative AI Skill Execution Modality, By Skill Family, By Skills Config, By Workflow|Daily|\#|0|
|Total skill actions|Automated|Generative AI Usage Log\[sys\_gen\_ai\_usage\_log\]|Count of skill executions|By Gen AI Feature, By Generative AI Skill Execution Modality, By Skill Family, By Skills Config, By Workflow|Daily|\#|0|
|Accepted skill actions|Automated|Gen AI Log Metadata\[sys\_gen\_ai\_log\_metadata\]|Count of skill executions where Feedback is Accepted|By Feedback, By response accepted without edits, By Skills Config, By Skill Family|Daily|\#|0|
|Acceptance rate|Formula|Gen AI Log Metadata\[sys\_gen\_ai\_log\_metadata\]|\(Count of skill executions where Feedback is Accepted/Count of skill executions\)x100|By Skills Config|Daily|%|0|
|Daily active users|Automated|Generative AI Usage Log\[sys\_gen\_ai\_usage\_log\]|Count of daily unique users|By Gen AI Feature, By Skills Config, By Skill Family, By Generative AI Skill Execution Modality|Daily|\#|0|

## Custom skills indicator details

|Visualization|Indicator type|Indicator source table|Calculation|Available breakdowns|Frequency|Unit|Precision|
|-------------|--------------|----------------------|-----------|--------------------|---------|----|---------|
|Skill engagement trend by workflows|Automated|Generative AI Usage Log\[sys\_gen\_ai\_usage\_log\]|Count of custom skill executions grouped by workflows|By Custom Skill \(Workflow Type\), By Custom Skill \(Feature Type\), By Custom Skill \(Product Type\), By Custom Skill Completion Status, By Skills Config|Daily| |0|
|Skill engagement trend by products|Automated|Generative AI Usage Log\[sys\_gen\_ai\_usage\_log\]|Count of custom skill executions grouped by products|By Custom Skill \(Workflow Type\), By Custom Skill \(Feature Type\), By Custom Skill \(Product Type\), By Custom Skill Completion Status, By Skills Config|Daily| |0|
|Skill engagement trend by features|Automated|Generative AI Usage Log\[sys\_gen\_ai\_usage\_log\]|Count of custom skill executions grouped by features|By Custom Skill \(Workflow Type\), By Custom Skill \(Feature Type\), By Custom Skill \(Product Type\), By Custom Skill Completion Status, By Skills Config|Daily| |0|
|Daily unique users engaging with the skill|Automated|Generative AI Usage Log\[sys\_gen\_ai\_usage\_log\]|Count of unique users who executed custom skills|By Skills Config|Daily|\#|0|
|Executed successfully|Formula|Generative AI Usage Log\[sys\_gen\_ai\_usage\_log\]|\(Count of custom skill executions with status Completed/Count of custom skill executions\)x100|By Skills Config|Daily|%|2|
|Skills feedback|Automated|Generative AI Usage Log\[sys\_gen\_ai\_usage\_log\]|Count|By Feedback, By Skills Config|Daily|\#|0|

## Now Assist Guardian offensive content guardrail indicator details

|Visualization|Indicator type|Indicator source table|Calculation|Available breakdowns|Frequency|Unit|Precision|
|-------------|--------------|----------------------|-----------|--------------------|---------|----|---------|
|Guardrail-added latency|Automated|Generative AI Metric\[sys\_generative\_ai\_metric\]|Average time taken by the guardrail to evaluate offensive content|By Skills Config|Daily|Milliseconds|0|
|Percentage flagged as offensive|Formula|Generative AI Metric\[sys\_generative\_ai\_metric\]|\(Count of offensive content occurrences/Total number of LLM calls for which the guardrail was enabled\)x100|By Skills Config|Daily|%|0|
|Total offensive content occurrences|Automated|Generative AI Metric\[sys\_generative\_ai\_metric\]|Count of offensive content occurrences|By Gen AI metric value, By Skills Config|Daily|\#|0|
|Categories of offensive content|Automated|Generative AI Metric\[sys\_generative\_ai\_metric\]|Count of offensive content occurrences grouped by categories|By Offensiveness Type, By Skills Config|Daily|\#|0|
|Offensive content occurrences by skill|Automated|Generative AI Metric\[sys\_generative\_ai\_metric\]|Count of offensive content occurrences grouped by skill|By Gen AI metric value, By Skills Config|Daily|\#|0|

## Now Assist Guardian prompt injection guardrail indicator details

|Visualization|Indicator type|Indicator source table|Calculation|Available breakdowns|Frequency|Unit|Precision|
|-------------|--------------|----------------------|-----------|--------------------|---------|----|---------|
|Guardrail-added latency|Automated|Generative AI Metric\[sys\_generative\_ai\_metric\]|Average time taken by the guardrail to evaluate prompt injection|By Skills Config|Daily|Milliseconds|0|
|Percentage flagged as prompt injection|Formula|Generative AI Metric\[sys\_generative\_ai\_metric\]|\(Count of prompt injection occurrences/Total number of LLM calls for which the guardrail was enabled\)x100|By Skills Config|Daily|%|0|
|Total prompt injection occurrences|Automated|Generative AI Metric\[sys\_generative\_ai\_metric\]|Count of prompt injection occurrences|By Gen AI metric value, By Skills Config|Daily|\#|0|
|Prompt injection occurrences by skill|Automated|Generative AI Metric\[sys\_generative\_ai\_metric\]|Count of prompt injection occurrences grouped by skill|By Gen AI metric value, By Skills Config|Daily|\#|0|

## User search analyzer indicator details

|Visualization|Indicator type|Indicator source table|Calculation|Available breakdowns|Frequency|Unit|Precision|
|-------------|--------------|----------------------|-----------|--------------------|---------|----|---------|
|Queries with Genius Results|Automated|Search Event\[sys\_search\_event\]|Count of search queries where Genius Result Displayed = true|AIS Search Application|Daily|\#|0|
|Genius Result engagement|Automated|Genius Result Event Action\[sys\_search\_genius\_result\_event\_action\]|Count of genius results where Card Type = Now Assist Multi-Content Response and Action Type = Show Full Answer or Action Type = Ask a Follow Up or Action Type = uxf\_client\_action|AIS Search Application|Daily|\#|0|
|Genius Result response time|Automated|Search Signal Event\[sys\_search\_signal\_event\]|Average \(Genius Result Response Time in Seconds\)|AIS Search Application|Daily|Seconds|0|
|Genius Result to chat handoff|Automated|Genius Result Event Action\[sys\_search\_genius\_result\_event\_action\]|Count of queries where Card Type = Now Assist Multi-Content Response and Action Type = Ask a Follow Up|AIS Search Application|Daily|\#|0|
|Genius Results citation engagement|Automated|Genius Result Event Action\[sys\_search\_genius\_result\_event\_action\]|Count of queries where Card Type = Now Assist Multi-Content Response and Action Type = uxf\_client\_action|AIS Search Application|Daily|\#|0|
|Feedback \(Thumbs up\)|Automated|Genius Result Event Action\[sys\_search\_genius\_result\_event\_action\]|Count of queries where Card Type = Now Assist Multi-Content Response and Action Type = Feedback and Action Value = Helpful|AIS Search Application|Daily|\#|0|
|Feedback \(Thumbs down\)|Automated|Genius Result Event Action\[sys\_search\_genius\_result\_event\_action\]|Count of queries where Card Type = Now Assist Multi-Content Response and Action Type = Feedback and Action Value = Not Helpful|AIS Search Application|Daily|\#|0|
|Genius Results with KB|Automated|Search Signal Genius Result Triggered Event\[sys\_search\_signal\_genius\_result\_triggered\_event\]|Count of queries where Source Table = kb\_knowledge|AIS Search Application|Daily|\#|0|
|Genius Results with Catalog Item|Automated|Search Signal Genius Result Triggered Event\[sys\_search\_signal\_genius\_result\_triggered\_event\]|Count of queries where Source Table = sc\_cat\_item|AIS Search Application|Daily|\#|0|
|Top 10 queries with KB Genius Result|Automated|Search Signal Genius Result Triggered Event \[sys\_search\_signal\_genius\_result\_triggered\_event\]|Top 10 queries with count of genius results where Source Table = kb\_knowledge|Not Applicable|Daily|Not Applicable|Not Applicable|
|Top 10 queries with Catalog Item Genius Result|Automated|Search Signal Genius Result Triggered Event \[sys\_search\_signal\_genius\_result\_triggered\_event\]|Top 10 queries with count of genius results where Source Table = sc\_cat\_item|Not Applicable|Daily|Not Applicable|Not Applicable|

## Now Assist context menu analytics indicator details

|Visualization|Indicator type|Indicator source table|Calculation|Available breakdowns|Frequency|Unit|Precision|
|-------------|--------------|----------------------|-----------|--------------------|---------|----|---------|
|Usage in this period|Automated|Generative AI Log\[sys\_generative\_ai\_log\]|Count of actions where Source is Now Assist context menu|By NAcm implicit feedback, By Skills Config, By Feedback, By Status, By Skill Capability|Daily|\#|0|
|Acceptance distribution|Automated|Generative AI Log\[sys\_generative\_ai\_log\]|Count of actions where content generated by Now Assist context menu grouped by Accepted or Not Accepted|By NAcm implicit feedback, By Skills Config, By Feedback, By Status, By Skill Capability|Daily|\#|0|
|Usage trend by skill|Automated|Generative AI Log\[sys\_generative\_ai\_log\]|Count of context menu actions grouped by Now Assist skills|By NAcm implicit feedback, By Skills Config, By Feedback, By Status, By Skill Capability|Daily|\#|0|
|Capability distribution|Automated|Generative AI Log\[sys\_generative\_ai\_log\]|Count of context menu actions grouped by capability|By NAcm implicit feedback, By Skills Config, By Feedback, By Status, By Skill Capability|Daily|\#|0|
|Responses by feedback|Automated|Generative AI Log\[sys\_generative\_ai\_log\]|Count of actions where feedback for the content generated by Now Assist context menu grouped by Accepted or Rejected.|By NAcm implicit feedback, By Skills Config, By Feedback, By Status, By Skill Capability|Daily|\#|0|

