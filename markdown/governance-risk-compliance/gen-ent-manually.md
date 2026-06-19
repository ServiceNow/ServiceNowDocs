---
title: Add entities manually
description: Add entities manually from the Operational Resilience Workspace as an optional step once pillars, entity types, and entity filters are active. Entities are individual records matching your filter criteria. Automatic generation is recommended for most scenarios; manual addition is available for exceptions.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/gen-ent-manually.html
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Setting up pillars, entity types, entity filters, and entities, Configure, Operational Resilience, Governance, Risk, and Compliance]
---

# Add entities manually

Add entities manually from the Operational Resilience Workspace as an optional step once pillars, entity types, and entity filters are active. Entities are individual records matching your filter criteria. Automatic generation is recommended for most scenarios; manual addition is available for exceptions.

## Before you begin

Role required: sn\_oper\_res.admin, sn\_oper\_res.manager

## About this task

For automatic generation of the entities, see [Generate entities automatically using a scheduled job](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/gen-ent-auto.md).

## Procedure

1.  Navigate to the **Workspaces** &gt; **Operational Resilience Workspace** &gt; **List view** and select a business service or business process for which you want to generate entities.

2.  To add a business service or business process, select **New**.

    The example shows how to add a business service from the Operational Resilience Workspace.

    \[Omitted image "add-ent-manually-opres-ws-1.png"\] Alt text: Add a business service.

3.  On the form, fill in the fields.

    The form for creating a business service is shown in the example. For information on the fields in the record form, see [Create New Business Service form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/create-new-business-service-form.md) and [Create New Business Process form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/create-new-business-process-form.md).

    \[Omitted image "add-ent-manually-opres-ws-2.png"\] Alt text: Create a new business service.

4.  Select **Save**.

5.  To add a service or process to Operational Resilience reporting and create entities for the record manually, select **Add to OpRes reporting** in the record header.

    The examples show the **Add to OpRes reporting** button from the Operational Resilience Workspace.

    \[Omitted image "add-ent-manually-opres-ws-3.png"\] Alt text: Add to OpRes reporting button.

    A message is displayed that the service is added to Operational Resilience reporting. The record now appears as an entity in Operational Resilience.

    **Note:** Use manual addition only for exceptions or one-off additions that don't fit the filter criteria.

6.  To view the entity record, select **Go to entity** from the record header.


