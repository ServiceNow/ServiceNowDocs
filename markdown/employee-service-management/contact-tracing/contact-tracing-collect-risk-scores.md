---
title: Collecting risk scores in Contact Tracing
description: Identify at-risk and potentially exposed users by importing and monitoring risk scores from their wearable devices and external systems.
locale: en-US
release: zurich
product: Contact Tracing
classification: contact-tracing
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Contact Tracing, Safe Workplace, Health and Safety, Employee Service Management]
---

# Collecting risk scores in Contact Tracing

Identify at-risk and potentially exposed users by importing and monitoring risk scores from their wearable devices and external systems.

Use risk scores to identify at-risk and potentially exposed users by integrating the Devvio DevvTrace platform. Create cases to investigate potentially exposed or infected users based on their scores.

The Devvio DevvTrace platform collects data from supported wearable devices and generates a risk score. Use Contact Tracing and the Devvio API to import data into the Devvio Users Risk Reports \[sn\_imt\_tracing\_devvio\_users\_risk\_report\] table. You can use this data in the following ways:

-   Update the Devvio Users Risk Reports table daily with the Devvio Integration scheduled job.
-   Create cases and work notes automatically if a risk score is equal to or greater than a risk threshold value.
-   Examine the Daily Risk Scores for Devvio users report to analyze daily trends. The indicator source for use in Performance Analytics is Devvio.Users.Risk.Report.

-   **[Configure Devvio integration](../task/configure-devvio-integration.md)**  
Configure Contact Tracing properties to import risk scores from the DevvTrace platform using the Devvio API.

**Parent Topic:**[Contact Tracing](contact-tracing.md)

