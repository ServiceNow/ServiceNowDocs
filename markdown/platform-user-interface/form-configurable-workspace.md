---
title: Forms
description: Learn about the components in UI Builder that enable admins to create and customize forms for a Configurable Workspace.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Explore, Configurable Workspace UI, Configure UIs and portals, Configure user experiences]
---

# Forms

Learn about the components in UI Builder that enable admins to create and customize forms for a Configurable Workspace.

## Forms overview

A [form](../configurable-workspace-glossary.md#) is a content page that displays fields and values for a single record from a database table.

Within a Configurable Workspace record, the form enables agents to view, enter, and update details about the record.

For example, an agent can update the short description, priority, assignment group, and status within an incident record form.

![Form on a Configurable Workspace record](../image/configurable-workspace-form-record.png)

## Form component bundle

The Form component bundle in UI Builder displays record data and enables interaction with fields. It includes the Form component connected to the Form controller.

The standard record page template in UI Builder uses the Form component bundle alongside other components that create a record page. While the standard record page template offers a useful starting point, admins can customize or build their own record pages as needed.

The Form component bundle is configured and customized by admins in UI Builder. For information on Form component configurations, see [Form UIB Setup](https://developer.servicenow.com/dev.do#!/reference/next-experience/yokohama/now-components/form%20record%20page/uib-setup).

## Related lists

While the form displays field-level data for a single record, [related lists](../configurable-workspace-glossary.md#) show records from other tables that are linked to the current record like tasks or associated incidents.

The standard record page template in UI Builder often displays related lists as tabs alongside the form that provides details about a record.

The Record List component bundle enables related lists as a list type and is configured and customized by admins in UI Builder.

