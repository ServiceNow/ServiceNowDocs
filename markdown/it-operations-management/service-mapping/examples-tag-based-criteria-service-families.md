---
title: Example definitions for service families in tag-based mapping
description: When preparing to map application services based on tags, create tag categories that contain tags with similar use. Define a tag-based service family and the tags you want to use for mapping. In addition to tag categories, you can also define tag values to narrow the criteria for the service candidates created by Service Mapping. Use these examples for guidance.
locale: en-US
release: zurich
product: Service Mapping
classification: service-mapping
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Service Mapping reference, Service Mapping, ITOM Visibility, IT Operations Management]
---

# Example definitions for service families in tag-based mapping

When preparing to map application services based on tags, create tag categories that contain tags with similar use. Define a tag-based service family and the tags you want to use for mapping. In addition to tag categories, you can also define tag values to narrow the criteria for the service candidates created by Service Mapping. Use these examples for guidance.

For detailed information about defining service families in tag-based mapping, see [Prepare for mapping application services based on tags](../task/prepare-map-service-tag.md).

**Note:** Starting with Service Mapping Plus version 1.16.3, take advantage of the Tag-based Service Mapping workspace to efficiently map your application services. .

<table id="table_zbx_gvs_djb"><thead><tr><th>

Definitions for service family

</th><th>

Category

</th><th>

Key

</th><th>

Value \(optional\)

</th><th>

Result

</th></tr></thead><tbody><tr><td>

Example 1: one tag category, no values

</td><td>

Environment

</td><td>

Env

</td><td>

Not defined

</td><td>

Service Mapping creates a service candidate for each tag value for the Env key. Each service candidate contains only CIs with the same value for the Env key.

</td></tr><tr><td>

Example 2: one tag category, one value

</td><td>

Environment

</td><td>

Env

</td><td>

Production

</td><td>

Service Mapping creates the service candidate containing only CIs that have the Env tag key with the Production tag value.

</td></tr><tr><td>

Example 3: one tag category, two values

</td><td>

Environment

</td><td>

Env

</td><td>

Staging,Production

</td><td>

Service Mapping creates two service candidates: One containing CIs that have the Production tag value; another containing CIs that have the Staging tag value.

</td></tr><tr><td>

Example 4: two tag categories, no values

</td><td>

EnvironmentApplication

</td><td>

EnvApp

</td><td>

Not defined

</td><td>

Service Mapping creates a service candidate for each combination of tag values for all defined tag keys.

</td></tr><tr><td>

Example 5: two tag categories, two values for each category

</td><td>

EnvironmentApplication

</td><td>

EnvApp

</td><td>

Production,Staging

 HR,Finance

</td><td>

Service Mapping creates four service candidates: production::hr, production::finance, staging::hr, staging::finance.

</td></tr></tbody>
</table>**Parent Topic:**[Service Mapping reference](service-mapping-reference.md)

