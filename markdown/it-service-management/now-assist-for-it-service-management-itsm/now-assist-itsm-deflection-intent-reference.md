---
title: Deflecting incidents in Now Assist for IT Service Management \(ITSM\) reference
description: Deflection retrieves user context and sentiment analysis to rephrase search queries for more relevant results.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/now-assist-for-it-service-management-itsm/now-assist-itsm-deflection-intent-reference.html
release: australia
product: Now Assist for IT Service Management \(ITSM\)
classification: now-assist-for-it-service-management-itsm
topic_type: reference
last_updated: "2026-06-24"
reading_time_minutes: 1
keywords: [user context, Now Assist for ITSM, incident classification]
breadcrumb: [In-form deflection, Use generative AI skills, Now Assist for IT Service Management \(ITSM\), IT Service Management]
---

# Deflecting incidents in Now Assist for IT Service Management \(ITSM\) reference

Deflection retrieves user context and sentiment analysis to rephrase search queries for more relevant results.

## User context information

The system retrieves the following user context information from the knowledge graph to personalize search results.

|Context type|Description|
|------------|-----------|
|Hardware|The primary device used by the user. Examples: MacBook Pro, Dell Laptop, Windows Desktop. This context is applied to queries about device-specific issues.|
|Location|The user's office location or site. This context is applied to queries about location-specific services, networks, or resources.|

## When user context is applied to queries

User context is applied to the search query only when the context is relevant to the issue description.

<table id="table_vf3_4dv_rjc"><thead><tr><th>

Original description

</th><th>

User hardware context

</th><th>

Rephrased query that is passed to search

</th></tr></thead><tbody><tr><td>

My laptop is not working

</td><td>

MacBook Pro

</td><td>

MacBook Pro not working

</td></tr><tr><td>

My laptop is stuck

</td><td>

MacBook Pro

</td><td>

MacBook Pro stuck

</td></tr><tr><td>

What is Outlook

</td><td>

MacBook Pro

</td><td>

Outlook overview. **Note:** Here, no context is applied.

</td></tr></tbody>
</table>## Sentiment analysis in responses

The system detects the emotional tone in the user's description and incorporates this sentiment in the response. When the user expresses frustration or urgency, Now Assist for ITSM acknowledges the concern in the response. For example, if the user types `I am frustrated. My laptop is broken`, the response begins with `I understand your frustration with your broken MacBook Pro` and returns solutions in order of relevance.

