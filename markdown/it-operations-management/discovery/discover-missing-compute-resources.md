---
title: Discover missing compute resources
description: Use the Discovery Admin Workspace to identify compute resources that weren't discovered recently. Run a quick discovery to update the resource's data. If a resource isn't discoverable, ignore the resource and exclude it from the report. This procedure helps you maximize the use of your resources.
locale: en-US
release: australia
product: Discovery
classification: discovery
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [Discovery, Admin, Workspace]
breadcrumb: [Discovery monitoring and issue resolution, Using Discovery, Discovery, ITOM Visibility, IT Operations Management]
---

# Discover missing compute resources

Use the Discovery Admin Workspace to identify compute resources that weren't discovered recently. Run a quick discovery to update the resource's data. If a resource isn't discoverable, ignore the resource and exclude it from the report. This procedure helps you maximize the use of your resources.

## Before you begin

Role required: discovery\_admin or admin

## About this task

By default, the report provides the following information:

-   Resources discovered by the ServiceNow® platform and ServiceWatch Suite.
-   Resources that weren't discovered since the previous discovery ran 14 days previously or that have no discovery date in the **Most recent discovery** field.
-   Resources that don't have an **ignore from report** tag.

## Procedure

1.  Navigate to **Workspaces** &gt; **Discovery Admin Workspace** &gt; **Insights** &gt; **Missing compute resources from Discovery**.

2.  Run a quick discovery for a resource.

    1.  In the list, select the resource.

    2.  Select **Quick discovery**.

    3.  Select a MID Server to run discovery.

        The **Enter IP List** is automatically populated.

    4.  In the **MID Selection Method** and **MID Server** fields, select the preferred options.

        For more information, see [MID Server selection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/mid-server/c_MIDServerSelector.md).

    5.  Select **Run discovery**.

3.  If the resource's discovery failed, ignore the resource and exclude it from the report.

    If you successfully ignore a resource, a green banner appears to indicate that the resource is ignored from the report. When the resource is ignored, it's removed from the **Missing compute resources** report.

    1.  In the list, select the resource.

    2.  Select **Ignore from report**.

4.  If you want to enable the discovery for a previously ignored resource, remove the **ignore from the report** tag.

    1.  Navigate to **All** and type in the filter `cmdb_ci_server.list`.

    2.  Personalize the list to include the **Tags** column, using the settings button.

    3.  Search for the resource name.

    4.  In the **Tags** field, select the removal option.


## Result

If the quick discovery was successful, the instance redirects to the **Discovery status** dashboard. When the resource is discovered, it's removed from the **Missing compute resources** report and is listed in the Server \[cmdb\_ci\_server\] table.

