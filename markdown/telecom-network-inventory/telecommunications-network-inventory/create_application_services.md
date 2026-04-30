---
title: Create or add an xNF instance
description: Create or add an existing xNF \(different types of network functions\) instance by using the Telecommunications Network Inventory application. You can create xNF instances to model your 5G network.Created topics for STRY55389656 - DOC1072742
locale: en-US
release: xanadu
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Create xNF and xNF instances, Reviewing and updating your network inventory with the Network Inventory Workspace, Using Telecommunications Network Inventory, Telecommunications Network Inventory]
---

# Create or add an xNF instance

Create or add an existing xNF \(different types of network functions\) instance by using the Telecommunications Network Inventory application. You can create xNF instances to model your 5G network.

## Before you begin

-   Table name: \[cmdb\_ci\_service\_auto\].
-   Role required: sn\_ni\_core.inventory\_admin, sn\_ni\_core.inventory\_agent, sn\_ni\_core.telco\_inventory\_catalog\_manager.

## About this task

Application services support a business or technical service and are mapped to the CMDB Application Service table \[cmdb\_ci\_service\_auto\] for common reporting. This task enables you to create, review, update, and delete multiple instances.

## Procedure

1.  Navigate to **All** &gt; **CSDM** &gt; **Manage Technical Services** &gt; **Application Service**.

2.  Select **New**.

3.  On the Create an Application Service form, in the Basic Details section, fill in the fields.

    To get a description of the field values, see [Create an application service](https://www.servicenow.com/docs/access?context=create-it-services&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).

4.  In the set relationships section, select the **Business application** tab.

5.  Search and select a business application under the available box.

6.  Move the selected business application to the selected box.

    The selected business application is assigned to this application service.

7.  Select the **Parent Application Service** tab and assign the parent application service to this application service, if applicable.

8.  Select **Next**.

9.  Select **Choose a method**.

10. On the Choose a Method form, fill in the fields.

<table id="table_zpy_2nv_yxb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Service Population Method

</td><td>

Method to populate the application service with configuration items \(CIs\).

</td></tr><tr><td>

CMDB Table

</td><td>

CMDB Table. Based on the selected method, this field is automatically filled in.

</td></tr><tr><td>

Group name

</td><td>

Group name.**Note:** This field is applicable only for dynamic CI groups.

</td></tr><tr><td>

Class

</td><td>

Class that you can select the CI to add to this application service.**Note:** This field applies only for the manual method.

</td></tr><tr><td>

CI

</td><td>

CI that you can add to this application service.**Note:** This field is application only for the manual method.

</td></tr><tr><td>

Level

</td><td>

Number of interconnected CI levels to apply to this application service.**Note:** This field is applicable only for the dynamic service method.

</td></tr></tbody>
</table>11. Select **Save**.

12. Add another method by selecting **Add method**.

13. Select **Next**.

14. On the following tabs, select **Edit relationships**:

    -   **Relationships**: Updates your relationship with the business application and parent application service.
    -   **Population methods summary**: Updates an existing method or adds another method.
15. Select **Done**.

16. In the network inventory workspace, view the visual representation of the selected record by selecting the **Open Map** button.

    **Note:** Install CMDB Workspace 3.5.0 or a later version to enable this button in your network inventory workspace. To learn more, see [CMDB Workspace](https://store.servicenow.com/sn_appstore_store.do#!/store/application/c8ab76825371201032b7ddeeff7b1280/3.5.0).


## What to do next

You can review, update the fields, create a related tab record, or delete a record. To learn more, see [Update or delete a service record](../concept/update_or_delete_a_service_record.md).

**Parent Topic:**[Create xNF and xNF instances](../concept/services.md)

