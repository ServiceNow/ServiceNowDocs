---
title: Configure the start node to ask for cardholder and transaction details
description: Add questions to ask for credit cardholder details and transaction details and configure answer types in a start node in Decision Tree Builder.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Example configuration of a decision tree, Guided Decisions configuration, Agent tools, Organize agent workspaces, Configuring Customer Service Management, Customer Service Management]
---

# Configure the start node to ask for cardholder and transaction details

Add questions to ask for credit cardholder details and transaction details and configure answer types in a start node in Decision Tree Builder.

## Before you begin

Role required: admin, sn\_gd\_core.decision\_tree\_author

## About this task

In the question node, you can add the questions that you want to ask customers or details that you want to collect. For example, you can ask for the type of credit card or whether any amount is debited. Based on the answers provided, the path to a next question or guidance node is taken.

## Procedure

1.  Select **Open in Builder**.

    The new decision tree opens in Decision Tree Builder in a new tab.

    ![After entering the details in Decision tree new record and submitting the form, the Open in Builder button is shown.](../image/ex-open-in-builder.png)

2.  Select **New node**, which is a start node of your decision tree.

3.  In the **Node name** field, enter `Ask card holder and transaction details`.

4.  In the Input section, in the **Reference table** field, select the Case table.

    ![Input section contains the Input name, type of input, and reference table fields.](../image/ex-case-ref-table.png)

    The reference table doesn’t necessarily have to be a task table. For example, you can select a case, incident, or interaction table for the record context to recommend this decision tree in a workspace.

    **Note:** You must select the same table as the reference table for the context record in Recommended Actions.

5.  Configure question 1.

    1.  In the **Question or instruction** field, type `Enter your name`.

    2.  Make this question a required question by selecting the **Required question** field.

    3.  In the **Type of answer** field, select String.

    ![Question 1 for asking the card holder's name and the answer type selected as string.](../image/ex-start-node-ques-1.png)

6.  Configure question 2.

    1.  Select the **Add question** button.

    2.  In the **Question or instruction** field, type `Enter your credit card number`.

    3.  Make this question a required question by selecting the **Required question** field.

    4.  In the **Type of answer** field, select Integer.

    ![Question 2 for asking the credit card number and the answer type selected as integer.](../image/ex-start-node-ques-2.png)

7.  Configure question 3.

    1.  Select the **Add question** button.

    2.  In the **Question or instruction** field, type `Enter the transaction ID`.

    3.  Make this question a required question by selecting the **Required question** field.

    4.  In the **Type of answer** field, select Integer.

    ![Question 3 for asking the transaction ID and the answer type selected as integer.](../image/ex-start-node-ques-3.png)

8.  Configure question 4.

    1.  Select the **Add question** button.

    2.  In the **Question or instruction** field, type `Select the card type`.

    3.  Make this question a required question by selecting the **Required question** field.

    4.  In the **Type of answer** field, select Choice.

    5.  In the **Label** field, enter `Visa` for the first option in the list.

    6.  Select **Add choice**.

    7.  In the **Label** field, enter `MasterCard` for the second option in the list.

    8.  Select **Add choice**.

    9.  In the **Label** field, enter `Meestro` for the third option in the list.

    ![Question 4 for asking the card type and the answer type selected as choice. The choice list includes options such as Visa, MasterCard, and Meestro.](../image/ex-start-node-ques-4.png)

9.  Configure question 5.

    1.  Select the **Add question** button.

    2.  In the **Question or instruction** field, type `Select date and time of the failed transaction`.

    3.  Make this question a required question by selecting the **Required question** field.

    4.  In the **Type of answer** field, select Date/time.

    ![Question 5 for asking the date and time of the transaction and the answer type selected as date/time.](../image/ex-start-node-ques-5.png)

10. Configure question 6.

    1.  Select the **Add question** button.

    2.  In the **Question or instruction** field, type `Has any amount been debited?`.

    3.  Make this question a required question by selecting the **Required question** field.

    4.  In the **Type of answer** field, select True/False.

    ![Question 6 for asking whether any amount is debited and the answer type selected as true/false.](../image/ex-start-node-ques-6.png)

11. Select **Save and close**.


## What to do next

[Add paths and configure conditions for transactions](../concept/configuring-paths-for-next-nodes.md#) when the next question or guidance node is displayed in a decision tree.

