---
title: Create the Initiate transaction tracking guidance
description: Create the Initiate transaction tracking guidance by configuring inputs, outputs, preview experience and detail experience.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Example configuration of a decision tree, Guided Decisions configuration, Agent tools, Organize agent workspaces, Configure, Customer Service Management]
---

# Create the Initiate transaction tracking guidance

Create the Initiate transaction tracking guidance by configuring inputs, outputs, preview experience and detail experience.

## Before you begin

Role required: sn\_gd\_guidance.guidance\_manager

## Procedure

1.  Navigate to **All** &gt; **Guided Decisions** &gt; **Guidances**.

2.  Create a guidance.

    1.  Select **New** in the Guidances list.

    2.  In the **Name** field, enter `Initiate transaction tracking`.

    3.  In the **Description** field, enter `Guidance for tracking the failed credit card transaction`.

3.  Create the following inputs for the guidance.

    Inputs are the variables or information that the system needs to perform the guidance. You can use inputs in multiple places such as the guidance preview experience and the guidance actions.

    1.  In the Guidance Input tab, select **New** for each input.

    2.  Create the following inputs and select **Submit**.

        |Label|Type|Reference|Order|Is form field|
        |-----|----|---------|-----|-------------|
        |Cardholder name|String|-|100|true|
        |Task|Reference|Case|200|false|
        |Credit card number|Integer|-|300|true|
        |Transaction ID|Integer|-|400|true|
        |Date and time of transaction|Date/time|-|500|true|

4.  Create an output for the guidance.

    Outputs are the desired result of the guidance action. For example, if a guidance action creates a case task, the output of that action can return a reference to the case task that was created.

    1.  In the Guidance Output tab, select **New**.

    2.  In the **Label** field, enter `Case number for transaction tracking`.

    3.  In the **Type** field, select Reference.

    4.  In the **Reference** field, select the Case table.

    5.  Select **Submit**.

5.  Configure the preview and detail experiences.

    For more information, see [Configure guidance detail experience](configure-guidance-preview-detail-experiences-ga.md).

6.  Select **Submit**.


## What to do next

[Configure a guidance action](create-guidance-action-ga-use-case.md) that an agent can take while initiating transaction tracking.

