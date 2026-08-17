---
title: Project form
description: Learn about the fields on the Project form. Use this form to create or edit a project from the Execute page in AI Control Tower.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/aict-plan-project-form.html
release: zurich
topic_type: reference
last_updated: "2026-04-28"
reading_time_minutes: 5
keywords: [project form, project fields, AI Plan, Execute]
breadcrumb: [Reference, Plan AI strategy, prioritize, and execute, Plan your AI strategy, AI Control Tower, Enable AI experiences]
---

# Project form

Learn about the fields on the Project form. Use this form to create or edit a project from the Execute page in AI Control Tower.

The Project form contains the following fields.

|Field|Description|
|-----|-----------|
|Project name|Name of the project. This field is required.|
|Number|System-generated unique identifier for the project. This value is set automatically.|
|Project manager|User responsible for managing this project.|
|Assigned to|User assigned to this project.|
|Status|Overall health status of this project.|
|Assignment group|Group assigned to this project.|
|State|Current working state of this project. The default value is Pending.|
|Additional assignee list|Additional users assigned to this project.|
|Percent complete|Percentage of work completed for this project. This value is calculated automatically.|
|Description|Detailed information about the project.|

|Field|Description|
|-----|-----------|
|Schedule|Project schedule template applied to this project. This value is set automatically.|
|Approved start date|Approved start date for this project.|
|Approved end date|Approved end date for this project.|
|Planned duration|Planned duration for this project in days, hours, minutes, and seconds.|
|Actual duration|Actual duration of this project in days, hours, minutes, and seconds. This value is calculated automatically.|
|Planned effort|Planned effort for this project in days, hours, minutes, and seconds.|
|Actual effort|Actual effort recorded for this project in days, hours, minutes, and seconds. This value is calculated automatically.|

|Field|Description|
|-----|-----------|
|Portfolio|Portfolio that this project is associated with.|
|Priority|Priority of this project. The default value is 4 - Low.|
|Program|Program that this project is associated with.|
|Phase|Current phase of this project. The default value is **Initiating**.|
|Investment class|Investment class that this project is categorized under.|
|Department|Department associated with this project.|
|Investment type|Type of investment that this project represents. For projects created from the Execute page, this field is set to Artificial Intelligence.|
|Business unit|Business unit associated with this project.|
|Execution type|Delivery methodology for this project. Select from **Waterfall**, **Agile**, or **Hybrid**. The default value is Waterfall.|
|Impacted business units|Business units that this project has an impact on.|
|Expense type|Expense type for this project. The default value is Opex.|
|Business capabilities|Business capabilities associated with this project.|
|Impacted business applications|Business applications that this project has an impact on.|

|Field|Description|
|-----|-----------|
|Strategic priority|Strategic priority associated with this project. This value is populated automatically based on the primary goal.|
|Primary goal|Goal associated with this project as the primary goal.|
|Business case|Business case to invest in this project.|
|Risk of performing|Risks to the business if work on this project is completed.|
|Risk of not performing|Risks to the business if work on this project isn't completed.|
|Enablers|Enablers for this project.|
|Barriers|Blockers, if any, for this project.|
|In scope|Defined criteria that are included in this project.|
|Out of scope|Criteria that are explicitly excluded from this project.|
|Assumptions|Assumptions, if any, for this project.|

|Field|Description|
|-----|-----------|
|Total planned cost|Total planned cost for this project.|
|Planned benefit|Planned benefit from this project.|
|Planned capital|Planned capital expenditure for this project.|
|Planned return|Planned financial return on this project.|
|Planned operating|Planned operating expenditure for this project.|
|Planned ROI %|Planned return on investment percentage for this project.|
|Budget cost|Approved budget for this project.|
|Discount rate %|Discount rate used to calculate the net present value of this project.|
|Actual cost|Actual cost incurred on this project.|
|Net present value|Net present value of this project, calculated using the discount rate. This value is calculated automatically.|
|Estimate at completion|Estimated total cost at the time work on this project is completed.|
|Internal rate of return %|Internal rate of return for this project. This value is calculated automatically.|
|Estimate to completion|Estimated remaining cost to complete this project.|

|Field|Description|
|-----|-----------|
|Risk score|Score for the risk associated with this project.|
|Size score|Score for the effort required to complete this project.|
|Value score|Score for the value delivered by this project.|
|Score|Overall score for this project, calculated from the risk, value, and size scores.|

|Field|Description|
|-----|-----------|
|Watch list|Users who receive notifications about activity on this project.|
|Work notes list|Users who receive notifications when work notes are added.|
|Work notes|Notes to capture updates and discussions on this project as work progresses.|

|Field|Description|
|-----|-----------|
|Allow time card reporting on|Level at which time cards can be reported for this project. Select from project only or project and project tasks.|
|Derive assignee list from resource plan|Option to automatically populate the assignee list from the resource plan associated with this project.|
|Update actual effort from time card|Option to update the actual effort on this project automatically from submitted time cards.|
|Recalculate score on project change|Option to recalculate the project score automatically when project details change.|
|Calculation|Method used to calculate project progress. The default value is Automatic.|
|Project schedule date format|Format used to display dates in the project schedule.|
|Show on Program Status Report|Option to include this project in the Program Status Report.|
|Derive time component from planned dates|Option to derive the time component of duration fields from the planned dates.|
|Constraint date|Date constraint applied to the project schedule.|

|Field|Description|
|-----|-----------|
|Inherent risk|Risk level of this project before any controls or mitigations are applied. Select **Inherent Heatmap** to view the risk distribution.|
|Residual risk|Risk level of this project after controls and mitigations are applied. Select **Residual Heatmap** to view the risk distribution.|

**Related topics**  


[Monitoring AI plan execution in AI Control Tower](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/aict-plan-execute.md)

