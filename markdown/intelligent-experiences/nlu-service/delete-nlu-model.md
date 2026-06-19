---
title: Delete an NLU model
description: Delete a Natural Language Understanding \(NLU\) model permanently.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/nlu-service/delete-nlu-model.html
release: australia
product: NLU Service
classification: nlu-service
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Creating models, Model management, Natural Language Understanding, Enable AI experiences]
---

# Delete an NLU model

Delete a Natural Language Understanding \(NLU\) model permanently.

## Before you begin

Role required: admin or nlu\_admin

## About this task

Deleting an NLU model removes the model and its contents, including its default test set, from the system. You cannot delete a model if it meets any of the following criteria:

-   The model is pre-built
-   The model contains at least one intent that is mapped to a Virtual Agent topic

**Warning:** Deleting a model cannot be undone.

## Procedure

1.  Set your scope to the scope of the model you want to delete.

2.  Navigate to **All** &gt; **NLU Workbench** &gt; **Models**.

3.  On the far right column of the model list, select the more the **More options** menu for the model you want to delete.

    \[Omitted image "delete-nlu-model02.png"\] Alt text: The More options menu in the model list

4.  Select the option to **Delete this model**.

5.  Select the check box to acknowledge that all references to this model will be deleted.

    \[Omitted image "delete-nlu-model03.png"\] Alt text: Confirmation popup for Delete model

6.  Select **Delete model**.

    The system deletes your model and reloads the page.


