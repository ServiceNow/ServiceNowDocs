---
title: Assessment scorecard head-to-head compare view
description: The Head to Head Compare view allows you to compare the ratings of two assessable records of the same type. Select an assessable record from the choice list to compare against the current record's trailing twelve month \(TTM\) ratings.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [View an assessment scorecard, Assessment administrator tasks, Use, Assessments, Assessments and Surveys, Exploring Service Administration, Service Administration, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Assessment scorecard head-to-head compare view

The Head to Head Compare view allows you to compare the ratings of two assessable records of the same type. Select an assessable record from the choice list to compare against the current record's trailing twelve month \(TTM\) ratings.

## Head to head compare

The Diff column displays the difference between each assessable record's most recent TTM ratings. By default, the system selects the first assessable record in the list when you open this view. The scorecard displays three years of ratings for the comparison record. All ratings are expressed as averages.

![](../images/ScorecardHeadToHeadCompare.png "Scorecard head to head compare")

## Overall Rating

The Overall Rating is calculated as:

```
(sum of normalized values in category result) / (number of assessment groups)
```

In the following example, the calculation is

```
(2.13 + 2.86 + 3.79 + 1.43 + 2.39 + 3.7) / 2 = 8.15
```

![Assessment category result normalized values](../images/RatingWeight.png "Normalized values")

![Overall rating on the group scorecard](../images/OverallRatingExample.png "Overall Rating on the group scorecard")

**Parent Topic:**[View an assessment scorecard](../task/t_ViewAnAssessmentScorecard.md)

**Related topics**  


[Create a link to a scorecard](../task/t_CreateALinkToAScorecard.md)

[Assessment scorecard averages](r_Averages.md)

[Assessment scorecard categories](r_Categories.md)

[Assessment scorecard category metrics](r_CategoryMetrics.md)

[Assessment scorecard history](r_History.md)

[Live feed view of assessable records](r_LiveFeed.md)

[Assessment scorecard ratings](r_Ratings.md)

