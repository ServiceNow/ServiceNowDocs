---
title: Create data structure
description: Organize multiple data variables into a structure to process them as a unit and identify the individual items within it.
locale: en-US
release: xanadu
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Complex data, Building actions, Using Workflow Studio, Workflow Studio, Build workflows]
---

# Create data structure

Organize multiple data variables into a structure to process them as a unit and identify the individual items within it.

## Before you begin

-   Role required: action\_designer, flow\_designer, or admin
-   [Set up an application in Guided Application Creator](https://www.servicenow.com/docs/access?context=set-up-app&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US) to store Workflow Studio content.
-   [Create an action in Workflow Studio](create-action.md) or [Create a subflow in Workflow Studio](create-subflow.md)

## About this task

A data structure is a collection of related data elements organized into a hierarchy. Each element in a data structure has its own data type and its own unique position in the hierarchy.

## Procedure

1.  Create a data variable.

    | | |
    |---|---|
    |**Action or subflow input**|Click **Create Input**|
    |**Action or subflow output**|Click **Create Output**|
    |**XML parser step**|See [XML parser step](https://www.servicenow.com/docs/access?context=xml-parser-step-action-designer&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US)|

2.  Set **Type** to **Object**.

    The top level of a data structure hierarchy must be an Object variable.

3.  Click the **Add Child Item** icon.

    Workflow Studio adds a child data variable to the bottom of the object list.

    **Note:** You can insert a child item variable between existing variables by hovering your mouse pointer between two variables, and click the insert item icon \(![Insert item icon](../images/insert-child-icon.png)\) that appears.

    **Note:** When hovering your mouse pointer between a child and sibling variable, you will see a add child icon \(![Insert child item icon](../images/insert-item-icon.png)\). Click the left side of the icon to add a new sibling variable to the child's parent, or the right side to add another child variable under the current variable.

4.  Set the child variable **Label** and **Type**.

    To add another branch to the data structure hierarchy, set the Type to Object.

5.  Repeat steps 3-4 for each data variable in the hierarchy.


## What to do next

Use the data structure to populate action, step, or subflow inputs. If you can reuse the data structure, save it as a template.

**Parent Topic:**[Complex data](../concept/complex-data.md)

