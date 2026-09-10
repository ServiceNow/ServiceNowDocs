---
title: Create a UX cross-experience route
description: Create a UX cross-experience route to share a record page from one workspace so it opens automatically when the same record type is viewed in another workspace.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/service-operations-workspace/create-ux-cross-experience-route.html
release: australia
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: task
last_updated: "2026-09-02"
reading_time_minutes: 1
keywords: [UX cross-experience route, sys\_ux\_interoperable\_route]
breadcrumb: [Sharing record pages from Service Operations Workspace across workspaces, Configuring Service Operations Workspace for ITSM to improve your experience, Configuring Service Operations Workspace for ITSM, Service Operations Workspace for ITSM, IT Service Management]
---

# Create a UX cross-experience route

Create a UX cross-experience route to share a record page from one workspace so it opens automatically when the same record type is viewed in another workspace.

## Before you begin

Before you begin, identify the record page you want to share and the workspace where it should open.

Role required: admin.

## Procedure

1.  Navigate to the UX cross-experience route list.

    In the filter navigator, enter `sys_ux_interoperable_route.list`.

2.  Select **New**.

3.  Specify the record page to share and the workspace where it should open.

    For example, configure the Service Operations Workspace record page so it opens in the CSM Workspace.

4.  Add a usage condition to limit when the shared page opens.

    For example, enter `table=incident` so the page opens only when incident records are viewed.

5.  Submit the record.


## What to do next

This configuration is also visible in UI Builder.

**Parent Topic:**[Sharing record pages from Service Operations Workspace across workspaces](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/service-operations-workspace/sow-share-record-pages-other-workspaces.md)

