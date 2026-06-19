---
title: Include CIs based on classes in tag-based discovery
description: Use CI classes to identify which CIs Service Mapping includes in application services during tag-based discovery. By default, this list appears empty and includes all CIs belonging to all CI classes. Define CI classes and allow only CIs belonging to these classes or their extensions to participate in tag-based discovery.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/service-mapping/include\_cis\_tag\_discovery\_configuration.html
release: zurich
product: Service Mapping
classification: service-mapping
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Tag-based discovery configuration, Advanced Service Mapping configuration, Configuring Service Mapping, Service Mapping, ITOM Visibility, IT Operations Management]
---

# Include CIs based on classes in tag-based discovery

Use CI classes to identify which CIs Service Mapping includes in application services during tag-based discovery. By default, this list appears empty and includes all CIs belonging to all CI classes. Define CI classes and allow only CIs belonging to these classes or their extensions to participate in tag-based discovery.

## Before you begin

Learn about default feature configuration in [Tag-based discovery in Service Mapping](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/service-mapping/tag-based-mapping.md).

**Note:** Starting with Service Mapping Plus version 1.16.3, take advantage of the Tag-based Service Mapping workspace to efficiently map your application services. .

Role required: service\_mapping\_admin

## Procedure

1.  Navigate to **Service Mapping** &gt; **Administration** &gt; **Properties**.

2.  Enter CI classes, separated by commas, in the allow list that controls which tagged CIs participate in tag-based mapping.

    \[Omitted image "service-mapping-properties-allow-list.png"\] Alt text: Allow list used to define CI classes and control which CIs participate in tag-based mapping

3.  Click **Save**.


## What to do next

If you refine the default configuration after creating appliations based on tags, see [Recalculate previously created application services](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/service-mapping/recalculate_application_services.md) for the next steps.

**Parent Topic:**[Tag-based discovery configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/service-mapping/tag_discovery_configuration.md)

