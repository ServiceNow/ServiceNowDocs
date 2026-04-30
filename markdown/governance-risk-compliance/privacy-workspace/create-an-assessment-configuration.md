---
title: Create and validate an assessment configuration
description: Create your assessment configurations to determine when a processing activity must be automatically created.
locale: en-US
release: yokohama
product: Privacy Workspace
classification: privacy-workspace
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure, Privacy Management, Governance, Risk, and Compliance]
---

# Create and validate an assessment configuration

Create your assessment configurations to determine when a processing activity must be automatically created.

## Before you begin

Role required: sn\_privacy.admin or sn\_privacy.manager

## About this task

When a privacy screening assessment is sent to the entity owners, their responses determine the creation of processing activity. You can also modify the default configurations on the privacy screening assessment to create processing activities automatically.

You can also create a new processing activity creation condition for your own privacy screening assessments.

After you create the configurations, you can validate if the responses create the processing activities according to the defined conditions.

## Procedure

1.  Navigate to **All** &gt; **Privacy Management** &gt; **Assessments** &gt; **Processing activity creation rules**.

2.  Click **New**.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name of the assessment configuration.|
    |Description|Brief description of the configuration.|
    |Assessment template|Template for which the configuration is being created.|
    |Active|Option to make the configuration active.|
    |Advanced|Option to add more than three conditions.|

4.  In the Conditions related list, create filters by selecting **Metric** and using the condition builder.

5.  In the Advanced related list, specify the script for adding more than three conditions.

    The Advanced related list only appears if you select the **Advanced** option.

6.  Click **Validate**.

    1.  In the **Assessment instance** field, select the instance on which this configuration must be used.

    2.  Click **Validate**.


**Parent Topic:**[Configuring Privacy Management](../concept/configure-privacy-mgmt.md)

