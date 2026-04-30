---
title: Generate a report for a safety incident, observation, or injury
description: Generate a report for a safety incident, observation, or an injury that you want to export for your regional or industry-specific requirements.
locale: en-US
release: xanadu
product: Health and Safety Incident Management
classification: health-and-safety-incident-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Manage incidents and observations, Health and Safety Incident Management, Health and Safety, Employee Service Management]
---

# Generate a report for a safety incident, observation, or injury

Generate a report for a safety incident, observation, or an injury that you want to export for your regional or industry-specific requirements.

## Before you begin

Role required: sn\_ohs\_im.manager, sn\_ohs\_im.agent, or sn\_ohs\_im.operations\_manager

## About this task

The report generation uses a report field mapping for your reporting PDF template. A report field mapping includes mappings of fields from the safety record \(such as incident or observation\) to the fields in the reporting PDF template. When generating a report, the exported PDF fills in information from the selected safety record through mapped fields. This field mapping, therefore, speeds up the report filling for incidents, observations, or injury and illness records. For more information on report field mapping, see [Create a safety report field mapping](create-safety-report-field-mapping.md).

## Procedure

1.  Navigate to **All** &gt; **Health and Safety** &gt; **Health and Safety Workspace**.

2.  Select the Incident Management icon \(![Incident Management icon.](../image/list-icon-hs.png)\).

3.  In the **Lists** tab, open the safety incident, observation, or injury and illness list.

    -   For the safety incidents list, select **Safety Incidents** and then **All**.
    -   For the safety observations list, select **Safety Observations** and then **All**.
    -   For the injury and illness list, select **Injury / illnesses** and then **All**.
4.  In the list, open a safety record to generate a report for.

5.  Select **Generate report**.

6.  In the **Generate report** dialog box, select a report mapping in the **Select report** field.

    Only the published report mapping forms are available to select in the **Select report** field.

7.  Select **Generate**.


## Result

-   The report is generated based on the selected report mapping and its PDF template.
-   The PDF template is automatically filled with the values from the selected safety record.
-   The generated report is available in the **Attachments** section of the safety record, for example, safety incident.

**Parent Topic:**[Managing Health and Safety incidents and observations](../concept/managing-hs-incidents-obs.md)

