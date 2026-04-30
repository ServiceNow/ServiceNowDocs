---
title: Add a related party to an install base item
description: Add related parties to an install base item in the Customer Service Management application so that you can enable another party to have access to an install base.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Using customer access management, Customer management, Using Customer Service Management, Customer Service Management]
---

# Add a related party to an install base item

Add related parties to an install base item in the Customer Service Management application so that you can enable another party to have access to an install base.

## Before you begin

Role required: admin and sn\_customerservice\_manager

## About this task

An install base related party is a list of contacts, consumers, contributors, service organization members, accounts, or service organizations. You add a related party to enable access to another party that isn't the owner of the install base. The related parties that you associate to an install base can access the install base and related entities, including the installed products, sold products, and cases that are associated to the install base.

**Note:** You can enable additional contacts by using the **Restrict Contact Access** field. For details, see [Restrict contact access](manage-account-access-cam.md).

## Procedure

1.  Navigate to **All** &gt; **Customer Service** &gt; **Products** &gt; **Install Base Items**.

2.  Open an install base item from the list.

3.  Select **Install Base Related Parties**, and select **New**.

4.  From the **Type** drop-down, select the type of related party that you want to add to the install base item.

    Based on the selection that you chose, you can assign one of the combinations in the following table:

    |Type|Entity|
    |----|------|
    |Authorized Service Organization|Service Organization|
    |Authorized Consumer|Consumer|
    |Authorized Contributor|User|
    |Authorized Member|Service Organization|
    |Authorized Contact|Contact|
    |Authorized Account|Account|
    |Listed Contact|Not applicable|
    |Listed Service Organization|Not applicable|
    |Listed Contributor|Not applicable|
    |Listed Member|Not applicable|
    |Listed Account|Not applicable|
    |Listed Consumer|Not applicable|

    **Note:** The **Responsibility** field on the Install Base Related Parties form is automatically populated based on the type of related party that is selected. For information on the type of related parties, see [Add related party configurations to cases, sold products, install bases, or service organizations](adding-related-party-config-to-case.md).

5.  Select **Submit**.


## Result

The contact is assigned as a related party to the Install base item. The contact gets access to all the corresponding items, such as the child install base items and the cases on the install base item form.

