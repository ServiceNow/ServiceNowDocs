---
title: Integrating Learning Core with third-party learning management systems
description: Connect your ServiceNow instance with third-party learning systems to pull learning content into a single repository.
locale: en-US
release: yokohama
product: Learning Core
classification: learning-core
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Configuring Learning Core, Learning Core, HR Service Delivery, Employee Service Management]
---

# Integrating Learning Core with third-party learning management systems

Connect your ServiceNow instance with third-party learning systems to pull learning content into a single repository.

## Before you begin

Role required: learning\_admin

Activating the Learning Core \(sn\_lc\) plugin automatically enables the following plugins:

-   [Enterprise Service Management Integrations Framework](../concept/hr-integrations-framework.md)

The following plugins are not active by default, and you must install them to use them with Learning Core.

## Procedure

1.  Integrate your ServiceNow instance with the third-party learning source account that you plan to use.

<table id="id_znb_bqn_vfc"><thead><tr><th>

Third-party content

</th><th>

New and Updated Services synchronized

</th></tr></thead><tbody><tr><td>

Udemy

</td><td>

-   Courses
-   User activity


</td></tr><tr><td>

Cornerstone

</td><td>

-   Users
-   Courses
-   User activity
-   Course assign service


</td></tr><tr><td>

Pluralsight

</td><td>

-   Courses
-   Course progress such as percentage


</td></tr><tr><td>

Sumtotal

</td><td>

-   Users
-   Courses
-   User activity
-   Assign course in Sumtotal


</td></tr><tr><td>

Saba

</td><td>

-   Course assign service
-   Pull Courses from Saba
-   Sync Saba Users
-   Pull Saba User Course Activity


</td></tr><tr><td>

Workday Learning

</td><td>

-   Users
-   Courses
-   User activity
-   Assign course in Workday Learning


</td></tr></tbody>
</table>2.  Activate the required schedule flow to synchronize third-party learning content into your ServiceNow instance.

    For more information, see [Activate Learning Core flows](flows-lp.md).

3.  Configure the learning system with which you want to integrate your ServiceNow instance.

    For more information, see [Configure a learning system](create-source-ln.md).

    **Note:** Once you set up the Learning Core application, the source record for Cornerstone OnDemand, Pluralsight, and Udemy applications are automatically created in the Source module in Enterprise Service Management Integrations Framework. These source records contain a predefined set of properties and integration services. For more information, see [Sources for Learning Core](../reference/source-lnpst.md).

4.  Refresh the entire third-party content or synchronize new and updated service content into your ServiceNow instance.

    -   To refresh the entire content, set the **full\_pull** property to **true**.

        **Note:** When the schedule flow is run for the first time, it always is a full pull irrespective of the value set in the property.

    -   To synchronize new and updated service content, set the **full\_pull** property to **false**.
    1.  Open any integration source for which you want to pull content.
    2.  Click **Run Job** to manually synchronize data.
    The integration framework pulls the corresponding third-party learning courses into the Learning External Content \[sn\_lc\_external\_content\] table on your ServiceNow instance.

    When synchronizing new and updated services, the content is populated as described in the table below.

<table id="table_h4y_4lj_ppb"><thead><tr><th>

Third-party content

</th><th>

New and Updated Services synchronized

</th></tr></thead><tbody><tr><td>

Udemy

</td><td>

-   Courses
-   User activity


</td></tr><tr><td>

Cornerstone

</td><td>

-   Users
-   Courses
-   User activity
-   Course assign service


</td></tr><tr><td>

Pluralsight

</td><td>

-   Courses
-   Course progress such as percentage


</td></tr><tr><td>

Sumtotal

</td><td>

-   Users
-   Courses
-   User activity
-   Assign course in Sumtotal


</td></tr><tr><td>

Saba

</td><td>

-   Course assign service
-   Pull Courses from Saba
-   Sync Saba Users
-   Pull Saba User Course Activity


</td></tr><tr><td>

Workday Learning

</td><td>

-   Users
-   Courses
-   User activity
-   Assign course in Workday Learning


</td></tr><tr><td>

SuccessFactors Learning spoke

</td><td>

-   Retrieve learning information
-   User data
-   Course data
-   Sync user activity


</td></tr></tbody>
</table>
## What to do next

To integrate Learning Core with a new third-party learning system, follow the instructions in [Create a source for a learning system](set-up-int-lc.md).

-   **[Sources for Learning Core](../reference/source-lnpst.md)**  
Once you set up the Learning Core application, the source record for Cornerstone On Demand, Pluralsight, Udemy, Sumtotal, and Saba applications are automatically created in the Source module in Enterprise Service Management Integrations Framework. The source records in the Enterprise Service Management Integrations Framework application contain a predefined set of properties and integration services.
-   **[Activate Learning Core flows](flows-lp.md)**  
Activate the flows that run on a schedule basis to pull learning course items from the Cornerstone OnDemand, Udemy, Pluralsight, Sumtotal, and Saba applications into the ServiceNow application.

**Parent Topic:**[Configuring Learning Core](../concept/configuring-learning-core.md)

**Related topics**  


[Administration tasks in Learning Core](ln-administration.md)

