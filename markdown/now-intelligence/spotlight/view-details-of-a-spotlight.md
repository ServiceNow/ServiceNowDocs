---
title: See Spotlight score details
description: To see the criteria whose weights contributed to a Spotlight score, view the details of the Spotlight record.
locale: en-US
release: yokohama
product: Spotlight
classification: spotlight
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Ranking records with Spotlight, Configure Performance Analytics advanced features, Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# See Spotlight score details

To see the criteria whose weights contributed to a Spotlight score, view the details of the Spotlight record.

## Before you begin

Role required: pa\_spotlight or admin

## Procedure

1.  Navigate to **All** &gt; **Spotlight** &gt; **Spotlight** or view the **Spotlights** related list in a Spotlight Group record.

2.  Locate the Spotlight that interests you and click the information icon ![](../../common-ui-elements/image/PreviewIcon.png).

3.  Click **Open Record**


## Result

The Spotlight record opens. In the Spotlight Audits related list, you can see which Spotlight criteria the record met and the contribution of each criterion to the total score.

## Spotlight criteria contributing to total score

Consider the Spotlight record for Incident INC0006831, which had a Spotlight score of 1,200 against a threshold of 1,000.

![The Spotlights list showing the preview of the Spotlight for Incident INC0006831](../image/spotlight-record-entry.png "Spotlights list with selected record")

Opening the Spotlight record, you see that the following criteria weights contributed to the total score:

|Criteria|Weight|
|--------|------|
|Open incidents not updated 30 days|1,000|
|Incidents older than 28 days|25|
|Incidents older than 7 days|25|
|Open incidents not updated 5 days|100|
|Incidents older than 14 days|25|
|Incidents older than 90 days|25|
|TOTAL SCORE:|1,200|

**Parent Topic:**[Ranking records with Spotlight](../concept/spotlight.md)

