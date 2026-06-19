---
title: Configure a question node to ask failure codes
description: Add a question to ask for the failure code that the customer received after a failed credit card transaction.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/customer-service-management/configure-question-node-to-ask-failure-codes.html
release: zurich
product: Customer Service Management
classification: customer-service-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Example configuration of a decision tree, Guided Decisions configuration, Agent tools, Organize agent workspaces, Configure, Customer Service Management]
---

# Configure a question node to ask failure codes

Add a question to ask for the failure code that the customer received after a failed credit card transaction.

## Before you begin

Role required: admin, sn\_gd\_core.decision\_tree\_author

## About this task

\[Omitted image "ex-failure-code-question.png"\] Alt text: The Ask for failure codes question node showing the choice as the answer type with 200, 300, and 500 as the choices.

## Procedure

1.  Select **Add node** on the Amount-not-debited path.

    \[Omitted image "ex-amt-not-debited-question.png"\] Alt text: the Add node button in the Decision Tree Builder to configure a question or guidance node.

2.  In the pop-up window, select **Ask users at least one question** to configure a question node.

3.  In the **Node name** field, enter `Ask for failure codes`.

4.  In the **Question or instruction** field, type `Enter the failure code`.

5.  Make this question a required question by selecting the **Required question** field.

6.  In the **Type of answer** field, select Choice.

7.  In the **Label** field, enter `Failure code 200` for the first option in the list.

8.  Select **Add choice**.

9.  In the **Label** field, enter `Failure code 300` for the second option in the list.

10. Select **Add choice**.

11. In the **Label** field, enter `Failure code 500` for the third option in the list.

12. Select **Save and close**.


## What to do next

[Configure a path](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/configure-path-for-200-failure-code.md) for each failure code the customer can receive after a failed credit card transaction.

