---
title: Normalized value and application score for an assessment
description: If the source of the indicator is Assessments in the Data source field, then the Target maximum, Target minimum, Application weight, and Total weight values are considered as zero.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Job schedule to compute application scores, Application assessment, Explore, Enterprise Architecture \(formerly Application Portfolio Management\), Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# Normalized value and application score for an assessment

If the source of the indicator is **Assessments** in the **Data source** field, then the Target maximum, Target minimum, Application weight, and Total weight values are considered as zero.

For a business application to be considered for scoring, it must be mapped to a respective application profile to which the indicator is associated. You can check the scoring profiles in the apm\_application\_profile list.

All the business application related Assessment Category Results having assessment groups created within a fiscal period are considered for calculating the score. You can check the assessment category results for a business application in the asmt\_category\_result list.

For an assessment group to be considered for computing scores, all the related assessment instances must be either in completed or cancelled state.

```
scaleFactor = (9/ scale factor on metric type)
```

```
appAsmtScoreSUM = SUM of ratings of category results groupedBY source for each assessment group
```

```
appWeight=((scaleFactor * appAsmtScoreSUM )+1;
```

```
Normalized value = total app weight of BA/appOccurences.
```

```
totalIndicatorsWeightage = the sum of all indicator weightage mapped to a scoring profile.
```

```
appIndWeightage = weightage of the current indicator
```

```
Indicator Score = normalizedValue * appIndWeightage / totalIndicatorsWeightage
```

The app occurrence is the occurrences of a business application.

**Parent Topic:**[Job schedule to compute application scores](job-run-compute-application-scores.md)

