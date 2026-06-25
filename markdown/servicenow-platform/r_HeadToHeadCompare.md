---
title: Assessment scorecard head-to-head compare view
description: The Head to Head Compare view allows you to compare the ratings of two assessable records of the same type. Select an assessable record from the choice list to compare against the current record's trailing twelve month \(TTM\) ratings.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/r\_HeadToHeadCompare.html
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [View an assessment scorecard, Assessment administrator tasks, Using assessments, Assessments, Assessments and Surveys, Exploring Service Administration, Service Administration, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Assessment scorecard head-to-head compare view

The Head to Head Compare view allows you to compare the ratings of two assessable records of the same type. Select an assessable record from the choice list to compare against the current record's trailing twelve month \(TTM\) ratings.

## Head to head compare

The Diff column displays the difference between each assessable record's most recent TTM ratings. By default, the system selects the first assessable record in the list when you open this view. The scorecard displays three years of ratings for the comparison record. All ratings are expressed as averages.

\[Omitted image "ScorecardHeadToHeadCompare.png"\] Alt text:

## Overall Rating

The Overall Rating is calculated as:

```
(sum of normalized values in category result) / (number of assessment groups)
```

In the following example, the calculation is

```
(2.13 + 2.86 + 3.79 + 1.43 + 2.39 + 3.7) / 2 = 8.15
```

\[Omitted image "RatingWeight.png"\] Alt text: Assessment category result normalized values

\[Omitted image "OverallRatingExample.png"\] Alt text: Overall rating on the group scorecard

**Parent Topic:**[View an assessment scorecard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/t_ViewAnAssessmentScorecard.md)

**Related topics**  


[Create a link to a scorecard]()

[Assessment scorecard averages]()

[Assessment scorecard categories]()

[Assessment scorecard category metrics]()

[Assessment scorecard history]()

[Live feed view of assessable records]()

[Assessment scorecard ratings]()

