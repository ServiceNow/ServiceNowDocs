---
title: Microsoft Azure resource inventory discovery
description: The ServiceNow Discovery application uses the Azure Resource Inventory \(LP\) pattern to find resources available through Azure that don’t have a dedicated pattern. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
release: xanadu
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Available discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Microsoft Azure resource inventory discovery

The ServiceNow Discovery application uses the Azure Resource Inventory \(LP\) pattern to find resources available through Azure that don’t have a dedicated pattern. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

You can discover up to 10 thousand resources using the Azure Resource Inventory \(LP\) pattern.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Prerequisites

-   **Azure service principal**

    Verify the Azure service principal is configured. For more information, see [Azure Cloud Discovery](../../discovery/concept/azure-cloud-discovery.md)

-   **Privileges**

    For versions 1.3.0 and later:

    On the Microsoft Azure Console, provide a user with the API Management Service Reader role with permissions to run the following REST POST request:

    `"https://management.<resource url>/providers/microsoft.resourcegraph/resources?api-version=2022-10-01"`

    &lt;resource url&gt; – The URL varies based on the Azure account type, like "azure.com" or government site address.

    For versions 1.0.99 and earlier:

    On the Microsoft Azure Console, provide a user with the API Management Service Reader role with permissions to run the following REST GET request:

    `"https://management.azure.com/subscriptions/<subscription id>/resources"`

-   **Create a Cloud Discovery schedule**

    Create a schedule for the relevant Azure service account as described in [Create discovery schedules for cloud resources](../../discovery/concept/discovery-manager.md#)

-   **Fine-tune Azure inventory discovery using the Resource Inclusion List**

    If your deployment has custom patterns for Azure discovery, ensure that you don’t discover Azure resources twice.

    **Note:** Leaving the \[pre\_resource\_whitelist\] table empty causes the Pattern to populate all resources and it might cause performance issues.

    1.  Ensure that the application scope is Discovery and Service Mapping Patterns:
        1.  Navigate to **Settings** &gt; **Developer**.
        2.  Select `Discovery and Service Mapping Patterns` from the **Application** list.
    2.  Navigate to **System Definitions** &gt; **Tables**.
    3.  Open the Cloud Inventory Resource Inclusion List \[sa\_cloud\_inventory\_resource\_whitelist\] table.
    4.  Under **Related Links**, click **Show List**.
    5.  Select resource types for which you have custom patterns, and select `Delete` from the **Actions on selected rows** list.
    The Cloud Inventory Resource Inclusion List is predefined with common services. You can expand the inclusion list with additional resource types that you want the pattern to discover. The names of these resource types must conform to the appropriate vendor naming conventions.

    **Note:** When you modify the out-of-the-box inclusion list, it is no longer updated automatically in application updates. You must maintain the customized list on your own.

    1.  Open the Cloud Inventory Resource Inclusion List \[sa\_cloud\_inventory\_resource\_whitelist\] table.
    2.  Click **New**.
    3.  Fill in the form, and then click **Submit**.

        |Field|Description|
        |-----|-----------|
        |Cloud Vendor|The vendor of the resource type: Azure.|
        |Resource Type|The Azure resource type value.|
        |Application|The application scope: Discovery and Service Mapping Patterns.|

    The changes are applied the next time you run the pattern.

-   **Modify the ServiceNow related entries**

    1.  Navigate to **Related Entries**.
    2.  Click **New**.
    3.  For the identifier, enter **cmdb\_ci\_cmp\_resource**.
    4.  For the related table, select **Key Value \[cmdb\_key\_value\]**.
    5.  For the referenced field, select **Configuration Item**.
    6.  For the criterion attributes, add **Key** and **Value**.

        You may need to click the lock icon ![Lock icon](../../event-management/image/lock-icon.png) to view and change the criterion attributes.

    ![Related entry form](../image/related-entry.png)


## Data collected by Discovery during horizontal discovery

|Table and field|Additional information|
|---------------|----------------------|
|Cloud Resource \[cmdb\_ci\_cmp\_resource\]|
|Name|A descriptive name used to identify the Azure resource.|
|Resource type|The type of the resource, for example network, load balancer.|
|Object ID|The ID of the Azure resource.|
|Description|The text populated during discovery that specifies that this resource is available from Azure.|
|Key Value \[cmdb\_key\_value\]|
|Key|The Azure tag key name.|
|Value|The Azure tag value name.|

## CI relationships

These relationships are created to support Azure resource inventory discovery:

<table id="table_ysf_fpq_f987b"><thead><tr><th>

CI

</th><th>

Relationship

</th><th>

CI

</th></tr></thead><tbody><tr><td>

Cloud Resource \[cmdb\_ci\_cmp\_resource\]

</td><td>

Hosted on:Hosts

</td><td>

Azure datacenter \[cmdb\_ci\_azure\_datacenter\]

</td></tr></tbody>
</table>**Parent Topic:**[Available discovery patterns](../concept/available-patterns.md)

**Related topics**  


[https://learn.microsoft.com/en-us/azure/governance/resource-graph/reference/supported-tables-resources](https://learn.microsoft.com/en-us/azure/governance/resource-graph/reference/supported-tables-resources)

