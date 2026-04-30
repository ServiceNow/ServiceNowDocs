---
title: Contextual based discovery
description: Use contextual based discovery to help discover sensitive data that does not follow fixed patterns.
locale: en-US
release: zurich
product: Data Discovery
classification: data-discovery
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Exploring Data Discovery \(Classic\), Data Discovery, Platform Privacy]
---

# Contextual based discovery

Use contextual based discovery to help discover sensitive data that does not follow fixed patterns.

Data Discovery supports using a Named Entity Recognition \(NER\) model to discover data such as names, organizations, nationalities, and political affiliations. Data patterns with the type **Model** use this feature, see pattern type in [Configure Data Discovery patterns](../task/configure-data-discovery-patterns.md) for more details.

**Warning:** This feature requires a license check from the customer before it is enabled.

AI model-based discovery supports 5 patterns by default.

|Pattern|Description|Example text|Matching text|
|-------|-----------|------------|-------------|
|Person|The name of individual\(s\)|John Doe came by for a coffee.|John Doe|
|Nationality, religious or political groups \(NRPs\)|National, religious and political affiliations.|He was an American.|American|
|Location|Addresses or location information|He was in New York|New York|
|Date\_Time|Dates and time information|He came at 9:30 today.|9:30 today|
|Organization|Organization names|He works at ServiceNow.|ServiceNow|

**Note:** AI Model-based discovery is only supports English for use with [Real time anonymization](../../data-privacy-store/concept/real-time-anonymization.md)\(RTA\) for tables and the [Data Kit channel](configure-now-assist-data-privacy.md).

