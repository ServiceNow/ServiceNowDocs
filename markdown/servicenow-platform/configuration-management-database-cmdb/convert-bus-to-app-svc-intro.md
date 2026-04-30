---
title: Convert business services to application services
description: Unify the way you manage services in the organization by converting manually created records in the Service \[cmdb\_ci\_service\] table into application services. Conversion lets you streamline the different types of services in your organization, leverage ITOM Visibility capabilities, and align with the Common Service Data Model \(CSDM\). The conversion is irreversible: You can't transform application services back into business services.Convert a subset of business services to application services, in bulk and automatically rather than one at a time. Individually select the business services for the conversion, and then convert them into application services.Manually convert a specific business service to an application service.
locale: en-US
release: xanadu
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 8
breadcrumb: [Application services, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Convert business services to application services

Unify the way you manage services in the organization by converting manually created records in the Service \[cmdb\_ci\_service\] table into application services. Conversion lets you streamline the different types of services in your organization, leverage ITOM Visibility capabilities, and align with the Common Service Data Model \(CSDM\). The conversion is irreversible: You can't transform application services back into business services.

Using application services has benefits such as:

-   Viewing service maps and change history of services.
-   Easily seeing the service context by providing a flat list of all CIs in the application service.
-   Monitoring service health. If Event Management is deployed, you can monitor service performance and identify health issues for application services.
-   In Change Management, the list of impacted services on a change request form is more accurate because the list includes only application services.
-   Applying Customer Service Management tools to open and manage cases at the service level.

Discovery doesn't run on converted application services, because converted services are manual. However, if after the conversion you add **Discoverable by Service Mapping** entry points to the application service, then Service Mapping starts discovering such this application service.

## Choosing between application services of the manually created and dynamic type

You can convert business services into application services of the manually created type or of the dynamic type. You can edit manually created application services by adding or removing CIs at any time. The system does not update manually created services automatically. If there are changes to CIs making up a manually created application service, the service does not automatically reflect it.

Dynamic services are updated automatically to reflect any change to CI relationships stored in the CMDB CI Relationship \[cmdb\_rel\_ci\] table. When you add a relationship to a CI that is contained in a dynamic service, then that service automatically updates to reflect the addition of the relationship and the associated new CI. In a similar manner, a dynamic service automatically updates upon the removal of a relationship and its associated CI from a CI within the service.

To learn more about different types of application services, see [application services](../../configuration-management/concept/application-services.md).

## Conversion process

During conversion, the following changes and processes occur:

-   The service record is moved from the Service \[cmdb\_ci\_service\] table into the Mapped Application Service \[cmdb\_ci\_service\_discovered\] table by changing the record class.
-   The service instance is set with all the original business service attributes such as name, owner, and operational status.
-   The system adds related items from the business service to the converted service instance, up to the specified level.
-   The system queries the CMDB for the latest CI changes.
-   Event Management, if activated, applies CI impact rules to CIs that are associated with alerts and that are part of the service instance. Event Management deploys CI impact rules for alert monitoring.
-   You can edit a converted application service of the manually created type by navigating to **CSDM** &gt; **Manage Technical Services** &gt; **Application Service**. Then select a converted application service. The service population method for a converted application service, is set to **Converted Business Service**. For more information about editing application services, see [Create an application service](../task/create-it-services.md).

    **Note:** You can't edit a dynamic application service by adding or removing CIs from it. The system automatically modifies an application service of the dynamic type when you modify relevant relationships for CIs that are part of that application service.


## Non-compliant CIs

A conversion might involve adding CIs of the following CI types, which cannot be added to an service instance:

-   NAT \[cmdb\_ci\_translation\_rule\]
-   Endpoint \[cmdb\_ci\_endpoint\]
-   Qualifier \[cmdb\_ci\_qualifier\]
-   Application cluster \[cmdb\_ci\_application\_cluster\]

If the original business service contains related items belonging to these CI types, then the system does not add such CIs or connections coming from them. There are system records in the Manual CI Exclusions/Inclusions \[svc\_manual\_ci\_exclusions\_inclusions\] table. See [Components installed with application services](../../configuration-management/reference/components-installed-app-services.md#manual-ci-inclusion-exclusion-list) for more information.

**Note:** The Manual CI Exclusions/Inclusions \[svc\_manual\_ci\_exclusions\_inclusions\] table doesn't include CIs added using traversal rules.

## Domain separation

In environments with domain separation, only CIs belonging to the same domain as the service instance are added to the service instance. If there is a domain hierarchy, CIs must belong to the same child domain as the service instance.

## Convert business services to application services in bulk

Convert a subset of business services to application services, in bulk and automatically rather than one at a time. Individually select the business services for the conversion, and then convert them into application services.

### Before you begin

Role required: app\_service\_admin, ecmdb\_admin, or itil\_admin

### About this task

Use bulk conversion to convert legacy business services to application services. For the bulk conversion, individually select the business services from the Services list view, typically up to 100 business services in a single conversion. You can create multiple bulk conversion records, each with a different set of business services. However, do not include a business service in more than one bulk conversion.

**Note:** You can't undo this conversion operation.

### Procedure

1.  Navigate to **All** &gt; **Configuration** &gt; **Services**.

2.  In the Services list view, select the services that you want to include in the conversion.

3.  In the Actions on selected rows drop down list, select **Bulk Convert Application Services**.

4.  Fill out the Bulk Convert Services form.

<table id="table_l3h_wwg_bjb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Pre-populated with "Application Service Conversion: &lt;time stamp&gt;".

</td></tr><tr><td>

Select configuration items

</td><td>

List of services included in the conversion.

 You can unlock the list and select services to remove from the list. Or, use the Select target record search box to search and add services to the list, by service names.

</td></tr><tr><td>

Levels

</td><td>

The number of levels of related CIs to include in the converted application service.

</td></tr><tr><td>

Update service when CMDB updates

</td><td>

Select this check box to convert the business service into an application service of the dynamic type.

</td></tr></tbody>
</table>5.  Select **Start Conversion**.


### What to do next

-   Check the status of a conversion: On the Bulk Convert Services form, scroll to the Bulk Convert Services Entries section to see the status \(such as Ready or Completed\) of a conversion.
-   Track the progress of a conversion as it runs: In the navigation filter, enter `cmdb_convert_bulk_services.list` and press the Enter key to see the list of conversions, and their progress.
-   \(Optional\) On a change request form, view affected dynamic services. For example, after you add an affected CI that is associated with a dynamic service:

    1.  Navigate to **Change** &gt; **Open**.
    2.  Select a new change request to add affected CIs to.
    3.  On the Change Request form, scroll to the Related Links section.
    4.  Click the **Affected CIs** tab and then click **Add** to add an affected CI to the change request.
    5.  Open the form context menu and select **Refresh Impacted Services**.
    6.  Click the **Impacted Services/CIs** tab to see any dynamic services that are associated with the affected CI and that are impacted by the change request.
    For more information about affected CIs on a change request, see [Associated CIs on a change request](https://www.servicenow.com/docs/access?context=c_AffectedCIsAndImpactedServices&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US).


## Convert an individual business service to an application service

Manually convert a specific business service to an application service.

### Before you begin

Review the original business service to evaluate it.

-   Make sure that all CIs and CI relations are relevant for the future application service. If necessary, change the CI relations in the CMDB.
-   Make sure that the original business service doesn't contain more than 5000 CI relations. Application services that contain more than 5000 CI relations cause mapping and monitoring performance issues.
-   Decide how many levels of CI relations you are going to use during conversion.

**Warning:** The conversion is irreversible: You can't transform application services back into business services.

Role required: app\_service\_admin

### Procedure

1.  Navigate to **All** &gt; **Configuration** &gt; **Business Services**.

2.  Select the business service that you want to convert to an service instance.

3.  Click **Convert to Application Service**.

    The Converting to Application Service dialog box opens.

4.  Select a number from the **Up to** list, as the number of levels of related CIs to include in the conversion.

    The maximum number of levels is eight.

5.  Select **Update service when CMDB updates** to convert the business service into an application service of the dynamic type.

6.  Click **OK**.


### Result

The system adds the CIs from the business service to the converted service instance.

### What to do next

Open the map for the newly converted service instance.

Make sure that the application services aren't too large:

-   Service Mapping doesn't offer to view CI list instead of a map for a service instance.
-   There is no discovery message indicating that the application service is too large: **The map does not display the entire service, because it is too large. The number of CI connections exceeded the allowed maximum.**

If the service is too large, perform the following actions:

-   Review the converted application service to identify CI relations irrelevant or redundant for this service. Remove such CI relations in the CMDB.
-   Decide how many levels of related CIs you must include into this application service. If necessary, [change the number of levels used in conversion](../task/update-services-from-cmdb.md) to reduce the service size.

**Related topics**  


[Application services](../../configuration-management/concept/application-services.md)

