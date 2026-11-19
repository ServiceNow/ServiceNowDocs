---
title: Reset a demand to Draft state
description: A demand can be moved back to Draft state, if required.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/it-business-management/demand-management/reset-demand-to-draft-state.html
release: yokohama
product: Demand Management
classification: demand-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Use, Demand Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Reset a demand to Draft state

A demand can be moved back to Draft state, if required.

## Before you begin

Role required: it\_demand\_manager

## About this task

A demand can be reset to Draft from the Completed, Approved, Screening, or Submitted states, or until an artifact such as a project, enhancement, defect, or change is created from it. The **Reset to Draft** option is unavailable if the demand is in the Qualified state.

## Procedure

1.  Navigate to **All** &gt; **Demand** &gt; **Demands** &gt; **All**.

2.  Open the required demand form.

3.  Click **Reset to Draft**.

    A confirmation message appears if there are:

    -   Active assessments pending with stakeholders, or
    -   Resource assignments are created for the demand
4.  Select the check box to re-plan the allocated resource plans that have no actual hours reported.

5.  Click **OK**.


## Result

-   The demand is moved to Draft state.
-   All the score values in **Assessment Data** tab are reset to default.
-   All active assessments for the demand are canceled. New assessments are triggered when the demand moves to the Screening state and if the **Assessment Required** field on the demand form is set to true.

**Parent Topic:**[Use Demand Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/it-business-management/demand-management/r_UsingDemandManagement.md)

**Related topics**  


[Assess demands]()

[Create a demand]()

[View demands]()

[Add details to demands]()

[RIDACs records for a demand]()

[Delete demands]()

[Move and resize a demand]()

[Train the similarity solution for Demand Management to find similar demands]()

[PPM PIWB template - Find similar demands]()

[Identify similar records using ServiceNow Otto for Strategic Portfolio Management]()

