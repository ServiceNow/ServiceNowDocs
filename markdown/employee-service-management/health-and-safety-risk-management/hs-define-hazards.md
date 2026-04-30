---
title: Define Health and Safety hazards
description: Identify and define potential workplace hazards related to a job or task type. Maintain a list of all hazards for all job types in your organization.
locale: en-US
release: xanadu
product: Health and Safety Risk Management
classification: health-and-safety-risk-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure settings, Health and Safety Risk Management, Health and Safety, Employee Service Management]
---

# Define Health and Safety hazards

Identify and define potential workplace hazards related to a job or task type. Maintain a list of all hazards for all job types in your organization.

## Before you begin

Role required: sn\_hs\_rm.jsa\_manager or sn\_hs\_rm.risk\_data\_manager

## About this task

Review and update your hazard list regularly to verify its continued effectiveness.

## Procedure

1.  Navigate to **All** &gt; **Health and Safety** &gt; **Health and Safety Workspace**.

2.  Select the configuration icon \(![Configuration icon](../image/icon-config.png)\).

3.  In the **Configuration** tab, select **Hazards** and then **All**.

4.  Create a hazard or modify an existing one.

    -   To create a hazard, select **New**.
    -   To review an existing hazard, open the one that you want to configure.
5.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Risk category|Name of the risk category under which this hazard is organized. The list in this field displays items from the Risk category \[sn\_hs\_rm\_risk\_category\] table.|
    |Job location|Job or task location where this job and the associated risks may arise or exists.|
    |Active|Option to mark this hazard available for use. A hazard must be active to be used.|

6.  Select **Save**.

7.  Add all hazards that are possible for a job and location.


## Result

-   The hazard is listed in the **Hazards** list under **Configuration** and is saved in the Hazard \[sn\_hs\_rm\_hazard\] table.
-   The hazard is available to select in the following fields:
    -   **Hazard** field on the Hazard and controls form when defining a job in the job register.
    -   **Add hazards** window on a JSA form.
    -   **Hazard** field on the Risk and controls form when conducting a risk assessment.

**Parent Topic:**[Setting up Health and Safety Risk Management](../concept/hs-setting-up-risk-mgmt.md)

