---
title: Job schedule to compute application scores
description: After you set up assessment indicators and scoring profiles, application scores are calculated by a scheduled job. Enterprise Architecture provides a predefined scheduled job that periodically recalculates application scores based on the assigned scoring profiles. An administrator can review or adjust the schedule from the Scheduled Jobs list if needed.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Application assessment, Explore, Enterprise Architecture \(formerly Application Portfolio Management\), Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# Job schedule to compute application scores

After you set up assessment indicators and scoring profiles, application scores are calculated by a scheduled job. Enterprise Architecture provides a predefined scheduled job that periodically recalculates application scores based on the assigned scoring profiles. An administrator can review or adjust the schedule from the Scheduled Jobs list if needed.

Understand how the system calculates application scores and create your application score profile per your requirements.

The assessment framework [calculates the application score for each application](application-score-profile.md) on a scale of 1–10, where 10 is a good score and 1 is a low score. Assessments are based on various configured indicators, which you can configure. Each of these indicators periodically captures the related application data, which is used to derive the application score. These indicators with their respective value \(weightage\) are added to an application profile. The application is then associated with the application profile, which calculates the application score.

-   **[Normalization of application scores](application-score-profile.md)**  
The indicators and their respective weights are used to calculate application score profiles for each configuration item. Use the score profile to calculate application scores and assess the applications. Apply these scores to compare applications and make strategic decisions about which ones to keep, replace, maintain, or invest more in.
-   **[Normalized value and application score for an assessment](nv-and-app-score-for-assessments.md)**  
If the source of the indicator is **Assessments** in the **Data source** field, then the Target maximum, Target minimum, Application weight, and Total weight values are considered as zero.

**Parent Topic:**[Application assessment](application-assessment.md)

**Related topics**  


[Framework setup for application assessment](applications-assessment-overview.md)

[Visualization of application performance](visualization-application-performance.md)

