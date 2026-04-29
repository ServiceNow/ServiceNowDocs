---
title: Create a relationship graph for an incident
description: Create a node relationship graph in Security Incident Response so you can better analyze a security incident by correlating it with malicious observables, configuration items \(CIs\), similar security incidents \(SIRs\), response tasks, and other related information.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Viewing incident details with a relationship graph, Working with Security Incident Records, Use, Security Incident Response Workspace, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Create a relationship graph for an incident

Create a node relationship graph in Security Incident Response so you can better analyze a security incident by correlating it with malicious observables, configuration items \(CIs\), similar security incidents \(SIRs\), response tasks, and other related information.

## Before you begin

Role required: sn\_si.analyst

## About this task

For information about how to create a customized relationship graph rather than using a predefined graph, see [Customize a relationship graph](create-relationship-graph-config.md).

**Note:** Changes to the relationship graph aren’t saved automatically.

## Procedure

1.  Navigate to **Workspaces** &gt; **Security Incident Response Workspace**.

2.  Open a security incident.

3.  Select the **Relationship Graph** tab.

4.  In the relationship graph, select and hold \(or right-click\) the parent node, and then select **Add Nodes**.

5.  Select one or more category nodes to display in the relationship graph, such as Related users, Affected CIs, similar security incidents \(SIRs\), or Affected Users.

    **Note:** You can select multiple category nodes.

6.  Select and hold \(or right-click\) a category node and select **Link Nodes** to add data associated with the category node.

    **Note:** You can apply filters to reduce the number of items in the list.

    A list of all related records for the selected category node appears. For example, if you select **Affected Users** from the node category, a list of all the users affected by this incident displays.

7.  Select the desired records from the list and select **Add**.

8.  Select **Add**.

9.  Clear changes if necessary by selecting **Refresh**.

10. Select **Save**.

    **Note:** Changes to filters are also saved when you save the relationship graph.

11. Display the details of a subnode.

    1.  Select a subnode.

    2.  Select **Show Details**.

12. Download the map to your system.

    1.  If only a portion of the map is visible on the screen and you want the whole screen to be included in the PDF, select the Fit to screen icon \(![Fit to screen icon](../image/fit-to-screen-sir.png)\).

        **Note:** Only the portion of the map that appears on the screen is included in the PDF file.

    2.  Select the export map icon \(![Export relationship graph icon](../image/export-node-graph-icon.png)\).


## Video showing how to edit a relationship graph to add category nodes and subnodes

Video showing how to create a relationship node graph for an incident 

**Parent Topic:**[Viewing incident details with a relationship graph](../concept/sir-relationship-graph.md)

