---
title: Create a case API Variable for a PaCE policy in Grants Management ​
description: Create a case API variable to transfer the information collected from the case to the PaCE eligibility rules engine. This will be used when creating a policy and referencing fields on the case.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-12-02"
reading_time_minutes: 1
breadcrumb: [Configure Eligibility Rules Engine Policies, Configure PaCE Eligibility Framework Engine, Grants Management, Playbooks and Solutions, Configure agent workspaces, Configure, Public Sector Digital Services \(PSDS\)]
---

# Create a case API Variable for a PaCE policy in Grants Management ​

Create a case API variable to transfer the information collected from the case to the PaCE eligibility rules engine. This will be used when creating a policy and referencing fields on the case.

## About this task

An API Variable is a variable that enables you to pass the value to the policy whenever the policy is invoked. Specify a value for this API Variable when calling the API, otherwise the policy is not executed and no decision is reached.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Workspaces** &gt; **CSM Configurable Workspace**.

2.  From the CSM Configurable Workspace sidebar, navigate to the **Policy Home**.

3.  Select the **API Variables** list.

4.  Select **Add** to create an API variable.

5.  On the form, fill in the fields with the following information.

    |Field|Value|
    |-----|-----|
    |Label|Case Reference|
    |Name|case\_reference|
    |Type|Reference|
    |Description|Case Reference|
    |Table|Grants Table|
    |Match Criteria|Select first match|

6.  Select **Save**.


## Result

An API variable is created, and will pass the value to the policy whenever the policy is invoked, after which the policy is executed and a decision is reached.

## What to do next

Create a data collector for a PaCE policy.

**Parent Topic:**[Configure Eligibility Rules Engine Policies in Grants Management](../task/psds-config-gmp-eligibility.md)

**Related topics**  


[Create a case data collector for a PaCE policy in Grants Management](psds-config-gmp-data-collector.md)

