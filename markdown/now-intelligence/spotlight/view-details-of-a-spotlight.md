---
title: See Spotlight score details
description: To see the criteria whose weights contributed to a Spotlight score, view the details of the Spotlight record.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/now-intelligence/spotlight/view-details-of-a-spotlight.html
release: zurich
product: Spotlight
classification: spotlight
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Ranking records with Spotlight, Configure advanced features, Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# See Spotlight score details

To see the criteria whose weights contributed to a Spotlight score, view the details of the Spotlight record.

## Before you begin

Role required: pa\_spotlight or admin

## Procedure

1.  Navigate to **All** &gt; **Spotlight** &gt; **Spotlight** or view the **Spotlights** related list in a Spotlight Group record.

2.  Locate the Spotlight that interests you and click the information icon \[Omitted image "PreviewIcon.png"\] Alt text:.

3.  Click **Open Record**


## Result

The Spotlight record opens. In the Spotlight Audits related list, you can see which Spotlight criteria the record met and the contribution of each criterion to the total score.

## Spotlight criteria contributing to total score

Consider the Spotlight record for Incident INC0006831, which had a Spotlight score of 1,200 against a threshold of 1,000.

\[Omitted image "spotlight-record-entry.png"\] Alt text: The Spotlights list showing the preview of the Spotlight for Incident INC0006831

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

**Parent Topic:**[Ranking records with Spotlight](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/spotlight/spotlight.md)

