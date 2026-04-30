---
title: Additional skill input and trigger information
description: Enable remaining generative AI skills within Now Assist for CSM, and reference summarized details to complete setup.
locale: en-US
release: zurich
product: Now Assist for CSM
classification: now-assist-for-csm
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Activate Now Assist Skills, Configure, Now Assist for CSM, Customer Service Management]
---

# Additional skill input and trigger information

Enable remaining generative AI skills within Now Assist for CSM, and reference summarized details to complete setup.

## Overview of skills and triggers

Depending on the selected skill, you can configure inputs or triggers. These settings determine how and when a skill is used. An input identifies the data that is used for a skill, such as the table and fields that are used to generate a case summary. A trigger initiates an action, such as when the system generates a chat summary.

## Sidebar discussion summarization skill

For the sidebar discussion summarization skill, select the triggers that determine when a sidebar discussion summary is generated.

The following table lists the triggers that determine when a sidebar discussion summary is generated.

|Trigger|Description|
|-------|-----------|
|User triggered|Sidebar discussion summarization that is generated when the agent manually triggers the skill.|

## Case sentiment analysis skill

The case sentiment analysis skill includes the inputs and outputs that identify the table and fields that are used when a case sentiment is generated.

The following table lists the inputs for the case sentiment analysis skill.

<table id="table_apt_5cv_52c"><thead><tr><th>

Input

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Input table

</td><td>

Case \[Case\]

</td></tr><tr><td>

Input fields

</td><td>

-   Short description
-   Description
-   Priority
-   State
-   Task creation date
-   Activities
-   Task SLA

</td></tr></tbody>
</table>The following table lists the outputs for the case sentiment analysis skill.

<table id="table_ffk_hfv_52c"><thead><tr><th>

Output

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Sentiment values

</td><td>

-   Very positive
-   Positive
-   Neutral
-   Negative
-   Very negative

</td></tr><tr><td>

Sentiment trend

</td><td>

-   Improving
-   Declining
-   Stable

</td></tr><tr><td>

Sentiment reasoning

</td><td>

Reasons for provide the sentiment value.

</td></tr></tbody>
</table>The following table lists the scheduled job for the sentiment analysis skill.

|Scheduled job name|Default value|Description|
|------------------|-------------|-----------|
|Sentiment analysis scheduled job \(case\)|True|Refreshes sentiments on the Trigger frequency screen for the Sentiment analysis skill.|
|Update sentiment historical records|False|When active, calculates sentiment and sentiment trends for historical records.|

## Suggested steps generation skill

The following table lists the suggested steps generation skill.

<table id="table_id3_4qw_52c"><thead><tr><th>

Input

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Input table

</td><td>

sn\_customerservice\_case

</td></tr><tr><td>

Input field

</td><td>

Short description

 The skill uses this field to cluster cases based on similar cases closed in the past.

</td></tr><tr><td>

Conditions

</td><td>

Filter conditions to generate the suggested steps.

 Similar cases closed or resolved within the last 6 months are used by default to create the case clusters.

</td></tr></tbody>
</table>