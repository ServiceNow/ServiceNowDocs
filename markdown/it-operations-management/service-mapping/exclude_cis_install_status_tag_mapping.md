---
title: Exclude CIs based on their installation status in tag-based discovery
description: Use the CI installation status to create CI classes and exclude CIs from application services during tag-based discovery. By default, application services based on tags exclude CIs with the Retired or Absent install status. You can expand this list of excluded CIs to include additional installation statuses such as Pending install or Stolen.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/service-mapping/exclude\_cis\_install\_status\_tag\_mapping.html
release: zurich
product: Service Mapping
classification: service-mapping
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Tag-based discovery configuration, Advanced Service Mapping configuration, Configuring Service Mapping, Service Mapping, ITOM Visibility, IT Operations Management]
---

# Exclude CIs based on their installation status in tag-based discovery

Use the CI installation status to create CI classes and exclude CIs from application services during tag-based discovery. By default, application services based on tags exclude CIs with the Retired or Absent install status. You can expand this list of excluded CIs to include additional installation statuses such as Pending install or Stolen.

## Before you begin

Learn about default feature configuration in [Tag-based discovery in Service Mapping](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/service-mapping/tag-based-mapping.md).

**Note:** Starting with Service Mapping Plus version 1.16.3, take advantage of the Tag-based Service Mapping workspace to efficiently map your application services. .

Role required: service\_mapping\_admin

## Procedure

1.  Navigate to **Service Mapping** &gt; **Administration** &gt; **Properties**.

2.  Enter values for installation statuses into the deny list that controls which CIs to exclude from tag-based mapping based on install status.

    Use commas to separate the values. \[Omitted image "service-mapping-properties-deny-list.png"\] Alt text: Deny list used to define install statuses and exclude CIs with these statuses from tag-based discovery.

3.  Click **Save**.


## What to do next

If you refine the default configuration after creating appliations based on tags, see [Recalculate previously created application services](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/service-mapping/recalculate_application_services.md) for the next steps.

**Parent Topic:**[Tag-based discovery configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/service-mapping/tag_discovery_configuration.md)

