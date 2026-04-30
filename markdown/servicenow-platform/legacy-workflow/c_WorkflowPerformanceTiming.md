---
title: Workflow performance timing
description: The workflow engine can generate detailed performance timing data that is useful for troubleshooting slow workflows.Administrators can enable the collection of workflow run time metrics by setting Estimated Run Time \(ERT\) properties.Workflow performance timing is disabled by default. You can create a system property to enable it.
locale: en-US
release: zurich
product: Legacy Workflow
classification: legacy-workflow
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Classic Workflow, ServiceNow AI Platform Additional Capabilities, Extend ServiceNow AI Platform capabilities]
---

# Workflow performance timing

The workflow engine can generate detailed performance timing data that is useful for troubleshooting slow workflows.

**Important:** As of the Zurich release, new customers no longer receive the legacy workflows created and published by ServiceNow, Inc.. All legacy workflow functionality has been replaced by Workflow Studio content. Only customers who upgraded from prior versions retain the ability to use and edit existing legacy workflows. While all customers retain the ability to create legacy workflows, you are strongly encouraged to instead use Workflow Studio to create process automation content. Only Workflow Studio will receive new features and enhancements.

An administrator must enable this functionality.

When workflow performance timing is enabled, the workflow engine tracks key performance data, including various execution speed metrics. The Workflow Timing \[wf\_workflow\_timing\] table stores the data, with a record for each workflow context. The workflow timing record is updated when the workflow engine completes the workflow, waits for an activity to complete, or otherwise exits the workflow execution.

## Workflow estimated run time properties

Administrators can enable the collection of workflow run time metrics by setting Estimated Run Time \(ERT\) properties.

Administrators can use ERT metrics to determine if workflows are running longer or shorter than expected and to identify errors in workflow processing. The system displays run time metrics on the Workflow Operations Dashboard.

## Enable workflow performance timing

Workflow performance timing is disabled by default. You can create a system property to enable it.

### Before you begin

Role required: admin

### Procedure

1.  [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=zurich&pubname=zurich-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US)with the following specifications.

    |Field|Value|
    |-----|-----|
    |Name|glide.workflow.show\_timing|
    |Type|true \| false|
    |Value|true|


