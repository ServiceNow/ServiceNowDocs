---
title: Enable record producer for external user
description: Enable the record producer to be available in the External Legal Service Center catalog.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/employee-service-management/external-legal-portal/lsd-ext-portal-config-intake-form.html
release: xanadu
product: External Legal Portal
classification: external-legal-portal
topic_type: task
last_updated: "2024-12-15"
reading_time_minutes: 1
breadcrumb: [Configuring up External Legal Service Center, External Legal Service Center, Legal Service Delivery, Employee Service Management]
---

# Enable record producer for external user

Enable the record producer to be available in the External Legal Service Center catalog.

## Before you begin

Role required: sn\_lg\_ops.legal\_admin

## About this task

You can create record producers for external users to submit requests through the External Legal Service Center. For more information, see [Managing record producers for legal services](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/employee-service-management/legal-request-management/record-producers-legal-services.md).

## Procedure

1.  Navigate to **All** &gt; **Legal Administration** &gt; **Record Producers**.

2.  Select the record producer from the list.

3.  Enable the record producer for external users.

    1.  Select Available For related list.

    2.  Select **Edit**.

    3.  Select **Users with sn\_lg\_ext\_portal.ext\_user**.

    4.  Select Add icon \(\[Omitted image "lsd-ext-portal-right-arrow.png"\] Alt text: Add icon\).

        **Users with sn\_lg\_ext\_portal.ext\_user** is moved to the Available For List.

    5.  Select **Save**.

4.  Remove external user role from not available list.

    1.  Select Not Available For related list.

    2.  Select **Edit**.

    3.  Select SNC External from the Not Available for list.

    4.  Select Remove icon \(\[Omitted image "lsd-ext-portal-left-arrow.png"\] Alt text: Add icon\).

5.  Select **Update** to save the record producer.

6.  For the record producer to be available in the catalog, configure ACLs for tables referenced from the record producers.

    For more information, see .


## Result

The record producer is available for the external users in the External Legal Service Center catalog.

## What to do next

If you want **Save as Draft** option to be enabled for a record producer, enable the system property **glide.sc.enable.save\_as\_draft.portal.elp**. For more information, see [Enable save as draft option for record producer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/employee-service-management/external-legal-portal/lsd-ext-portal-enable-draft.md).

