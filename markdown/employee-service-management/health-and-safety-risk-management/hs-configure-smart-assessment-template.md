---
title: Configure the smart assessment template for safety inspections and audits
description: You can create smart assessment templates and add instructions, questions, and reference information by using the template designer in the Smart Assessment Engine application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/employee-service-management/health-and-safety-risk-management/hs-configure-smart-assessment-template.html
release: yokohama
product: Health and Safety Risk Management
classification: health-and-safety-risk-management
topic_type: task
last_updated: "2026-01-12"
reading_time_minutes: 1
breadcrumb: [Configure settings, Health and Safety Risk Management, Health and Safety, Employee Service Management]
---

# Configure the smart assessment template for safety inspections and audits

You can create smart assessment templates and add instructions, questions, and reference information by using the template designer in the Smart Assessment Engine application.

## Before you begin

-   Smart assessments are built using the ServiceNow® Smart Assessment Engine \(SAE\) application. Familiarize yourself with the .
-   Verify that the application scope is selected as Health and Safety Risk Management. For more information, see Application picker.

Role required: sn\_hs\_rm.safety\_inspection\_manager or sn\_hs\_rm.safety\_audit\_manager

## About this task

You can also convert your existing Survey templates related to Health and Safety into Smart Assessment templates using the Smart Assessment Engine migration tool. For more information, see .

## Procedure

1.  Navigate to **All** &gt; **Health and Safety** &gt; **Health and Safety Workspace**.

2.  Select the **Workspaces** tab and then select the **Assessment workspace**.

    For more information on creating the smart assessment template, see .

3.  In the **Purpose** field on the **Smart assessment template** form, select **Health and Safety**.

    You can also configure a category role for a specific purpose. For more information, see .

4.  In the **Assessment target** field on the **Smart assessment template** form,

    -   For smart assessment for inspections, select the Inspection \[sn\_hs\_rm\_inspection\] table
    -   For smart assessment for audits, select the Audit survey \[sn\_hs\_rm\_audit\_survey\] table.
5.  Select **Create**.


## What to do next

You can configure which question in the smart assessment should have action creation enabled. For more information, see [Configure creating actions from smart assessment questionnaire](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/employee-service-management/health-and-safety-risk-management/hs-configure-property-smart-assessment-action-creation.md).

**Parent Topic:**[Setting up Health and Safety Risk Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/employee-service-management/health-and-safety-risk-management/hs-setting-up-risk-mgmt.md)

