---
title: Add a risk and its control measures for a safety risk assessment
description: For a risk assessment, add an identified risk and choose control measures to assess how they impact and mitigate the risk.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/employee-service-management/health-and-safety-risk-management/add-a-risk-and-its-controls-for-a-safety-risk-assessment.html
release: xanadu
product: Health and Safety Risk Management
classification: health-and-safety-risk-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Safety risk assessment, Use, Health and Safety Risk Management, Health and Safety, Employee Service Management]
---

# Add a risk and its control measures for a safety risk assessment

For a risk assessment, add an identified risk and choose control measures to assess how they impact and mitigate the risk.

## Before you begin

Role required: sn\_hs\_rm.risk\_assessment\_manager or sn\_hs\_rm.risk\_assessment\_writer

## Procedure

1.  Navigate to **All** &gt; **Health and Safety** &gt; **Health and Safety Workspace**.

2.  Select the risk management icon \(\[Omitted image "icon-risk-assessment.png"\] Alt text: Risk assessment icon\).

3.  Select the **Risk assessment** list and then **All**.

4.  Open the risk assessment to add the risk and control.

5.  In the **Risks and controls** tab, select **New**.

6.  On the form, fill in the fields.

    1.  Select a hazard to perform its assessment and choose the severity and likelihood of this hazard.​

    2.  If this risk assessment is for a pre-defined job in the job register, select the job and the applicable job step.

        For more information on job register, see [Jobs in job register](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/employee-service-management/health-and-safety-risk-management/hs-define-job-register.md).

    3.  Identify what effect this hazard could have, for example, burns, and enter what control measures could help prevent this hazard.​

    4.  Choose what the severity and likelihood of this hazard is, after those controls have been put in place.

7.  Select **Import hazards and controls** to import hazards and controls from a pre-defined job and assess their risk levels.

    For more information, see [Import hazards and controls from a job](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/employee-service-management/health-and-safety-risk-management/import-hazards-and-controls.md).

8.  Select **Save**.


## Result

-   The risk matrix of the associated risk assessment evaluates the risk level for the hazard.

    -   The severity and likelihood of the hazard before controls are evaluated to show the hazard's risk level in the **Risk before controls** field in the form header.
    -   The severity and likelihood of the hazard after controls are evaluated to show the hazard's risk level in the **Risk after controls** field in the form header. After controls, the risk level should be reduced.
    \[Omitted image "hs-risk-controls-form-header.png"\] Alt text: Risk and controls form header showing Risk level fields

    For more information on risk level calculation, see [Risk matrix form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/employee-service-management/health-and-safety-risk-management/hs-risk-matrix-form.md).

-   The risk and controls record is listed in the **Risks and controls** tab of the assessment.

## What to do next

If a risk assessment includes more than one hazard, create a risk and controls record for each.

**Parent Topic:**[Safety risk assessment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/employee-service-management/health-and-safety-risk-management/hs-risk-assessment.md)

