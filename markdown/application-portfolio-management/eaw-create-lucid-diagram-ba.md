---
title: Create a Lucidchart diagram for a business application in the EA Workspace
description: Create a diagram Lucidchart for your business application hierarchy and associate it with an architectural artifact.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Working with an application portfolio, Portfolio list view, Enterprise Architecture Workspace, Enterprise Architecture \(formerly Application Portfolio Management\), Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# Create a Lucidchart diagram for a business application in the EA Workspace

Create a diagram Lucidchart for your business application hierarchy and associate it with an architectural artifact.

## Before you begin

Ensure the following ServiceNow Store apps are installed:

-   Lucidchart Diagramming Spoke \[sn\_lucdchart\_spoke\] \(v 1.1.1\)
-   Lucidchart Integration \[sn\_lcdchart\_int\] \(v 2.3.0\)
-   Personal Authentication \[sn\_ihub\_personal\_auth\] \(v 27.0.0\)

Ensure a connection is established with Lucid. For details, see [Create OAuth 2.0 Client in Lucidchart](https://www.servicenow.com/docs/access?context=set-up-lucidchart&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US) and [Create a connection and credential alias for the Lucidchart diagramming spoke](https://www.servicenow.com/docs/access?context=create-conn-cred-lucidchart&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US).

Role required: sn\_apm.apm\_analyst

## Procedure

1.  Navigate to **Workspaces** &gt; **Enterprise Architecture Workspace** &gt; **Portfolio**.

2.  Select the expand row icon \(![Expand Row icon](../../image/ExpandIcon.png)\) next to **Application Portfolio**.

3.  Select **Business Applications**.

4.  Select a business application to open it.

5.  Select the more actions menu \(![More Actions menu](../../image/icon-three-dot-menu.png)\) and select **Create Diagram**.

6.  On the Create Diagram form, fill in the fields.

    **Note:** Use the authorization link on the Create Diagram window, to generate an authentication token and fetch your Lucid folders to save the diagram.

    For field information, see [Create a diagram for a business application in the EA Workspace](eaw-create-diagram-ba.md).

    **Note:** Ensure that you have at least one folder created in the My documents folder of your computer.

7.  Select **Create Diagram**.


## Result

After a successful submission, a link to the newly created Lucid diagram appears on top of the screen. You can select the link to navigate to the diagram. The Architectural Artifacts page shows the link to the Lucidchart diagram and an artifact name associated with it. You can select the respective link to access the artifact or diagram.

**Parent Topic:**[Working with an application portfolio](../../concept/eaw-concept/eaw-app-portfolio.md)

