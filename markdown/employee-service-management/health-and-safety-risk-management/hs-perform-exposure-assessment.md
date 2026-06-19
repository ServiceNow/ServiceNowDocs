---
title: Perform an exposure assessment for a location
description: Perform an exposure assessment for an exposure type for each site location in your organization.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/employee-service-management/health-and-safety-risk-management/hs-perform-exposure-assessment.html
release: zurich
product: Health and Safety Risk Management
classification: health-and-safety-risk-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Safety exposure management, Use, Health and Safety Risk Management, Health and Safety, Employee Service Management]
---

# Perform an exposure assessment for a location

Perform an exposure assessment for an exposure type for each site location in your organization.

## Before you begin

Role required: sn\_hs\_rm.industrial\_hygienist or sn\_hs\_rm.exposure\_writer

## Procedure

1.  Navigate to **All** &gt; **Health and Safety** &gt; **Health and Safety Workspace**.

2.  Select the risk management icon \(\[Omitted image "icon-risk-assessment.png"\] Alt text: Risk management icon\).

3.  Select the **Exposure types** list and open the exposure type to perform the assessment for.

4.  In the **Exposure assessment** tab, select the record for the location that you want to perform the exposure assessment for.

5.  In the **Exposure creation conditions** field, add conditions to create exposure records for this assessment.

    The criteria defined in this field—particularly the measurement limit—trigger the creation of exposure records under the **Exposures** tab for this assessment. An exposure assessment might generate multiple exposures over time whenever the measurement limits exceed the defined criteria.

    1.  Select **Set conditions**.

    2.  In the condition builder, add criteria \(including the measurement condition\) and select **Set**.

        For example, the following image shows the measurement condition for noise exposure limits.

        \[Omitted image "hs-exposure-creation-conditions.png"\] Alt text: Exposure creation conditions with measurement limit set to greater than 100 and unit as dBA.

        **Note:** The measurement condition will only apply when a measurement record is created in the **Measurements** tab.

6.  In the **Affected people conditions** field, add conditions to see all the people affected from an exposure.

    This criteria is based on the Health and Safety profile \[sn\_ohs\_im\_health\_and\_safety\_profile\] table. It automatically adds or updates the affected people in the exposure records generated for this assessment.

    1.  Select **Set conditions**.

    2.  In the condition builder, define the conditions to identify people affected, and select **Set**.

        You can choose fields from the Health and Safety profile table and dot-walk fields when selecting a field in the condition builder. For example, the following image shows the conditions to identify people in the Warehouse department in Dublin who are affected by this exposure.

        \[Omitted image "hs-affected-people-conditions.png"\] Alt text: Affected people conditions showing location and dot-walked condition for user's department name

7.  In the **Action schedule** tab, set up actions for the affected people.

    The action schedule creates and auto-assigns an action for each affected person when there's an active exposure for this assessment. For more information, see [Define an action schedule for affected people](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/health-and-safety-risk-management/hs-define-action-schedule-affected-people.md).

8.  In the **Documents** tab, add any documents related to this assessment.

    -   Select **Add** to link an existing document stored in the **Health and Safety document library** list.
    -   Select **New** to upload a new document.
    For information on storing documents in the Health and Safety Workspace, see [Add a new Health and Safety related document](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/health-and-safety-core/add-hs-related-document.md).

9.  In the **Details** tab of the assessment, set the **State** as Active.

10. Select **Save**.

11. In the **Measurements** tab, add the exposure measurement value and the source of the exposure.

    For information on adding a measurement and creation of an exposure from it, see [Add a measurement and exposure source for an exposure assessment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/health-and-safety-risk-management/hs-add-measurement-exposure-assessment.md).


## Result

-   Based on the exposure creation conditions, affected people conditions, and the measurement value, the following records are created:
    -   An exposure is created and listed in the **Exposures** tab of the assessment.
    -   The affected people are added to the **Affected people** tab of the generated exposure record.
    -   The action scheduler runs for the active exposure and assigns actions to exposed people. The actions for each affected person are listed in the **Actions** tab under the action schedule.
-   If an active exposure is manually added to a Health and Safety user's profile, the user is also listed in the **Affected people** tab of the exposure record.
-   Any assigned actions appear in the affected people's **My Tasks** list in the Employee Center.

-   **[Define an action schedule for affected people](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/health-and-safety-risk-management/hs-define-action-schedule-affected-people.md)**  
Define an action schedule for the people affected by an exposure. The action schedule creates an action for each affected person when there's an active exposure for an exposure assessment.
-   **[Add a measurement and exposure source for an exposure assessment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/health-and-safety-risk-management/hs-add-measurement-exposure-assessment.md)**  
Add a measurement recorded for the exposure type when performing an exposure assessment.

**Parent Topic:**[Safety exposure management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/health-and-safety-risk-management/hs-safety-exposures.md)

