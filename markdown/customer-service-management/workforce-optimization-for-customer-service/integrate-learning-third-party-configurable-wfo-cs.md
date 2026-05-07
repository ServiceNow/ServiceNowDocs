---
title: Integrate Coaching with Learning with third-party learning management systems
description: Connect your ServiceNow instance with third-party learning sites to pull learning content into your repository.
locale: en-US
release: australia
product: Workforce Optimization for Customer Service
classification: workforce-optimization-for-customer-service
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Setting up Workforce Optimization Coaching, Configure, Workforce Optimization for Customer Service, Customer Service Management]
---

# Integrate Coaching with Learning with third-party learning management systems

Connect your ServiceNow instance with third-party learning sites to pull learning content into your repository.

## Before you begin

**Important:** This feature is available with the Workforce Optimization for CSM Configurable Workspace \(sn\_csm\_wfo\_workspa\) from the ServiceNow Store. To enable this feature, see [Activate Workforce Optimization for CS configurable workspace](request-configurable-wfo-cs.md).

Role required: learning\_admin

## About this task

**Applications to integrate third-party learning sites**

Activating the Coaching with Learning \(sn\_coach\_lrn\) plugin enables the following applications from the ServiceNow Store:

-   [Enterprise Service Management Integrations Framework](https://www.servicenow.com/docs/access?context=hr-integrations-framework&version=australia&pubname=australia-employee-service-management&ft:locale=en-US)
-   Cornerstone spoke
-   Pluralsight spoke
-   Udemy spoke

## Procedure

1.  Create the integration source for each of your third-party systems.

    **Note:** Cornerstone, Pluralsight, and Udemy integrations are available by default.

    1.  Navigate to **Integrations Framework** &gt; **Source**
    2.  Click **New**.
    3.  In the **Name** field, enter the name of the integration source, for example, Pluralsight.
    4.  Right-click the form header and click **Save**.
    5.  In the Integration Services related list that appears, click **New**.
    6.  On the form, fill in the fields:

<table id="table_kfz_z3j_ppb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the integration service, for example, Pluralsight.

</td></tr><tr><td>

Import set tables

</td><td>

List of intermediate tables which store records from the third-party system.**Note:** This field is enabled only when a Scheduled pull service is selected in the **Service type** field.

</td></tr><tr><td>

Flow

</td><td>

Flow that interacts with the third-party system to pull the required data.

</td></tr><tr><td>

Active

</td><td>

Option to indicate that the integration service is available for use.

</td></tr><tr><td>

Application

</td><td>

Application which includes the integration service record.

</td></tr><tr><td>

Source

</td><td>

Name of the third-party system with which you want to integrate your application.

</td></tr><tr><td>

Order

</td><td>

Order in which you want to run transformation scripts.

</td></tr><tr><td>

Service type

</td><td>

Option to indicate the type of service **Scheduled pull** or **Ondemand Push**.

</td></tr><tr><td>

Retry policy

</td><td>

Configuration set to push a record if the last push fails.**Note:** This field appears only when an Ondemand Push service is selected in the **Service type** field.

</td></tr></tbody>
</table>    7.  Click **Submit**.
2.  Integrate your ServiceNow instance with your third-party learning source accounts.

<table id="choicetable_bzs_wvn_rpb"><thead><tr><th align="left" id="d130939e302">

To integrate with this third-party learning source

</th><th align="left" id="d130939e305">

Do this

</th></tr></thead><tbody><tr><td id="d130939e311">

**Pluralsight Skills account**

</td><td>

Use an API key to authenticate the ServiceNow requests. Follow the steps in [Set up the Pluralsight spoke](https://www.servicenow.com/docs/access?context=setup-pluralsight-spk&version=australia&pubname=australia-integrate-applications&ft:locale=en-US) to perform the integration.

</td></tr><tr><td id="d130939e324">

**Cornerstone application**

</td><td>

Register an OAuth application in Cornerstone and authenticate requests from ServiceNow. Follow the steps in [Set up the Cornerstone spoke](https://www.servicenow.com/docs/access?context=setup-cornerstone&version=australia&pubname=australia-integrate-applications&ft:locale=en-US) to perform the integration.

</td></tr><tr><td id="d130939e337">

**Udemy application**

</td><td>

**Note:** You must manually configure fields such as logos and course reassignments in the learning system configuration table.

</td></tr></tbody>
</table>    The records from the third-party content are pulled into your ServiceNow instance using and API call. To successfully run this API call, you must do the following:

    1.  In the application navigator, enter `sys_properties.list`.
    2.  For each of the following properties, set the value to **1638400**:
        -   com.glide.transform.json.max-partial-length
        -   com.snc.process\_flow.reporting.serialized.val\_size\_limit
    For more information on these system properties, see [Coaching With Learning System Properties](../reference/components-installed-configurable-wfo-cs.md).

3.  Activate schedule flows to integrate third-party learning content.

    1.  Navigate to **Process Automation** &gt; **Flow Designer**
    2.  In the **Flows** section, select each of the following flows and click **Activate**:
        -   Trigger Cornerstone Learning Sync
        -   Trigger Pluralsight Learning Sync
        -   Trigger Udemy Learning Sync
    3.  Navigate to **Learning** &gt; **Administration** &gt; **Learning System Configuration**
    4.  Select each of the third-party learning sources and set the **Active** field to **true**.
    Schedule flows automatically run on a scheduled basis to synchronize third-party learning content into your ServiceNow instance.

4.  After [configuring the third-party integration sources](../reference/integration-source-coaching-with-learning-coaching-wfo-cs.md), you can refresh the entire third-party content or synchronize new and updated services into your ServiceNow instance.

    -   To refresh the entire content, set the **full\_pull** property to **true**.

        **Note:** We recommend that you periodically refresh the entire content.

    -   To synchronize new and updated services, set the **full\_pull** property to **false**.
    1.  Open any integration source for which you want to pull content.
    2.  Click **Run Job**.
    The integration framework pulls the corresponding third-party learning courses into the Learning External Content \[sn\_lc\_external\_content\] table on your ServiceNow instance.

    When synchronizing new and updated services, the content is populated as described in the table.

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


</td></tr><tr><td>

Pluralsight

</td><td>

-   Courses
-   Course progress such as percentage


</td></tr></tbody>
</table>
## What to do next

[Add external courses to Coaching With Learning](../concept/coaching-configurable-wfo-cs.md#)

-   **[External Content Integration Sources](../reference/integration-source-coaching-with-learning-coaching-wfo-cs.md)**  
When you integrate Coaching With Learning with third-party learning management systems, the source record for Cornerstone OnDemand, Pluralsight, and Udemy applications are automatically created in the Enterprise Service Management Integrations Framework. These source records contain a predefined set of properties and integration services.

**Parent Topic:**[Setting up Coaching in Workforce Optimization for Customer Service](../concept/setup-coaching-configurable-wfo-cs.md)

