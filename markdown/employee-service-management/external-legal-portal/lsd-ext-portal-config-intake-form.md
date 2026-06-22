---
title: Enable record producer for external user
description: External users can submit requests through the External Legal Service Center catalog after you configure the record producer availability, access roles, and catalog topics.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/employee-service-management/external-legal-portal/lsd-ext-portal-config-intake-form.html
release: zurich
product: External Legal Portal
classification: external-legal-portal
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuring up External Legal Service Center, External Legal Service Center, Legal Service Delivery, Legal and Contract Operations, Employee Service Management]
---

# Enable record producer for external user

External users can submit requests through the External Legal Service Center catalog after you configure the record producer availability, access roles, and catalog topics.

## Before you begin

Role required: sn\_lg\_ops.legal\_admin

## About this task

You can create record producers for external users to submit requests through the External Legal Service Center. For more information, see [Managing record producers for legal services](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/legal-request-management/record-producers-legal-services.md).

## Procedure

1.  Navigate to **All** &gt; **Legal Administration** &gt; **Record Producers**.

2.  Select the record producer from the list.

3.  Enable the record producer for external users.

    1.  Select the Available For related list.

    2.  Select **Edit**.

    3.  Select **Users with sn\_lg\_ext\_portal.ext\_user**.

    4.  Select Add icon \(\[Omitted image "lsd-ext-portal-right-arrow.png"\] Alt text: Add icon\).

        **Users with sn\_lg\_ext\_portal.ext\_user** is moved to the Available For List.

    5.  Select **Save**.

4.  Remove the external user role from the Not Available For related list.

    1.  Select the Not Available For related list.

    2.  Select **Edit**.

    3.  Select SNC External from the list.

    4.  Select Remove icon \(\[Omitted image "lsd-ext-portal-left-arrow.png"\] Alt text: Add icon\).

5.  Assign the record producer to the External Legal Service Center catalog topic.

    1.  Select the Assigned Topics related list.

    2.  Select **Add**.

    3.  From the Taxonomy list, select External Legal Service Center.

    4.  Select **Browse Legal**.

    5.  Select **OK**.

6.  Select **Update** to save the record producer.

7.  Configure ACLs for tables referenced from the record producers to make is available in the catalog.

    For more information, see [Configure an ACL rule](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-security/access-control/t_CreateAnACLRule.md).


## Result

The record producer is available for the external users in the External Legal Service Center catalog.

## What to do next

If you want **Save as Draft** option to be enabled for a record producer, enable the system property **glide.sc.enable.save\_as\_draft.portal.elp**. For more information, see [Enable save as draft option for record producer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/external-legal-portal/lsd-ext-portal-enable-draft.md).

