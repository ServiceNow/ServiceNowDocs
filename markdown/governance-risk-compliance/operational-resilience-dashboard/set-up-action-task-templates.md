---
title: Set up action task templates in Regulatory agency profile
description: Set up action task templates in the Regulatory Body Management Agency Profile \[sn\_reg\_body\_mgmt\_agency\_profile.list\] table. Verify that the action task configurations \(with Smart Assessment Smart Assessment template configurations\) for the selected regulation are correctly set up.
locale: en-US
release: xanadu
product: Operational Resilience Dashboard
classification: operational-resilience-dashboard
topic_type: task
last_updated: "2025-11-25"
reading_time_minutes: 4
breadcrumb: [Configure, Using Digital resilience incident reporting, Manage, Operational Resilience, Governance, Risk, and Compliance]
---

# Set up action task templates in Regulatory agency profile

Set up action task templates in the Regulatory Body Management Agency Profile \[sn\_reg\_body\_mgmt\_agency\_profile.list\] table. Verify that the action task configurations \(with Smart Assessment Smart Assessment template configurations\) for the selected regulation are correctly set up.

## Before you begin

Role required: sn\_oper\_res.admin, sn\_dri\_inc\_rptg.digital\_resilience\_incident\_admin

## Procedure

1.  Navigate to **Workspaces** &gt; **Operational Resilience Workspace** and open the "Regulatory Body Management Agency Profile" \[sn\_reg\_body\_mgmt\_agency\_profile.list\] table for the selected regulation.

2.  Configure the action tasks \(with Smart Assessment templates.

    As a Digital Resilience Incident administrator \(sn\_dri\_inc\_rptg.digital\_resilience\_incident\_admin\), you can modify action tasks or configure additional action tasks to meet your organizational requirements.

    This example shows the Regulatory agency profile's "DORA reporting cases" record, featuring the 'European Union' as the regulatory agency and 'Digital Operational Resilience Act' as the regulation. This record also contains action tasks preconfigured with Smart Assessment templates.

    ![DORA reporting cases" record. For the text description, refer to the text that precedes this image.](../image/action-task-config-dora-conditions.png)

    1.  Configure single or multiple regulatory agency profiles for the Digital Resilience Incident Reporting Case \[sn\_grc\_inc\_rptg\_case\_task\] table, based on different combinations of agency, regulation, or jurisdiction criteria.

    2.  Verify the action task configurations preconfigured with Smart Assessment templates.

        **Note:** Use an action task configuration to set up contextual information for different regulations. The configuration includes the assessment template, assignment group, trigger conditions, due dates, and more.

        **Note:** The templates shown in this example are specific to DORA regulation. If other regulations are mapped to the entities in use, verify that their corresponding Smart Assessment templates are set up and published in the Assessment Workspace first. For more information, see [Set up DRI Smart Assessment templates](set-up-sae-templates.md).

        The DORA regulations include four Smart Assessment template configurations as shown in the Action Task Configurations related list.

        ![Smart Assessment template configurations. For the text description, refer to the text that precedes this image.](../image/action-task-config-dora.png)

        -   **Regulatory reporting assessment of IT incidents template**

            When a case is created, the 'Regulatory reporting assessment of IT incidents' template is used to generate the action tasks.

            The following example shows that when you create a DIR case with DORA as the authority document, an action task is generated automatically using the 'Regulatory reporting assessment of IT incidents' template. The system creates a case with DORA as the authority document, assigns it a specific title, and routes it to a designated group.

            The **Repeat** field indicates that the action tasks can be configured for either once or periodically. For regulatory reporting, the initial action task is created only once.

            The **On create** field shows that the action tasks are generated only when a DRIR case is created. If the **On create** field is inactive \(cleared\), the action task isn’t generated. The **Assignment group** field assigns the action task to a designated group automatically.

            ![Task 1.](../image/act-task-1-temp-condition.png)

        -   **DRI Initial report template**

            When the reporting status of a regulation changes from "To be determined' to 'Reportable' after the first assessment, an initial report is sent automatically. Similar to other action tasks, you can configure the assignment group and due date, and this template is created only once according to trigger.

            ![Task 2.](../image/act-task-2-temp-condition.png)

            A single DIR case can be associated with multiple regulations. When the reporting status of any individual regulation changes to 'reportable,' a dedicated initial report is generated for that specific regulation. For example, if a case involves five regulations, and each one's status becomes 'reportable,' five separate initial reports are created, demonstrating comprehensive support for multiple regulations.

        -   **DRI Intermediate report template**

            Intermediate reporting and periodic assessments: When the DRI initial report is completed, the DRI intermediate reporting is triggered, specifically when its status changes to **Closed Complete**.

            Periodic action tasks: Following the initial report's completion, action tasks for intermediate assessments can be generated periodically as shown in the **Repeat** field. Configure the repetition frequency in the **Repeat interval** field. The example shows that you’re going to create an action task with the given template every 3 days.

            Termination conditions: When specific conditions are met, the periodic generation of these action tasks is terminated, indicating the underlying issue is resolved or no longer requires ongoing assessment. The system doesn’t send the intermediate action task anymore.

            These conditions are evaluated against the DIR case state or the incident or the security incident source record.

            ![Task 3.](../image/act-task-3-temp-condition.png)

            The example shows the following termination conditions:

            -   The source of DIR case is 'Manual' and its state is 'Closed' or 'Canceled'.
            -   The source of DIR case isn’t 'Manual', the source record state of incident or security incident is Closed' or the state of DIR case is 'Closed' or 'Canceled'.
            When any of these termination conditions are met, no further intermediate assessment action tasks are generated.

        -   **DRI Final report template**

            When the associated source record's state is 'Closed' and the source isn’t manual as shown in the example, the final report is generated automatically.

            ![Task 4.](../image/act-task-4-temp-condition.png)

            If the source is manual, you must create the final report manually.

3.  Modify the action tasks as necessary.

4.  Select **Save**.

    Completing the configuration steps outlined in this section sets up the action task configurations in the 'Regulatory Body Management Agency Profile' table.


