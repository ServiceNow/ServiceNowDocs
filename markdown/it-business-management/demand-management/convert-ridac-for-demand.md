---
title: Convert one RIDAC record to another for a demand
description: Convert one RIDAC record to another to retain record information and track issues without creating a record manually.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-business-management/demand-management/convert-ridac-for-demand.html
release: australia
product: Demand Management
classification: demand-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [RIDAC \(Risk, Issue, Decision, Action, and Request Changes\) records, Use, Demand Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Convert one RIDAC record to another for a demand

Convert one RIDAC record to another to retain record information and track issues without creating a record manually.

## Before you begin

Role required: it\_demand\_manager

## About this task

When you convert a RIDAC record to another record, the values for the **Short description**, **Requester**, and **Assigned to** fields are carried forward.

You can also specify to close the parent record on creation of the new record instead of manually closing the parent record.

To view all converted RIDAC records, select the **View RIDAC** related link on the Demand form. You can also access this list from **View RIDAC** in the Demand module application navigator.

## Procedure

1.  Navigate to **All** &gt; **Demand** &gt; **Demands** &gt; **All**.

2.  Select the demand for which you want to convert a risk, issue, decision, action, or request change record to another RIDAC record.

3.  From the Demand form related list, select the risk, issue, decision, action, or request change record to open the form view.

4.  Select the **Convert to RIDAC** related link on the form.

5.  On the Convert dialog box, from the select task type list, select the RIDAC record to which you want to convert the selected record.

    For example, if you wanted to convert a risk to an issue, you would select **Issue**.

6.  Modify the text in the **Short description** field, which is copied from the parent record.

7.  Change the default assignment copied from the parent record in the **Assigned to** field by selecting the lookup icon \[Omitted image "assigned-to-lookup-icon.png"\] Alt text: and selecting a different user.

8.  If you want to close the parent RIDAC record on creation of the new record, select the close parent record option.

    The label of the close parent record option changes depending on the parent record type. For example, if the parent record is Risk and you’re converting it to an issue record, the close record option would appear as **Close Risk**.

9.  Select **OK**.


**Parent Topic:**[RIDACs records for a demand](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/demand-management/ridac-entries-for-demand.md)

