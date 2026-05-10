---
title: Create a Service instance \(application service\)
description: Create an application service to adhere to Common Service Data Model standards and to standardize the organization, maintenance, and monitoring of services in your organization.
locale: en-US
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 8
breadcrumb: [Service instances \(Application services\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Create a Service instance \(application service\)

Create an application service to adhere to Common Service Data Model standards and to standardize the organization, maintenance, and monitoring of services in your organization.

## Before you begin

Role required: Depending on the population method used:

-   Dynamic CI Group: app\_service\_admin
-   Manual: app\_service\_admin
-   Dynamic Service: app\_service\_admin
-   Top-Down Discovery: sm\_admin
-   Tags: sm\_admin

## About this task

An application service is a set of interconnected applications and hosts, which are configured to offer a service for the organization. Application services can be internal, like an organization's email system, or customer-facing, like an organization's website.

An application service has an entry point, which lets users access the application service. If you are at the planning stage and don’t know what the entry points are for an application service, you can create the application service without entry points. Such an application service is referred to as an empty application service, to which you can add entry points at any later time.

All application services created in the Application Service wizard, are set with the **application service** classification.

Service Mapping, if activated, can automatically discover and map application services as described in [Application service mapping](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-mapping/c_DefineMapBusinessServices.md). A discovered application service contains the CIs and the connections between them that Service Mapping discovered and mapped.

You can also create an application service by using the [createOrUpdateService - POST](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/rest-apis/application-service-api.md) REST API.

## Procedure

1.  Navigate to **All** &gt; **CSDM** &gt; **Manage Technology Management Services** &gt; **Service Instance**.

2.  In the Service Instances list view, select **New** to open the Application Service wizard.

3.  In the **Provide Basic Details** tab:

    1.  Fill out the fields for Basic Details.

<table id="table_gtd_cxq_zkb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Pre-populated unique ID for the application service.

</td></tr><tr><td>

Name

</td><td>

Unique application service name, which isn’t in use by any other type of application service. Use self-explanatory names such as `mailing service` or `printing service`.

</td></tr><tr><td>

Environment

</td><td>

The environment of the offering such as production, development, or test, as identified by some service offerings.

 Used by Incident Management and Change Management.

</td></tr><tr><td>

Version

</td><td>

The application service configuration version.

</td></tr><tr><td>

Model ID

</td><td>

A product model such as a software model where end of life data is stored.

</td></tr><tr><td>

Operational Status

</td><td>

Operational status of the application service, such as **Ready** or **Retired**.

</td></tr><tr><td>

Support Group

</td><td>

Used by Incident Management as the group managing the contract covering the asset.

</td></tr><tr><td>

Change Group

</td><td>

Used by ITSM for routing of change and change-related tasks.

</td></tr><tr><td>

Managed By Group

</td><td>

Group responsible for managing the data.

</td></tr><tr><td>

Owned By

</td><td>

User who is familiar with the infrastructure and applications making up the service. This user is the application service Subject Matter Expert \(SME\) who provides information necessary for a successful creation of an application service.

 If the owner name is not listed, create a user with the sm\_app\_owner role, as the owner. Alternatively, you can choose a user with the sm\_admin role.

</td></tr></tbody>
</table>        **Note:** See [Teams related list](../../configuration-management/reference/r_RelatedListsOfCIComponents.md) for details about the automatic synchronization between the assignment group fields and the **Teams** related list.

    2.  In the Set Relationships section, add relationships between the application service and other components in the CSDM domain.

    3.  Select the **Business Application**, **Technical Service Offering**, **Business Service Offering**, or the **Parent Application Service** tab, and add items to the respective **Selected** list.

        -   The technical service offering list includes records in the Service Offering \[service\_offering\] table, in which the **Service classification** attribute is **Technical Service**.
        -   The business service offering list includes records in the Service Offering \[service\_offering\] table, in which the **Service classification** attribute is **Business Service**.
        -   The parent application service list includes application service records from the Service Instance \[cmdb\_ci\_service\_auto\] table. Adding a parent application service relationship creates hierarchies and dependencies of application services in deployments such as:
            -   Platform host and platform application deployments
            -   Micro service deployments in which one or more micro services identified as an application service, is part of a larger application service deployment
            -   Shared technical service dependencies
    4.  Select **Next**.

    For information about CSDM relationships, see [CI relationships in the CSDM](../../csdm-implementation/concept/ci-relationships.md).

    Also, some fields and relationships are noted as required on the page. To change which fields and which relationships are required, see [Modify the attributes and relationships required for application services](../../configuration-management/task/modify-req-fields-appservice.md).

4.  On the **Populate the Application Service** tab:

    ![Populate the application service tab for a new application service](../image/app-services-tab2.png)

    1.  Click **Choose a Method** or select **Next** to skip selecting a service population method.

    2.  On the Choose a Method page, select a **Service Population Method**, and then follow the respective link to complete the specific population method:

        -   **Top Down Discovery**: [Use top-down discovery to populate application services](../../configuration-management/task/populate-app-service-top-down.md)
        -   **Dynamic CI Group**: [Populate an application service using the Dynamic CI Group method](../../configuration-management/task/populate-app-service-dynamic-group.md).
        -   **Tags**: [Use tags to populate application services](../../configuration-management/task/populate-app-service-tags.md)
        -   **Manual**: [Use the Manual method to populate application services](../../configuration-management/task/populate-app-service-manual.md)
        -   **Dynamic Service**: [Populate an application service using the Dynamic Service method](../../configuration-management/task/populate-app-service-dynamic-service.md)
        **Note:** The **Top Down Discovery** and the **Tags** options are available only if Service Mapping is installed.

    3.  To add another method to populate the application service, click **Add Method** on the Service Population Methods page.

        Or, select **Next**.

        -   You can add any combination of the **Top Down Discovery** and the **Manual** methods. However, if you select the **Dynamic CI Group**, **Tags**, or the **Dynamic Service** method, the **Add Method** button is grayed out and you can’t add additional methods.
        -   You can select a card for a Converted Business Service method to see details about the service conversion, such as the conversion type. For more information, see [Convert business services to application services](../concept/convert-bus-to-app-svc-intro.md#).
5.  On the **Preview the Service** tab, review and verify the summaries for creating and populating the application service.

    ![Preview service tab](../image/app-services-tab3.png)

    1.  Review **Relationships**.

    2.  You can select **Edit Relationships** to modify the relationships to other CSDM objects.

    3.  Review **Population Methods Summary**.

    4.  You can select **Edit Methods** to modify the selection methods.

    5.  Select **Done**.


## Result

The application service is created, and you can access the new application service by navigating to application services list views:

-   **CSDM** &gt; **Manage Technology Management Services** &gt; **Application Service**: Contains application service CIs from any class extending the Service Instance \[cmdb\_ci\_service\_auto\] class, except alert groups. The list view includes the tag-based, discovered, manual, dynamic CI groups, converted, dynamic, and empty application service types.
-   **Configuration** &gt; **Application Services** &gt; **Application Services**: Contains application service CIs from any class extending the Service Instance \[cmdb\_ci\_service\_auto\] class, except alert groups. The list view includes the tag-based, discovered, manual, dynamic CI groups, converted, dynamic, and empty application service types.
-   **Service Mapping** &gt; **Services** &gt; **Service Instances**: Contains application service CIs from the Mapped Application Service \[cmdb\_ci\_service\_discovered\] class. The list view includes the top-down \(discovered\) and empty application service types.

## What to do next

-   If the service population method is **Dynamic CI Group**:

    -   Select **View CMDB Group CI's** to list all the CIs in the CMDB group that is associated with the application service.
    -   Select **View Service CI's** to list all the CIs in the application service.
    Both lists of CIs are identical, unless the CMDB group contains more than 10,000 CIs. In this case, **View CMDB Group CI's** shows all the CIs in the CMDB group, and **View Service CI's** shows only the 10,000 CIs that are members of the application service.

-   If the service population method is **Tags**, **Top Down Discovery**, or **Manual**, and select **View Map** to [view the application service map](../../configuration-management/task/app-service-map-base-system.md) where you can:
    -   [Link application services](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-mapping/link-services-to-services.md)
    -   [View CI attributes in an application service map](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-mapping/t_ViewCIDetails.md)
    -   [View the change history of application services](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-mapping/t_ViewCIChanges.md)
    -   [Compare two versions of an application service](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-mapping/t_CompareBS.md)
-   Select **Advanced**, and then on the Advanced Details page, select **Additional Info**, **Questionnaire**, **Reject Messages**, or **Worknotes**, to add details.

