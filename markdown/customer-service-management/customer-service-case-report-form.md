---
title: Case Report form
description: The Case Report form includes reporting-related fields that are derived from case records.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Customer Service forms, Reference, Customer Service Management]
---

# Case Report form

The Case Report form includes reporting-related fields that are derived from case records.

The Case Report table stores KPIs and metrics for case records and includes the following calculated metrics which are displayed on the [Customer Service Manager dashboard](../concept/csm-manager-dashboard.md).

-   Agent Reassignment Count
-   First Contact Resolution
-   Reopen Count

The Customer Service Manager dashboard includes the **First Call Resolution** indicator, which shows the percentage of cases that were resolved during the first contact with the customer. The percent change in the current period appears under the total percentage. The value for the First Call Resolution indicator is returned by the CaseReportUtils script include.

<table id="table_fyv_dtr_bs"><thead><tr><th>

Field

</th><th>

Definition

</th></tr></thead><tbody><tr><td>

Number

</td><td>

The automatically generated case report number.

</td></tr><tr><td>

First Contact Resolution

</td><td>

Records whether a case was resolved during a customer’s first contact with an agent. This field can have one of the following values:

-   0: None \(default value\)
-   1: True
-   2: False

 For more information about how this field is calculated, see First Call Resolution \(FCR\) metric below.

</td></tr><tr><td>

Agent Reassignment Count

</td><td>

The number of times that a case has been reassigned to a different agent. The default value is 0.

</td></tr><tr><td>

Reopen Count

</td><td>

The number of times a case has been closed and reopened. The default value is 0.

</td></tr><tr><td>

Skipped by Prediction

</td><td>

Used to identify cases that are skipped by the Predictive Intelligence feature. The default value is false \(disabled\).

</td></tr><tr><td>

Case

</td><td>

The case for which this case report was generated.

</td></tr><tr><td>

Customer Satisfaction Score

</td><td>

The customer gives the customer satisfaction score on accepting the case resolution.

</td></tr><tr><td>

Time to Resolve

</td><td>

Time taken by an agent to resolve the case. Calculated as the difference between the case resolved time and case created time.

</td></tr></tbody>
</table>## First Call Resolution \(FCR\) metric

The First Call Resolution \(FCR\) metric relates to the number of times that a customer request is resolved during the first contact with an agent. Out of box, the First Call Resolution script returns a value of true or false.

FCR is true if a record has one update. For example, if the state of a new case is set to Closed and then updated or saved, the FCR value is True.

FCR is false if:

-   A case is reopened.
-   The state of a case is updated to Awaiting Info.
-   An Openframe phone record exists for the case and the date of that record is prior to the case resolution date.
-   An email log exists for the case, the email was not created by the system, and the email creation date is prior to the case resolution date.
-   A work order entry exists for the case and the date of that work order is prior to the case resolution date.

