---
title: Configure the tolerance for Maintain constant targets
description: Set the tolerance percentage for Maintain constant targets to define the range of acceptable actual values and control how progress and status are calculated.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-business-management/goal-framework/configure-maintain-constant-tolerance.html
release: brazil
product: Goal Framework
classification: goal-framework
topic_type: task
last_updated: "2026-09-30"
reading_time_minutes: 1
keywords: [Maintain constant, tolerance, sn\_gf.maintain\_constant\_tolerance\_percent]
breadcrumb: [Configure, Goal Framework and Goal Framework for SPM, Strategic Portfolio Management]
---

# Configure the tolerance for Maintain constant targets

Set the tolerance percentage for Maintain constant targets to define the range of acceptable actual values and control how progress and status are calculated.

## Before you begin

Role required: sn\_gf.goal\_admin or admin

## About this task

A Maintain constant target is met for a period when the actual value is within the tolerance band around the planned target. The **sn\_gf.maintain\_constant\_tolerance\_percent** system property sets the tolerance percentage for all Maintain constant targets on the instance. The value is a whole number, and the default value is 5.

For example, with the default tolerance of 5 and a planned target of 50, actual values from 47.5 through 52.5 meet the target. For more information, see [Target types and achievement strategies](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/goal-framework/target-types-gf.md).

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **System Properties**.

2.  Search for and open the **sn\_gf.maintain\_constant\_tolerance\_percent** system property.

3.  In the **Value** field, enter the tolerance percentage as a whole number.

    For example, enter `10` for a tolerance of 10 percent.

4.  Select **Update**.


## Result

The new tolerance is used the next time progress is calculated for each Maintain constant target, for example, when an actual value is entered or changed. Progress that was already calculated is not recalculated until then.

**Parent Topic:**[Configuring Goal Framework and Goal Framework for SPM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/goal-framework/configuring-goal-framework.md)

