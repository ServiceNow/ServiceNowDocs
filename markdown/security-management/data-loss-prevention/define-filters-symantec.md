---
title: Define filters to apply for the Incident creation
description: Define and set filter conditions to drill down the incoming  Symantec DLP  incidents. Determine the incidents that should be created as DLP incidents in ServiceNow.
locale: en-US
release: yokohama
product: Data Loss Prevention
classification: data-loss-prevention
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Create a profile for Symantec DLP integration, Symantec Integration for Data Loss Prevention Incident Response, DLP integrations, Data Loss Prevention Incident Response, Security Operations]
---

# Define filters to apply for the Incident creation

Define and set filter conditions to drill down the incoming  Symantec DLP  incidents. Determine the incidents that should be created as DLP incidents in ServiceNow®.

## Before you begin

Role required: sn\_dlir.admin

## About this task

Filtering helps you to isolate DLP incidents and to limit the number of DLP incidents that you create. If additional filtering criteria are set, only incidents that match the conditions are created.

## Procedure

1.  Select **API based filter for incident ingestion** checkbox to apply the API filters and retrieve the incidents that match the filter criteria.

2.  Add the API filters.

    The following is an example that shows the API filters.

    ```
    {
                    "operandOne": {
                        "name": "incidentStatusName"
                    },
                    "filterType": "string",
                    "operator": "EQ",
                    "operandTwoValues": [
                        "incident.status.New"
                    ]
                }
    ```

    **Note:** For more information on the API filters on Symantec integration, see [Incident Lists: Parameters - Request object details](https://apidocs.securitycloud.symantec.com/#/doc?id=incidentlists).

3.  Click **Validate Filter** after you apply the API filters.

    **Note:** If the validation is unsuccessful then an error message is displayed that the validation is failed and this happens when the filters are not properly entered as per the Symantec APIs.

    ![Adding API based filters](../image/dlp-api-filters.png "Adding API Filters")

4.  Select **Post Incident Ingestion Filter** checkbox to define the criteria that an incoming Symantec DLP incident must satisfy so that a DLP incident is created.

    The options in the first field in the Filter Conditions match the fields that are available in the DLP incident. The criteria that you enter are case-sensitive. Verify that the criteria you define match the values of the incident.

5.  In the condition builder, set the filters in the **Filter Conditions** field.

    ![DLP Symantec Filtering section](../../data-loss-prevention/image/dlp-symantec-filtering.gif)

6.  To add more conditions, click  **AND**  or  **OR**.

    -   If  **AND**  is selected, all conditions must be matched.
    -   If  **OR**  is selected, either condition can be matched.

## What to do next

To configure the schedule, click **Continue**.

**Parent Topic:**[Create a profile for Symantec DLP integration](create-profile-symantec-dlp.md)

