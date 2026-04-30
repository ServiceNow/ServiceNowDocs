---
title: Service definition transfer from one instance to another
description: Save time and effort by exporting definitions of service instances from the source instance and importing these definitions into the target instance. You can use this method to copy definitions of service instances only of the discovered type.Create an import set containing definitions of services. You use this import set to import service definitions into another instance.Import definitions of application services from the source instance.
locale: en-US
release: yokohama
product: Service Mapping
classification: service-mapping
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 6
breadcrumb: [Application service completion, Application service mapping using classic Service Mapping, Using Service Mapping, Service Mapping, ITOM Visibility, IT Operations Management]
---

# Service definition transfer from one instance to another

Save time and effort by exporting definitions of service instances from the source instance and importing these definitions into the target instance. You can use this method to copy definitions of service instances only of the discovered type.

Typically, you maintain two ServiceNow instances in your organization: for production and for development. Perform the initial mapping of application services in your organization on the development instance, which you use for testing. The results of initial mapping often require some basic troubleshooting or fine-tuning. Once you finish mapping application services on your source instance, transfer service definitions into the target \(production\) instance.

Notice that you cannot export the actual application services, only service definitions. Mapping is a dynamic process, and the mapping result reflects the actual infrastructure and its configuration. Therefore, the services you exported from one instance and imported into another may look different.

By default, you export the following service definitions:

-   Service name
-   Traffic-based discovery usage
-   Entry point
-   Business criticality
-   Group to which the service belongs

    If this service group is part of a service group hierarchy, all parent service groups in this hierarchy are exported as well.

-   Comments

The system uses the Sys ID \[sys\_id\] attribute to identify services on the source and target instances and implements service definition import according to these rules:

-   If a service Sys ID does not exist on the target instance, the system creates a new service on the target instance.
-   If a service Sys ID and name already exist on the target instance, the system updates this service by overriding the existing service definitions with the imported definitions.
-   If a service Sys ID exists on the target instance, but is associated with a different service name, the system updates the service with this Sys ID. The system overrides service definitions, including the service name.
-   If the same name is used for different services on the source and target instances, the system does not import service definitions.
-   You cannot export manual services. Likewise, you cannot export manually added entry points. When importing definitions of a service containing manual entry points, the system does not make any changes to the entry points.

![Exporting service definitions.](../image/ExportService.png "Exporting service definitions flow")

When transferring service definitions between instances, imported service instances and service groups are assigned to the user's domain.

By default, the system assigns **Non-operational** status to application services whose definitions you imported.

A service definition transfer deploys the standard import set feature available on the ServiceNow AI Platform. When you export service definitions on the source instance, the system creates a JSON file containing exported data. When you copy service definitions into the target instance, you import the data from this JSON file, which becomes an import set.

**Parent Topic:**[Application service completion](advanced-business-service-definitions.md)

**Related topics**  


[Define criticality for application services](../task/define-criticality-for-business-services.md)

[Group application services](../task/organizing_services-into-groups.md)

[Control user access to application services](../task/control-user-access-to-business-services.md)

[Schedule a top-down discovery by Service Mapping](../task/t_CreateDiscoSchedForCITypes.md)

## Export service definitions

Create an import set containing definitions of services. You use this import set to import service definitions into another instance.

### Before you begin

-   Decide which service definitions you want to export.

    **Important:** You can use this method to copy definitions of application serviced of the discovered type only.

-   Verify that the source and the target instances are on the same ServiceNow release.
-   Open the source instance from which you want to copy service definitions.
-   If necessary, fine-tune the import set creation by modifying relevant properties under **Service Mapping** &gt; **Administration** &gt; **Properties**. For more information, see [Components installed with Service Mapping](../reference/components-installed-with-service-mapping.md).

Role required: service\_mapping\_admin

### Procedure

1.  If the instance uses domain separation and you have access to the global domain, select the domain to which the service instance belongs from the domain picker \(![Domain picker](../image/DomainPicker.png)\).

    The selected domain must be a domain without any child domains.

2.  Navigate to **Service Mapping** &gt; **Services** &gt; **Application Services**.

3.  Select the application services that you want to export.

4.  Click **Actions on selected rows** at the bottom of the page and select **Export Services**.

    The import set appears in the `Downloads` folder. The file name follows this convention: export\_service\_&lt;datetime&gt;.json.

5.  If necessary, copy the import set to a different location on the computer.


## Import service definitions from one instance to another

Import definitions of application services from the source instance.

### Before you begin

-   Verify that the source and the target instances are on the same ServiceNow release.
-   Open the target instance into which you want to import service definitions.

Role required: import\_admin

### Procedure

1.  If the instance uses domain separation and you have access to the global domain, select the domain to which the service instance belongs from the domain picker \(![Domain picker](../image/DomainPicker.png)\).

    The selected domain must be a domain without any child domains.

2.  Navigate to **Service Mapping** &gt; **Services** &gt; **Import Service Definitions**.

3.  In the Import Service Definitions window, click **Choose File**, navigate to the JSON file that contains service definitions, and click **OK**.

4.  Click **Show Preview** and check the definitions in the chosen JSON file.

5.  Click **Import**.

6.  Click **Yes** to confirm that you are ready to import service definitions.

    **Important:** During import, the system irreversibly overrides the current service definitions.

    The Progress window displays the success message.

    Service Mapping automatically starts the discovery of services containing imported entry points.

7.  Review imported or updated services after Service Mapping finishes the mapping process.

    If the transfer result is not as you expected, perform basic troubleshooting as described in the following table.


<table id="table_kjv_sdy_32b"><thead><tr><th>

Symptom

</th><th>

Cause

</th><th>

Solution

</th></tr></thead><tbody><tr><td>

Changes you have recently made to an service instance disappear.

</td><td>

Definitions of existing application services are always overridden during transfer.

</td><td>

1.  Make necessary changes to the definitions of this service instance again.
2.  Run the top-down discovery of this service instance by clicking **Run Discovery** in the service map.

</td></tr><tr><td>

An imported service group does not appear.

</td><td>

The import of an application service assigned to this group failed and the system did not create the group because it appears to be empty.

</td><td>

1.  Resolve the issue that prevented the system from importing the service instance belonging to this group.
2.  Import the import set again.
3.  Check that the service group appears.

</td></tr><tr><td>

An imported service group appears to have wrong application services assigned to it.

</td><td>

This is a different service group with the same name, not the service group you imported. The system failed to import the service group, because the source instance already has a service group with the same name or with the same name and Sys ID.

</td><td>

1.  Check the import log.
2.  If an error states that a record creation failed while running the Check Name Uniqueness business rule, perform the following steps:
    1.  Rename the service group on the source instance.
    2.  Re-export the application services assigned to this group.
    3.  Import the latest import set on the target instance.
3.  If an error states that a record creation failed because the Sys ID already exists, perform the following steps:
    1.  Recreate the service group on the source instance, ensuring you provide a different group name and Sys ID to it.
    2.  Re-export the application services assigned to this group.
    3.  Import the latest import set on the target instance.
4.  Verify that the service group appears correctly on the source instance.

</td></tr></tbody>
</table>