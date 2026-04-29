---
title: View CI attributes in an application service map in classic Service Mapping
description: An application service map displays attributes for each configuration item \(CI\) that is part of the application service, as well as for the application service itself. The attributes come from the CMDB.
locale: en-US
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Service instances \(Application services\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# View CI attributes in an application service map in classic Service Mapping

An application service map displays attributes for each configuration item \(CI\) that is part of the application service, as well as for the application service itself. The attributes come from the CMDB.

## Before you begin

Role required: service\_mapping\_admin or service\_mapping\_user

## About this task

You can view the following information for each CI:

-   **Name label**

    The CI name. This attribute is either preconfigured on the CI or configured during CI installation.

-   **Basic attributes**

    A summary of the most important CI attributes.

-   **Detailed attributes**

    A complete list of all attributes collected for the CI.


Each CI type \(CI class\) has different attributes. For example, the Linux Server type has different attributes than the SQL Instance type.

If Service Mapping is deployed, the way CIs appear on the map depends on the [view you select for the map](https://www.servicenow.com/docs/access?context=modify-map-view&version=australia&pubname=australia-it-operations-management&ft:locale=en-US). Attributes available for viewing also depend on the Service Mapping setup. For more information, see description of [components installed with Service Mapping](https://www.servicenow.com/docs/access?context=components-installed-with-service-mapping&version=australia&pubname=australia-it-operations-management&ft:locale=en-US).

## Procedure

1.  Open the service instance map.

    1.  Navigate to **All** &gt; **CSDM** &gt; **Manage Technology Management Services** &gt; **Service Instance**.

    2.  Select the needed service instance.

    3.  On the service instance page, select **View Map**.

2.  If needed, click **Edit** to ensure that the map is in Edit mode.

    If Service Mapping is deployed, then in Edit mode, the Discovery Messages section appears below the map.

3.  To see the full name of a CI whose name has been shortened on the map, point to the CI.

    A tooltip displays the full CI name.

4.  Click a CI to see its details in the **Properties** pane.

    The attributes of applications and the servers that host them appear separately.

    ![CI attributes displayed in the Properties pane](../image/AppServerProperties.gif)

5.  To view more detailed attributes for the CI, click **Detailed properties** at the bottom of the Properties pane.

6.  To view configuration files associated with a CI in environments where Service Mapping or Discovery are enabled and tracking changes to CI configuration files is enabled\):

    -   Review the list of files under **Tracked Files** in the **Properties** pane. Click the file name to open the actual file.
    -   Click the **Affected CIs** tab and view the list of configuration files. Click the file name to open the actual file.

