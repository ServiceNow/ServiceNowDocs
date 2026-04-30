---
title: Customize a relationship graph
description: Visualize and analyze security incidents and their associated data in a relationship graph.
locale: en-US
release: yokohama
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-04-21"
reading_time_minutes: 1
breadcrumb: [Viewing incident details with a relationship graph, Working with Security Incident Records, Use, Security Incident Response Workspace, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Customize a relationship graph

Visualize and analyze security incidents and their associated data in a relationship graph.

## Before you begin

Role required: sn\_si.admin

## Procedure

1.  Navigate to **Workspaces** &gt; **Security Incident Response Workspaces** &gt; **Administration**.

2.  Select **Relationship Graph**, and then **Relationship Graph Configurations**.

3.  Select **New**.

4.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Related Table Name|The table from which you want to fetch the security incident observable data, such as the Associate observable \[sn\_ti\_observable\] table or Security Incident \[sn\_si\_incident\] table.|
    |Node Label|The node label for the observable that appears on the relationship graph. The automatically supplied value depends on the selected related table.|
    |Active|Option to enable the configuration.|
    |Data Node Label|The primary label and secondary label to display on the node for the selected related list.|
    |Default Visible|Option to display the data node label.|
    |Relationship Label|The relationship between a node and link node to display on the relationship graph.|

5.  Select **Save**.


**Parent Topic:**[Viewing incident details with a relationship graph](../concept/sir-relationship-graph.md)

