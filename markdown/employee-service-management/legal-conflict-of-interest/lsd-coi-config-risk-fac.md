---
title: Configure risk assessment
description: Configure the risk assessment to automatically evaluate conflict of interest disclosures and assign risk levels that determine approval routing.
locale: en-US
release: australia
product: Legal Conflict of Interest
classification: legal-conflict-of-interest
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, Legal Conflict of Interest, Legal Service Delivery Practice Applications, Legal Service Delivery, Legal and Contract Operations, Employee Service Management]
---

# Configure risk assessment

Configure the risk assessment to automatically evaluate conflict of interest disclosures and assign risk levels that determine approval routing.

## Before you begin

Role required: sn\_lco\_cmn.config

## About this task

The risk assessment functionality evaluates each request against a set of risk factors to calculate a risk score. The risk score determines the risk level \(Low, Medium, or High\), which drives the approval workflow. Low-risk disclosures are auto-approved; Medium and High-risk disclosures enter the approval workflow with approvers determined by the conflict type.

The risk assessment record defines the risk factors, the table it applies to, and the conditions under which it runs.

COI Risk Assessment is available in the base system to evaluate the COI requests. You can also configure risk assessments to evaluate other compliance requests.

## Procedure

1.  Set the application scope to **Global** or **Legal and Contracts Common Utilities** in the application picker.

    ![Set application scope to Global or Legal and Contract Common Utilities](../image/lsd-coi-application-picker.png)

2.  Navigate to **All** &gt; **Legal and Contracts Common Utilities** &gt; **Risk Assessment**.

3.  Select **New**.

4.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|The name of the risk assessment.|
    |Table|The table the assessment applies to.|
    |Active|Select the check box to activate the risk assessment.|
    |Application|Displays the application scope.|
    |Order|Execution order when multiple assessments exist. Lower numbers run first.|
    |Report template|Select a report template to generate risk assessment reports.|
    |Applies to|Conditions under which this assessment runs.|

5.  Right-click on the form header and select **Save**.

    The risk assessment is saved and the related list for Risk factors appear


## What to do next

Add risk factors to define the criteria the risk assessment functionality evaluates a request. For more information, see [Configure risk factors](lsd-coi-config-rsk-factors.md).

-   **[Configure risk factors](lsd-coi-config-rsk-factors.md)**  
Configure risk factors to define the criteria the risk assessment functionality evaluates a request. Each risk factor uses one of three evaluation types: Condition, Skill, or Subflow.

**Parent Topic:**[Configure Legal Conflict of Interest](../concept/legal-coi-administration.md)

