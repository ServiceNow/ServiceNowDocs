---
title: Define third-party risk area criteria
description: A third-party risk area criteria is a group of risk domains \(sometimes called risk areas in other platform features\) that applies to a particular type of third party.
locale: en-US
release: xanadu
product: Third-party Risk Management
classification: third-party-risk-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Classic assessments, Configure, Third-party Risk Management, Governance, Risk, and Compliance]
---

# Define third-party risk area criteria

A third-party risk area criteria is a group of risk domains \(sometimes called risk areas in other platform features\) that applies to a particular type of third party.

## Before you begin

Role required: sn\_vdr\_risk\_asmt.vendor\_risk\_manager

## About this task

This is an example of the group of risk domains that you include in a risk area criteria that you might apply to IT service providers.

**Note:** Risk domains are called "risk areas" in some platform applications.

![A group of risk areas included in a risk area criteria.](../image/vendor-risk-area-criteria-related.png)

## Procedure

1.  Navigate to **All** &gt; **Third-party Risk Management** &gt; **Scoring Setup** &gt; **Risk Domain Criteria**.

2.  Select **New**, enter a **Name** and **Description**, and then save the record.

    The Third-party Risk Areas related list appears. In the following steps, you specify the risk areas to include in the risk area criteria.

3.  On the Third-party Risk Areas related list, select **Edit**.

4.  On the Edit Members page, select the third-party risk areas to add to the third-party risk area criteria record and then select **Save**.

    -   The selected third-party risk areas appear in the Third-party Risk Areas related list.
    -   Scoring method and weight are copied from the risk areas.
    -   You can adjust the weight of each risk area within a criteria definition.
    -   You can override the values when needed.
5.  To edit **Scoring method** and **Weight**, select the name of a third-party risk area.

    **Important:** Changes to the scoring method and weight are used for the third-party risk area criteria record but aren’t saved in the individual risk area definition records.

    ![Third-party risk areas are added to the criteria.](../image/vrm-tpr-area-set-scoring.png)


## Example

Assume you’re creating a third-party risk area criteria with two risk areas: Financial and Security. Financial has a scoring method of Min Risk and a weight of 10.

-   Your company is more concerned with security-related criteria, so the Security risk area has a scoring method of Average Risk and a weight of 20.
-   The weights for both risk areas add up to 30. Resulting in the risk area with a weight of 10 calculating as 10/30 or roughly 33%.
-   The risk area with a weight of 20 calculates as 20/30 or roughly 66%.
-   If both risk areas had a weight of 10, they would each carry a weight of 50%.

