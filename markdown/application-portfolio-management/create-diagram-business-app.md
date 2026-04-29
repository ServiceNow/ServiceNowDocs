---
title: Create a diagram for a business application
description: Create a diagram in for your business application hierarchy and associate it with an architectural artifact. Use the ServiceNow Enterprise Modeling and Visualization or Lucidchart to create a diagram for your business hierarchy.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Using Enterprise Architecture \(formerly Application Portfolio Management\), Enterprise Architecture \(formerly Application Portfolio Management\), Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# Create a diagram for a business application

Create a diagram in for your business application hierarchy and associate it with an architectural artifact. Use the ServiceNow Enterprise Modeling and Visualization or Lucidchart to create a diagram for your business hierarchy.

## Before you begin

**Important:**

Starting with the Xanadu release, the legacy create diagram feature has been deprecated from Enterprise Architecture \(formerly Application Portfolio Management\). However, if you’re an existing user of Enterprise Architecture \(formerly Application Portfolio Management\), you can still use the legacy create diagram feature. If you’re a new activation user, the legacy create diagram feature isn’t available.

You can leverage the same functionality by using the Enterprise Architecture Workspace. To learn more, see [Create a Lucidchart diagram for a business application in the EA Workspace](eaw-task/eaw-create-lucid-diagram-ba.md).

For creating the diagram using the ServiceNow Enterprise Modeling and Visualization, you must activate the following ServiceNow Store applications. For more information, see [Exploring Enterprise Modeling and Visualization in the EA Workspace](../concept/eaw-concept/eaw-modeling.md).

-   Enterprise Modeling and Visualization \(app-modelling-tool\)
-   Diagram Builder \(app-diagram-builder\)
-   APM Modelling tool Common \(app-modelling-tool-common\)

For creating the diagram using the Lucidchart, you must activate the following ServiceNow Store applications and establish a connection with Lucid:

-   Lucidchart Diagramming Spoke
-   Lucidchart Integration

To establish a connection with Lucid, see [Create OAuth 2.0 Client in Lucidchart](https://www.servicenow.com/docs/access?context=set-up-lucidchart&version=australia&pubname=australia-integrate-applications&ft:locale=en-US) and [Create a connection and credential alias for the Lucidchart diagramming spoke](https://www.servicenow.com/docs/access?context=create-conn-cred-lucidchart&version=australia&pubname=australia-integrate-applications&ft:locale=en-US).

Role required: Member of the Enterprise Architect group

## Procedure

1.  Navigate to the Business Application diagrams.

    -   Navigate to **All** &gt; **Enterprise Architecture** &gt; ** Architectural Artifacts** &gt; ** Diagrams**.
    -   Navigate to **All** &gt; **Enterprise Architecture** &gt; **Application Portfolio** &gt; **All Business Applications** and select a Business Application.
2.  Click **Create Diagram**.

3.  On the form, fill in the fields.

    For field information, see [Create diagram form for business application](../reference/create-lucidchart-diagram-form.md).

    **Note:** For Lucidchart, use the authorization link on the Create Diagram window, to generate an authentication token and fetch your Lucid folders to save the diagram.

4.  Click **Create Diagram**.


## Result

After a successful submission, a link to the newly created diagram appears on top of the screen. You can select the link to navigate to the diagram. The Architectural Artifacts page shows the link to the diagram and an artifact name associated with it. You can select the respective link to access the artifact or diagram.

**Parent Topic:**[Using Enterprise Architecture \(formerly Application Portfolio Management\)](../concept/using-apm.md)

