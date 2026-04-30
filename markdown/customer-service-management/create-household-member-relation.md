---
title: Create a relationship between household members
description: Create a relationship between two consumers who are current members of the same household.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configuring households, Customer data, Set up your environment, Configure, Customer Service Management]
---

# Create a relationship between household members

Create a relationship between two consumers who are current members of the same household.

## Before you begin

Role required: sn\_customerservice\_manager, admin

## About this task

Relationships are based on responsibilities. A responsibility definition describes a role or a function that supports a customer or consumer. To create a relationship between two consumers in a household, use the Authorized Representative responsibility.

## Procedure

1.  Navigate to **All** &gt; **Customer Service** &gt; **Customer** &gt; **Households**.

2.  Select a household.

3.  In the Member Relationships related list, click **New**.

    This related list shows the current relationships that exist between consumers in this household. When you click **New**, a new Household Member Relationship is displayed with the **Household** field already filled in.

4.  In the **Consumer is** field, select the consumer in the household to fulfill the responsibility on behalf of another consumer within the same household.

5.  In the **Responsibility** field, select the **Authorized Representative** responsibility.

6.  In the **of Consumer** field, select the consumer who is being represented by the consumer in the **Consumer is** field.

7.  In the **Type** field, select the type from the list of related party configurations and the **Order** field specifies the sequence in which records are displayed, organized according to business preferences.

    **Note:** Starting with the Yokohama release, the **Type** field is added to the Consumer Relationships form. For more information on how to populate the **Type** field for existing data, see [Populate the Type field in relationship tables using the fix script](migration-of-account-manager-responsibility-access.md).

8.  Click **Submit**.

    The relationship is added to the Member Relationships related list.


