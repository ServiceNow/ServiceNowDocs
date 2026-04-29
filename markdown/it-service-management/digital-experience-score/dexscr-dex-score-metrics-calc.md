---
title: DEX Score metrics calculation
description: Learn more about how the metrics values are calculated in the Digital Experience Score​ dashboard.
locale: en-US
release: australia
product: Digital Experience Score
classification: digital-experience-score
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Reference, Digital Experience Score, Digital End-User Experience, IT Service Management]
---

# DEX Score metrics calculation

Learn more about how the metrics values are calculated in the Digital Experience Score​ dashboard.

## Calculating the digital experience score

Digital experience score is the weighted average of device experience score and application experience score for all employees. The formula used to calculate the digital experience score is:

-   **Formula**

    `Weighted Average = Sum of (Score * Weight) / Sum of Weights`

    where,

    -   Score: Device experience score and application experience score
    -   Weight: Weight given to each contributing factor's score
    This score is rounded off to the nearest whole number.

-   **Score range definition**

    The following defines the score range and its corresponding classification:

    -   Good if the score is greater than 75
    -   Average if the score is from 45 through 75
    -   Poor if the score is less than 45
-   **Example**

    Consider the following values for the contributing factors:

    -   Application experience: Score = 55 and Weight = 50
    -   Device experience: Score = 54 and Weight = 50
    Then the overall digital experience score is calculated as:

    Digital experience score = `(55x50 + 54x50)/ (50+50)` = 54


## Calculating the application experience score

Application experience score is calculated as the average of the experience scores of all the applications. The experience score of an individual application is calculated by combining three scores: application health metric, user sentiment, and service experience. Each of these scores is given a weight, and then they're averaged together. The formula for the application experience score is:

-   **Formula**

    `Weighted Average = Sum of (Score * Weight) / Sum of Weights`

    where,

    -   Score: Application health metrics score, user sentiment score, and service experience score
    -   Weight: Weight given to each contributing factor's score
-   **Score range definition**

    The following defines the score range and its corresponding classification:

    -   Good if the score is greater than 75
    -   Average if the score is from 45 through 75
    -   Poor if the score is less than 45
-   **Example**

    Consider the following values for the contributing factors:

    |Contributing factor|Score|Weight|
    |-------------------|-----|------|
    |Application health metrics|55/100|50|
    |User sentiment|58/100|30|
    |Service experience|72/100|20|

    Then the application experience score is calculated as:

    Application experience score = `(55x50 + 58x30 + 72x20) / (50+30+20)` = 59 \(rounded off\).


## Calculating the device experience score

Device experience score is calculated as the average of the experience scores of all the devices across all device groups. The experience score of an individual device is calculated by combining three scores: device health, user sentiment, and service experience. Each of these scores is given a weight, and then they're averaged together.  The formula for the device experience score is:

-   **Formula**

    `Weighted Average = Sum of (Score * Weight) / Sum of Weights`

    where,

    -   Score: Device health metrics score, user sentiment score, and service experience score
    -   Weight: Weight given to each contributing factor's score
-   **Score range definition**

    The following defines the score range and its corresponding classification:

    -   Good if the score is greater than 75
    -   Average if the score is from 45 through 75
    -   Poor if the score is less than 45
-   **Example**

    Consider the following values for the contributing factors:

    |Contributing factor|Score|Weight|
    |-------------------|-----|------|
    |Device health metrics|64/100|50|
    |User sentiment|68/100|30|
    |Service experience|70/100|20|

    Then the device experience score is calculated as:

    Device experience score = `(64x50 + 68x30 + 70x20) / (50+30+20)` = 66 \(rounded off\).


## Application experience metrics

|Metric|Description|
|------|-----------|
|Application health metrics score|An application's health metrics score is a weighted average of the normalized values of multiple metrics, including CPU usage, memory usage, and crash reports. These metrics are tracked across all relevant devices.|
|User sentiment score|An application's user sentiment score is the average of the normalized sentiment scores obtained from user feedback collected for that application.|
|Service experience score​|The service experience score​ for an application is the weighted ​average of​ normalized​ incident metric scores based on all the incidents resolved for the application.|

## Device experience metrics

|Metric|Description|
|------|-----------|
|Device health metrics score​|The device health metrics score​ for each device group is computed as the weighted average of all normalized metric scores of that device group.|
|User sentiment score|The user sentiment score​ for each device group is the average of the normalized sentiment scores. The scores are collected from user feedback for the devices in the group.|
|Service experience score​|The service experience score​ for each device group is the weighted ​average of​ normalized​ incident metric scores. The scores are based on all the incidents resolved for the devices in the group.|

**Parent Topic:**[Digital Experience Score​ reference](../concept/dexscr-dex-score-reference.md)

**Related topics**  


[Metric scores in Digital Experience Score​](../concept/dexscr-dex-score-defs.md)

[DEX Score normalization for metric scores](dexscr-dex-score-normalization.md)

