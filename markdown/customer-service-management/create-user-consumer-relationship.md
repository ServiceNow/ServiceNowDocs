---
title: Create a relationship between two consumers
description: Create a relationship between two consumers, regardless of household.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure consumers, Customer data, Set up your environment, Configure, Customer Service Management]
---

# Create a relationship between two consumers

Create a relationship between two consumers, regardless of household.

## Before you begin

Role required: One of the following roles:

-   sn\_crm\_consumer\_relationship\_data\_manager
-   sn\_crm\_foundation\_data\_manager
-   sn\_crm\_foundation\_admin
-   sn\_customerservice.svc\_location\_manager
-   sn\_customerservice\_manager
-   admin

## About this task

Relationships are based on responsibilities. A responsibility definition describes a role or a function that supports a customer or consumer. To create a relationship between two consumers, use the Authorized Representative responsibility.

## Procedure

1.  Navigate to **All** &gt; **Customer Service** &gt; **Customer** &gt; **Consumers**.

2.  Select a consumer.

3.  In the Consumer Relationships related list, select **New**.

    This related list shows the current relationships that exist for the selected consumer. When you select **New**, a new Consumer to Consumer Relationship form is displayed with the **Consumer is** field filled in.

4.  In the **Responsibility** field, select the **Authorized Representative** responsibility.

5.  In the **of Consumer** field, select the consumer who is being represented by the consumer in the **Consumer is** field.

6.  In the **Type** field, select the type from the list of related party configurations and the **Order** field specifies the sequence in which records are displayed, organized according to business preferences.

    **Note:** Starting with the Yokohama release, the **Type** field is added to the Consumer Relationships form. For more information on how to populate the **Type** field for existing data, see [Populate the Type field in relationship tables using the fix script](migration-of-account-manager-responsibility-access.md).

7.  Select **Submit**.

    The relationship is added to the Consumer Relationships related list.


