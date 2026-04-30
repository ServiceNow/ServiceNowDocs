---
title: Capturing multiple job records for a user
description: Capture multiple job records for a user with the new Jobs \(sn\_hr\_core\_job\) table. When creating HR cases, you can specify which job the case pertains to. For example, say that you have a payroll discrepancy case and the employee has two associated job records. When the case is created, you can specify which job the case is for.
locale: en-US
release: xanadu
product: HR Service Delivery
classification: hr-service-delivery
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
keywords: [Rehires, Transfers, Multiple jobs]
breadcrumb: [HR Administration, Case and Knowledge Management, HR Service Delivery, Employee Service Management]
---

# Capturing multiple job records for a user

Capture multiple job records for a user with the new Jobs \(sn\_hr\_core\_job\) table. When creating HR cases, you can specify which job the case pertains to. For example, say that you have a payroll discrepancy case and the employee has two associated job records. When the case is created, you can specify which job the case is for.

## Jobs table overview

Beginning in the New York release, you can use the new Jobs \(sn\_hr\_core\_job\) table to store multiple job records per user and capture the job history of users within your organization.

## Jobs table and HR Profile table

The HR Profile table has a reference to the Jobs table for the user's primary job.

<table id="table_fn3_ylg_f3b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

primary\_job-   Job start date
-   Job end date

</td><td>

Reference field to the Jobs \(sn\_hr\_core\_job\) table.

</td></tr></tbody>
</table>For example, the following HR profile record is for Eva Seahorn. Eva was first hired as a UX designer in May 2017. In August 2018, Eva left the company. In June 2019, Eva was rehired as a marketing director. Eva has two associated job records, with the marketing director position as Eva's primary job.

-   In the Employment Information related list, information about the primary job is displayed.
-   In the Jobs related list, all of the associated job records are displayed.

**Note:** The employment start date represents the first day the user was employed with the organization. The job start date represents the first day of the user's current primary job. Because Eva left the organization in August 2018, but was rehired in June 2019. This represents Eva's new employment start date.

![HR profile record with multiple job records.](../image/multiple-jobs-hr-profile-example.png)

## Jobs table and HR Case table

The HR Case table has a reference to the Jobs table for the subject person's job.

|Field|Description|
|-----|-----------|
|subject\_person\_job|Reference field to the Jobs \(sn\_hr\_core\_job\) table.|

In the case of Eva Seahorn, for example, Eva was rehired as a marketing director in June 2019. Eva has two associated job records. When an onboarding case is created for Eva, the **subject\_person\_job** field enables you to specify which job the onboarding case pertains to. The onboarding case would be for the marketing director job Eva was rehired for.

## Supporting multiple jobs in a lifecycle event

Use the Jobs table to create lifecycle event cases where you can specify which job the case pertains to. For example, say that you have an intern that is being transferred to a full-time position. The intern has two associated job records. When an onboarding case for the full-time position is created, the case is associated with the full-time job record, ensuring that downstream activity sets and activities are triggered based on information from that relevant job record. For more information, see [Support multiple jobs in a lifecycle event](../task/adopt-jobs-table.md).

**Parent Topic:**[HR Administration](c_AdministerHRServiceManagement.md)

**Related topics**  


[hr\_Utils - Global](https://www.servicenow.com/docs/access?context=hr_UtilsAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)

[hr\_ActivitySet - Global](https://www.servicenow.com/docs/access?context=hr_ActivitySetAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)

[hr\_ActivityUtils - Global](https://www.servicenow.com/docs/access?context=hr_ActivityUtilsAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)

