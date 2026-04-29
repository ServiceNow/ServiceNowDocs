---
title: Security hardening
description: View your hardening compliance score, compare it with previous scores, and change settings to improve your compliance score and security posture in the security hardening page.
locale: en-US
release: australia
product: Security Center
classification: security-center
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Security configuration console, Security Center, Platform Security]
---

# Security hardening

View your hardening compliance score, compare it with previous scores, and change settings to improve your compliance score and security posture in the security hardening page.

![Hardening score comparison page](../images/sec-center-hardening.png)

[Hardening settings](../reference/security-hardening-settings.md) specify recommended values for the security-related properties and plugins in the ServiceNow AI Platform. The hardening tool calculates the hardening setting compliance score as a percentage. This number indicates how compliant your instance is with the Security Center hardening settings.

The formula for calculating the hardening compliance score:

-   Each hardening setting has a risk score between 0-10. You can see the values of individual settings in the **All settings** section.
-   The score equals the sum of all the compliant risk scores divided by the sum of all risk scores.

For example, the sum of all the compliant risk scores is 25.4, and the total for all risk scores is 34.9. For this sum, the compliance score is \(25.4 /34.9\) × 100 which equals 72.7. This decimal gets rounded up to the nearest whole number and will therefore be equal to 73.

This calculation is automatically performed on the first of the month, or after an installation or reinstallation of ServiceNow Security Center. You can trigger a recalculation at any time using the **Update score** button on this page.

## Security hardening subsections

The security hardening section contains three subsections that you can select on the left edge of the screen.

-   [All settings](all-settings.md)
-   [Hardening compliance score trend](score-trend.md)
-   [Hardening score comparison](hardening-score-comparison.md)

-   **[All settings](all-settings.md)**  
Review all of your instance hardening settings available from a single page.
-   **[Hardening compliance score trend](score-trend.md)**  
View the trends of your hardening compliance score over time in a chart or table.
-   **[Hardening score comparison](hardening-score-comparison.md)**  
Gain visibility to the health of your hardening settings and use this data to improve the security posture of your instance.

**Parent Topic:**[Security configuration console](homepage.md)

