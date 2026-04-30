---
title: Configure a resource generator for providing a similar major case to the current case
description: Configure a resource generator of type similarity with trend that provides a similar major case to the current case.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Example: Link the similar major case to the current case, Example configurations of recommended actions, Recommended Actions configuration, Implement Intelligence, Configuring Customer Service Management, Customer Service Management]
---

# Configure a resource generator for providing a similar major case to the current case

Configure a resource generator of type similarity with trend that provides a similar major case to the current case.

## Before you begin

-   Ensure Predictive Intelligence is active and set up on your instance. See [Install Predictive Intelligence](https://www.servicenow.com/docs/access?context=install-predictive-intelligence&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US).
-   Ensure you have a Predictive Intelligence subscription.
-   Train the Major issue detector similarity solution with the existing customer cases. For more information, see [Create and train a similarity solution](https://www.servicenow.com/docs/access?context=create-similarity-solution&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US).
-   Create a trend definition with the name Major issue trends to define how many records that have something in common constitute a trend, for example, six or more records with common field values.

Role required: sn\_nb\_action.next\_best\_action\_author, sn\_nb\_action.resource\_generator\_author, admin

## Procedure

1.  Navigate to **All** &gt; **Recommended Actions** &gt; **Resource Generators**.

2.  Select **New** from the Resource Generators list.

3.  In the **Name** field, enter `Similar major case`.

4.  In the **Context** field, select Case context.

5.  In the **Generator type** field, select Similarity with Trend.

6.  Save the record to display the generator inputs.

7.  On the Generator input form, fill in the fields.

    |Field|Action|
    |-----|------|
    |**Similarity definition**|Select the similarity solution, Major Issue Detector.|
    |**Trend definition**|Select the trend definition, Major issue trends.|

8.  Select **Update**.


