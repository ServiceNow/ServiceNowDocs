---
title: View prediction on field change
description: Agents can use Task Intelligence to predict values for configured fields before a case is created and after a case is created.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Use Task Intelligence for Customer Service, Automate and optimize, Using Customer Service Management, Customer Service Management]
---

# View prediction on field change

Agents can use Task Intelligence to predict values for configured fields before a case is created and after a case is created.

## Before you begin

Role required: sn\_customerservice\_agent, sn\_customerservice\_manager or ti\_admin

## About this task

When you create a case or after a case is created, the Task Intelligence feature predicts values for the configured fields based on the short description or description.

**Note:**

-   If you update the case, the values for these fields are not predicted again.
-   View prediction on field change is also available for interaction records.

## Procedure

1.  Create a case.

2.  Enter information in the **Short description** or **description** field and then tab to the next field.

    Based on this information, the system predicts the values for configured fields without saving the case form.

    **Note:** If the system cannot predict values based on the short description, these fields remain blank.

3.  Change the values in the predicted fields if needed or enter values for fields where Task Intelligence has skipped prediction.

    The system does not overwrite user-entered values for the predicted fields.

4.  Select **Save**.

    The data is saved in the record and persisted in the predictions table. A message is displayed to the agent indicating that the fields may have been modified, prompting them to save the revised predictions.


