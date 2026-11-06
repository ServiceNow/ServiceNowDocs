---
title: Configure success score rating
description: Configure the score ranges, colors, and text that the Change Success Score card displays for each success score rating.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-service-management/change-management/change-success-score-rating.html
release: australia
product: Change Management
classification: change-management
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Change success score, Configure, Change Management, IT Service Management]
---

# Configure success score rating

Configure the score ranges, colors, and text that the Change Success Score card displays for each success score rating.

## Before you begin

Role required: admin

The following default ratings are available.

-   Low
-   Medium
-   High
-   Excellent

**Tip:** Score ratings map a calculated score range to a color and text. They don't define how the score itself is computed. For the success score formula and the default multipliers applied to each automated indicator, see [Success score calculation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/change-management/change-score-calculation.md).

Each rating is associated with a default range and color.

The Change Success Score Ratings table stores the text and color associated with each success score range.

You can modify the score range and color of a rating, or add new ratings. These values appear on the **Change Success Score** card on the Change Request form.

**Note:** The change success score feature is installed after you activate the Change Management - Change Success Score plugin available with the ITSM Professional subscription only. Contact your account manager for more information.

\[Omitted image "change-success-score-tokyo.png"\] Alt text: Change Success Score card

## Procedure

1.  Navigate to **All** &gt; **Change** &gt; **Administration** &gt; **Change Success Score Ratings**.

2.  Perform one of the following actions.

    |Action|Procedure|
    |------|---------|
    |**To add a new score range**|Select **New**, enter the range details and the associated color, and select **Submit**.|
    |**To modify the existing range**|Open the rating, and select the **here** link in the record information message to modify the values.|

3.  Select **Update**.


**Parent Topic:**[Change success score](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/change-management/change-success-score.md)

**Related topics**  


[Success score calculation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/change-management/change-score-calculation.md)

[Modify score calculation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/change-management/modify-success-score-calculations.md)

[Change success score](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/change-management/change-success-score.md)

