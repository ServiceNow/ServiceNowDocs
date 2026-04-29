---
title: Manually normalize a software discovery model in Software Asset Management classic
description: You can edit a software discovery model to manually normalize discovered software that has not been fully normalized \(partially normalized, publisher normalized, or match not found\) on the Software Discovery Models form so that it can be reconciled.
locale: en-US
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [View normalization suggestions in Software Asset Management classic, Using Software Asset Management classic, Software Asset Management, IT Asset Management]
---

# Manually normalize a software discovery model in Software Asset Management classic

You can edit a software discovery model to manually normalize discovered software that has not been fully normalized \(partially normalized, publisher normalized, or match not found\) on the Software Discovery Models form so that it can be reconciled.

## Before you begin

Role required: sam\_user

## About this task

If the information automatically added to the software discovery model is incomplete, you can add the missing fields to manually normalize the software discovery model.

## Procedure

1.  Navigate to **All** &gt; **Software Asset** &gt; **Discovery** &gt; **Discovery models** and open a discovery model record that has a normalization status of Partially Normalized, Publisher Normalized, or Match Not Found.

2.  Fill in the **Publisher**, **Product**, and **Version** fields, as appropriate.

    You can create a [custom product](t_AddACustomProduct.md) from the Product lookup list, if desired.

3.  Select **Save**.

    The normalization status is set to Manually Normalized.

4.  To revert normalization, select **Revert Normalization**.

    **Note:** Discovery models with a status of Normalized, Partially Normalized, or Publisher Normalized revert to the status of Match Not Found. Discovery models with a status of Manually Normalized and discovery models that have been normalized using pattern rules cannot be reverted.

    Fields are reset to their original values, and any rules associated with the software discovery model are deactivated.


**Parent Topic:**[View normalization suggestions in Software Asset Management classic](view-norm-suggestions-sam.md)

