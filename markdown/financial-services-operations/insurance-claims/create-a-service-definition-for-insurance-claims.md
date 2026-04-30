---
title: Create a service definition for Insurance claims
description: Create a service definition for each claim type in your Insurance claims workflow. You can also create a service definition to generate adjuster tasks in the workflow.
locale: en-US
release: yokohama
product: Insurance Claims
classification: insurance-claims
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Creating a service definition for Insurance claims, Setting up Insurance claims, Insurance claims, Claims applications, Using insurance applications, Financial Services Operations \(FSO\)]
---

# Create a service definition for Insurance claims

Create a service definition for each claim type in your Insurance claims workflow. You can also create a service definition to generate adjuster tasks in the workflow.

## Before you begin

Set the application scope in your instance to **Insurance claims**.

Role required: admin

## About this task

A service definition describes a service that your workflow offers to support a claim type. In Insurance claims, you also create adjuster task service definitions. These definitions help to generate adjuster tasks when an incident is created \(for example, an adjuster review task\).

Create an adjuster task service definition for each incident type to ensure clear categorization and efficient task management in Insurance claims.

The service definition for the claim type and the adjuster service definition are both used in the Claim Incident Configuration \[sn\_ins\_claim\_incident\_config\] table as part of configuring your workflow. For more information, see [Claim Incident Configuration table](../concept/claim-incident-configuration-table.md).

## Procedure

1.  Navigate to **All** &gt; **Insurance claims** &gt; **Administration** &gt; **Service definitions**.

2.  Select **New**.

3.  In the **Table** field, select one of the following options.

    -   For defining a claim type, select Claim Case \[sn\_ins\_gen\_claim\_case\].
    -   For an adjuster task, select Claim Adjuster Task \[sn\_ins\_gen\_claim\_adj\_task\].
4.  In the **Name** field, enter the name that the customer representatives see in the playbook.

5.  In the **ID** field, enter the name in snake case \(all words in lowercase separated by underscores\).

6.  In the **Description** field, describe the purpose of the service definition.

7.  In the **Default table field values** field, select **Short description**, and enter a short description \(for example, the value in the name field\).

8.  Select **Save**.

9.  In the **Default table field values** field, add **Claim service**, and choose the service definition that you're currently creating.

10. Save the record.

    If you’re defining an adjuster task, the procedure is complete.

    If you’re defining a claim type, complete the following steps.

11. In the related list **Service Definition Category Relationships**, select **New**.

12. In the **Service Category** field, select the service definition category that this service definition is in.

13. Select **Submit**.

    ![Service definition for a travel claim with a service category relationship.](../image/create-service-definition-example.png)


**Parent Topic:**[Creating a service definition for Insurance claims](../concept/create-service-definitions-for-insurance-claims.md)

