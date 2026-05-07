---
title: Map application services based on Automated Service Suggestions
description: Map a new application service based on automatically generated suggestions. Use the Automated Service Suggestions or Service Fingerprints features to create a new application service or add to an existing service in a few clicks.
locale: en-US
release: australia
product: Service Mapping
classification: service-mapping
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Using Service Mapping, Service Mapping, ITOM Visibility, IT Operations Management]
---

# Map application services based on Automated Service Suggestions

Map a new application service based on automatically generated suggestions. Use the Automated Service Suggestions or Service Fingerprints features to create a new application service or add to an existing service in a few clicks.

## Before you begin

-   Service Mapping Plus must be installed. For more information, see [Install Service Mapping Plus](install-service-mapping-plus.md).
-   Confirm that the application is ready to discover and map application services. See [Application service readiness dashboard in configurable workspace](../reference/readiness-dashboard-ml.md).

Role required: service\_mapping\_admin

## About this task

In addition to being provided with automatically generated suggestions, you can also identify and choose an application service by using Service Fingerprints suggestions that include information about the components in the application service candidates. For more information, see [Automated Service Suggestions](../concept/auto-serv-suggest.md).

## Procedure

1.  Navigate to **Workspaces** &gt; **Service Mapping**

2.  Select **ML powered candidates**.

    **Note:** Starting with Service Mapping Plus version 1.16.3, the filtering process has been updated to include only the most relevant candidates, excluding any ignored or irrelevant ones. This enhancement requires the installation of ITOM Content Service.

3.  Select an application service either based on candidate suggestions or identify services with desired component.

<table id="sm-auto-sug"><thead><tr><th align="left" id="d447585e160">

Search method

</th><th align="left" id="d447585e163">

Actions

</th></tr></thead><tbody><tr><td id="d447585e169">

**Select from candidates based on a desired component**

</td><td>

1.  Select the Service Fingerprints tab.
2.  Review the list of Service Fingerprints suggestions that include components.
3.  Select your preferred application service candidate.


</td></tr><tr><td id="d447585e196">

**Select the candidate using basic details**

</td><td>

1.  Select the Application Service Suggestions tab.
2.  Review the list of suggested application services.
3.  Select your preferred candidate.


</td></tr></tbody>
</table>4.  Preview the map.

    1.  Select **Preview map**.

    2.  Review the components of the proposed application service map.

        **Note:** This preview map might appear different from the candidate because it doesn’t show absent connections. For more information, see the [Automated Service Suggestions Troubleshooting \[KB1205971\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1205971) article in the ServiceNow Support Knowledge Base.

    3.  Select **List navigation** to return to the candidate list.

5.  Select **Map application service**.

6.  Either create a new application service with the suggested candidate or add the suggested candidate to an existing application service.

<table id="choicetable_mwr_xjr_ycc"><thead><tr><th align="left" id="d447585e285">

Action

</th><th align="left" id="d447585e288">

Steps

</th></tr></thead><tbody><tr><td id="d447585e294">

**Create a new application service**

</td><td>

1.  Select **Create new service**.
2.  On the form, fill in the fields.

<table id="table_iyx_5kr_ycc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Pre-populated, unique name suggested for the new application service.

 Use this name. enter a unique name, or select **Other name suggestions** for additional options. For more information, see [Name suggestions for application service candidates](../reference/app-services-name-suggestions.md).

</td></tr><tr><td>

Number

</td><td>

Pre-populated unique ID for the application service.

</td></tr><tr><td>

Description

</td><td>

Description of the new application service.

</td></tr><tr><td>

Service owner

</td><td>

The user who approves of or rejects any change to the mapped application service.

</td></tr><tr><td>

Service group

</td><td>

A specific application services group to which you want to add this service. The default All setting means the application service is available to all groups.

</td></tr></tbody>
</table>

</td></tr><tr><td id="d447585e411">

**Add a candidate to an existing service**

</td><td>

1.  Select **Add to existing service**.
2.  Begin entering the name of the existing service and select the desired service from the list.


</td></tr></tbody>
</table>7.  Select **Map service**.

8.  Select **View map** to view the new or modified application service.


**Parent Topic:**[Using Service Mapping](../concept/using-service-mapping.md)

**Related topics**  


[Automated Service Suggestions](../concept/auto-serv-suggest.md)

