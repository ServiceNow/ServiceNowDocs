---
title: Automatically match to an existing model using the legacy Software Asset Management plugin
description: The automatic matching feature in the legacy Software Asset Management \(com.snc.software\_asset\_management\) plugin allows you to match a software discovery model to an existing software model.
locale: en-US
release: zurich
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Software discovery models in the legacy Software Asset Management plugin, Legacy Software Asset Management plugin, ITSM Software Asset Management, Asset Management, IT Service Management]
---

# Automatically match to an existing model using the legacy Software Asset Management plugin

The automatic matching feature in the legacy Software Asset Management \(com.snc.software\_asset\_management\) plugin allows you to match a software discovery model to an existing software model.

## Before you begin

Role required: sam

## Procedure

1.  Navigate to **All** &gt; **Software Asset** &gt; **Reconciliation** &gt; **Discovery models** and open a model.

2.  Clear the **Software model** field.

3.  Click an entry in the **Publisher** column.

4.  Click **Match model**.

    The system searches for the best match from existing models. If a match is found, the system automatically adds the name to the **Software model** field and selects the **Automatically matched** check box. If a match is not found, a **No match found** message is displayed, and two related links appear, allowing you to create a new model. No change occurs if the system has already made a match.

5.  If no match is found, create a new model.

    If a model is already matched, then the automatic matching feature does not run.

    The automatic matching feature can also be used when you insert a new discovery model record or if you modify and update an existing discovery model. If automatic matching is run, all software installations and usages that reference the discovery model will have their **Inferred suite** and **Cached** fields cleared.

    For more information on software installation and usage records, see [Determine where software is installed](../concept/c_DeterminWhereSWInstalled.md).


**Parent Topic:**[Software discovery models in the legacy Software Asset Management plugin](../concept/c_UsingSoftwareDiscoveryModels.md)

