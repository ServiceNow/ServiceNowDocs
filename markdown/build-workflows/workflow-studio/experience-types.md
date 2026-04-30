---
title: UI Layouts
description: A UI Layout describes what properties and components to use when an activity renders as a card in a Playbook Experience.
locale: en-US
release: yokohama
product: Workflow Studio
classification: workflow-studio
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Activity definitions, Stages and activities, Building playbooks, Using Workflow Studio, Workflow Studio, Build workflows]
---

# UI Layouts

A UI Layout describes what properties and components to use when an activity renders as a card in a Playbook Experience.

When creating an activity definition, you must select an UI Layout to associate your activity definition with. Playbooks come with the following UI Layouts that are available in your instance by default:

-   Create Record
-   Questionnaire
-   Instructional
-   Knowledge
-   List
-   Record
-   Record generator

Depending on the UI Layout associated with the activity, different sections and fields appear under the activity definition's Activity Experience. These sections and fields let you set up the activity data that renders during the runtime Playbook Experience.

**Note:** All UI Layouts, except for Record generator, display an Associated Record section. For information on how to set up or edit the Associated Record section in an activity definition, see [Create an activity definition](../task/create-activity-definition.md).

## Create Record

If you choose the Create Record UI Layout, the following sections appear in the Activity Experience section for your activity definition:

-   **Associated Record**

    Displays the following fields:

    -   Associated table
    -   Associated record
    -   Experience Status Table
    -   Experience Status Record
-   **Details**

    Displays the following fields:

    -   Tagline
    -   Icon
    -   Title
    -   Description
    -   Pending State Title
    -   Pending State Description
    -   Record fields
    -   Footer
-   **Form**

    Displays the following fields:

    -   Form View
    -   Form fields
    -   Template Fields
-   **Attachments**

    Displays the following fields:

    -   Attachment source
    -   Attachments read only
-   **Features**

    Displays the following fields:

    -   Show SLA
    -   Show Checklist
    -   Is Automated

The Create Record activity that comes with the application uses this UI Layout.

![]( "In an activity definition")

In Workflow Studio, the fields are configured on the UI Layouts tab of the side panel:

![]( "In Workflow Studio")

In a running playbook, your configurations are reflected:

![]( "In a running playbook")

## Questionnaire

If you choose the Questionnaire UI Layout, the following sections appear in the Activity Experience section for your activity definition:

-   **Associated Record**

    Displays the following fields:

    -   Associated table
    -   Associated record
    -   Experience Status Table
    -   Experience Status Record
-   **Details**

    Displays the following fields:

    -   Tagline
    -   Icon
    -   Title
    -   Description
    -   Pending State Title
    -   Pending State Description
    -   Record fields
    -   Footer
-   **Form**

    Displays the following fields:

    -   Form View
    -   Form fields
-   **Attachments**

    Displays the following fields:

    -   Attachment source
    -   Attachments read only
-   **Features**

    Displays the following fields:

    -   Show SLA
    -   Show Checklist
    -   Is Automated

## Instructional

If you choose the Instructional UI Layout, the following sections appear in the Activity Experience section for your activity definition:

-   **Associated Record**

    Displays the following fields:

    -   Associated table
    -   Associated record
    -   Experience Status Table
    -   Experience Status Record
-   **Details**

    Displays the following fields:

    -   Tagline
    -   Icon
    -   Title
    -   Description
    -   Footer
-   **Features**

    Displays the following field: Is Automated


## Knowledge

If you choose the Knowledge UI Layout, the following sections appear in the Activity Experience section for your activity definition:

-   **Associated Record**

    Displays the following fields:

    -   Associated table
    -   Associated record
    -   Experience Status Table
    -   Experience Status Record
-   **Knowledge**

    Displays the following fields:

    -   Knowledge Table
    -   Knowledge Record
-   **Details**

    Displays the following fields:

    -   Title
    -   Footer
-   **Features**

    Displays the following field: Is Automated


## List

If you choose the List UI Layout, the following sections appear in the Activity Experience section for your activity definition:

-   **Associated Record**

    Displays the following fields:

    -   Associated table
    -   Associated record
    -   Experience Status Table
    -   Experience Status Record
-   **Details**

    Displays the following fields:

    -   Tagline
    -   Icon
    -   Title
    -   Description
    -   Record fields
-   **List Details**

    Displays the following fields:

    -   List Title
    -   Table
    -   List Query
    -   UI View
    -   Columns
    -   Max Columns
    -   Row Count
-   **Features**

    Displays the following field: Is Automated


## Record

If you choose the Record UI Layout, the following sections appear in the Activity Experience section for your activity definition:

-   **Associated Record**

    Displays the following fields:

    -   Associated table
    -   Associated record
    -   Experience Status Table
    -   Experience Status Record
-   **Details**

    Displays the following fields:

    -   Tagline
    -   Icon
    -   Title
    -   Description
    -   Pending State Title
    -   Pending State Description
    -   Record fields
    -   Footer
-   **Form**

    Displays the following fields:

    -   Form View
    -   Form fields
-   **Attachments**

    Displays the following fields:

    -   Attachment source
    -   Attachments read only
-   **Features**

    Displays the following fields:

    -   Show SLA
    -   Show Checklist
    -   Is Automated

## Record generator

Activities with a Record generator UI Layout create a record during runtime, and redirect users to the record. For example, in this activity, after an agent selects the **Continue** button, a record is created and they are taken to that new record.

![Record generator activity during runtime](../images/record-generator-activity-pe.png)

If you choose the Record generator UI Layout, the following sections appear in the Activity Experience section for your activity definition:

-   Template Fields
-   Process Definition Scoped Name
-   Associated Table
-   Form View

## Guided Decision

**Note:** The Guided Decision UI Layout is available with a subscription to App Engine or Customer Service Management \(CSM\). For more information on how to enable this activity for use in Playbooks, see [Activate Playbooks for Customer Service Management \(CSM\)](activate-process-automation-designer.md#).

If you choose the Guided Decision UI Layout, the following fields appear in the Activity Experience section for your activity definition:

-   Decision Tree Execution
-   Decision Tree

**Parent Topic:**[Activity definitions](activity-definitions.md)

**Related topics**  


[Create an activity definition](../task/create-activity-definition.md)

[Create an action as an activity automation plan](../task/create-automation-plan.md)

