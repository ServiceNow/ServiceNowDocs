---
title: Create the Open Incident workflow in the Asset Refresh topic
description: Each Decision branch introduces additional workflows. After creating our main Asset Refresh workflow, we need to ensure that the user can get help if something goes wrong. In this example, we will help the user create an incident.
locale: en-US
release: yokohama
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Example Asset Refresh Virtual Agent conversation with notifications, Exploring Virtual Agent, Virtual Agent, Conversational Interfaces]
---

# Create the Open Incident workflow in the Asset Refresh topic

Each Decision branch introduces additional workflows. After creating our main Asset Refresh workflow, we need to ensure that the user can get help if something goes wrong. In this example, we will help the user create an incident.

## Before you begin

[Create the Asset Refresh topic in Virtual Agent Designer](create-example-conv-asset-refresh.md)

Role required: virtual\_agent\_admin or admin

## Procedure

1.  Open the Asset Refresh topic in Virtual Agent Designer.

2.  Return to the **false** decision branch after the Asset Check Boolean question that you asked the user.

    1.  From the Components area, drag a Text bot response node onto the **false** branch on the canvas.

    2.  Select the node to view the properties palette.

    3.  Enter a name for the node and the response you want to display to the user.

        For example, name the node `Open Incident`. For the **Response message**, type `Since you no longer have the device, we need to open an incident.`

        ![The Open Incident text bot response appears in the false decision flow for the Boolean question. The user will be prompted to open an incident.](../images/crawl-ex-open-incident-txt.png)

3.  Add a Topic Block utility to node to create the incident.

    1.  From the Components area, drag a Topic Block utility node onto the canvas.

    2.  In the properties palette, select **Create Incident** for the Topic block.

    3.  Under Input mapping, use dot-walking to specify the **caller** and **short\_description** parameters.

        -   For the caller, specify Input Variables &gt; User.
        -   For the short description, specify Input Variables &gt; Asset Lookup &gt; Asset tag.
        ![Use dot-walking to designate input mapping variables for the Incident. User is the session user, and the Asset tag is derived from the previous Asset Lookup node.](../images/crawl-ex-incident-input-vars.png)

    4.  Under Output mapping, make sure to enable the created\_incident\_sys\_id variable.

        ![Select the Enable box for created_incident_sys_id to pass the Incident ID back to Virtual Agent.](../images/crawl-ex-incident-output-var.png)

4.  Drag this flow's arrow to the End node to complete this part of the workflow.

5.  Select **Save**.


## What to do next

[Create the More Information workflow in the Asset Refresh topic](create-example-asset-refresh-flow3.md)

