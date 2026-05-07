---
title: Create a diagram for a business application in the EA Workspace
description: Create a diagram for your business application hierarchy and associate it with an architectural artifact.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Working with an application portfolio, Working with Portfolio list view, Managing Enterprise Architecture Workspace, Enterprise Architecture Workspace, Enterprise Architecture]
---

# Create a diagram for a business application in the EA Workspace

Create a diagram for your business application hierarchy and associate it with an architectural artifact.

## Before you begin

For creating the diagram using the ServiceNow Enterprise Modeling and Visualization, you must activate the following ServiceNow Store applications. For more information, see [Exploring Enterprise Modeling and Visualization in the EA Workspace](../../concept/eaw-concept/eaw-modeling.md).

-   Enterprise Modeling and Visualization \(app-modelling-tool\)
-   Diagram Builder \(app-diagram-builder\)
-   APM Modelling tool Common \(app-modelling-tool-common\)

For creating the diagram using the Lucidchart, you must activate the following ServiceNow Store applications and establish a connection with Lucid:

-   Lucidchart Diagramming Spoke \[sn\_lucdchart\_spoke\] \(v 1.1.1 or later\)
-   Lucidchart Integration \[sn\_lcdchart\_int\] \(v 2.3.0 or later\)
-   Personal Authentication \[sn\_ihub\_personal\_auth\] \(v 27.0.0 or later\)

To establish a connection with Lucid, see [Create OAuth 2.0 Client in Lucidchart](https://www.servicenow.com/docs/access?context=set-up-lucidchart&version=australia&pubname=australia-integrate-applications&ft:locale=en-US) and [Create a connection and credential alias for the Lucidchart diagramming spoke](https://www.servicenow.com/docs/access?context=create-conn-cred-lucidchart&version=australia&pubname=australia-integrate-applications&ft:locale=en-US).

Role required: Member of the Enterprise Architect group

## Procedure

1.  Navigate to **Workspaces** &gt; **Enterprise Architecture Workspace** &gt; **Portfolio**.

2.  Select the expand row icon \(![Expand Row icon](../../image/ExpandIcon.png)\) next to **Application Portfolio**.

3.  Select **Business Applications**.

4.  Select a business application to open it.

5.  Select the more actions menu \(![More Actions menu](../../image/icon-three-dot-menu.png)\) and select **Create Diagram**.

6.  On the Create Diagram form, fill in the fields.

    For field information, see [Create diagram form for a business application](../../reference/eaw-reference/eaw-create-diagram-ba-form.md).

    **Note:** For Lucidchart, use the authorization link on the Create Diagram window, to generate an authentication token and fetch your Lucid folders to save the diagram. Ensure that you have at least one folder created in the My documents folder of your computer.

7.  Select **Create Diagram**.


## Result

After a successful submission, a link to the newly created diagram appears on top of the screen. You can select the link to navigate to the diagram. The Architectural Artifacts page shows the link to the diagram and an artifact name associated with it. You can select the respective link to access the artifact or diagram.

**Parent Topic:**[Working with an application portfolio](../../concept/eaw-concept/eaw-work-with-application-portfolio.md)

**Related topics**  


[Create a Lucidchart diagram for a business application in the EA Workspace](eaw-create-lucid-diagram-ba.md)

[View roadmap of a business application](eaw-view-roadmap-ba.md)

[View business capabilities associated with a business application](eaw-view-business-capabilities-assoc-with-ba.md)

[Add or edit a business application](eaw-create-business-app.md)

[Manage information objects of a business application in EA Workspace](eaw-associate-info-obj-ba.md)

[Remove architectural artifacts associated with a business application](eaw-unassign-archi-artfct-assoc-ba.md)

[Create an architectural artifact and associate it with a business application](eaw-assoicate-artifact-ba.md)

[View architectural artifacts associated with a business application](eaw-view-archi-artfct-assoc-with-ba.md)

[Remove business capabilities associated with a business application](eaw-unassign-business-capabilities-from-ba.md)

[Open business application form in Core UI from EA Workspace](view-ba-form-in-coreui.md)

[View all business applications](view-all-business-apps.md)

[View a unified map for a business application](eaw-open-map-ba.md)

[Add an existing architectural artifact to a business application](eaw-add--existing-archi-artfct-to-a-ba.md)

[Add an existing business capability to a business application](eaw-add-existing-business-capability-to-ba.md)

