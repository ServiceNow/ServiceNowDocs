---
title: Integrate third-party learning management systems with the Coaching with Learning application
description: Connect your ServiceNow instance with third-party learning sites to pull learning content into your repository.When you integrate Coaching with Learning with third-party learning management systems, the source record for Cornerstone OnDemand, Pluralsight, and Udemy applications are automatically created in the Enterprise Service Management Integrations Framework. These source records contain a predefined set of properties and integration services.
locale: en-US
release: australia
product: Workforce Optimization for Field Service
classification: workforce-optimization-for-field-service
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Set up coaching, Workforce Optimization, Set up workforce, Configure, Field Service Management]
---

# Integrate third-party learning management systems with the Coaching with Learning application

Connect your ServiceNow instance with third-party learning sites to pull learning content into your repository.

## Before you begin

**Important:** The Coaching with Learning application is available with the Workforce Optimization for Field Service \(sn\_fsm\_wfo\) from the ServiceNow Store. To enable this feature, see [Activate Workforce Optimization for Field Service](activate-wfo-fsm.md).

Role required: learning\_admin

## About this task

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
    5.  In the Integration Services related list, click **New**.
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

List of intermediate tables which store records from the third-party system.**Note:** This field is enabled only when Scheduled pull service is selected in the **Service type** field.

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

Application that contains the integration service record.

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

Option to indicate the type of service: Scheduled pull or Ondemand Push.

</td></tr><tr><td>

Retry policy

</td><td>

Configuration set to push a record if the previous push fails.**Note:** This field appears only when Ondemand Push service is selected in the **Service type** field.

</td></tr></tbody>
</table>    7.  Click **Submit**.
2.  Integrate your ServiceNow instance with your third-party learning source accounts.

<table id="choicetable_bzs_wvn_rpb"><thead><tr><th align="left" id="d98879e319">

To integrate with this third-party learning source

</th><th align="left" id="d98879e322">

Do this

</th></tr></thead><tbody><tr><td id="d98879e328">

**Pluralsight Skills account**

</td><td>

Use an API key to authenticate the ServiceNow requests. Follow the steps in [Set up the Pluralsight spoke](https://www.servicenow.com/docs/access?context=setup-pluralsight-spk&version=australia&pubname=australia-integrate-applications&ft:locale=en-US) to perform the integration.

</td></tr><tr><td id="d98879e341">

**Cornerstone application**

</td><td>

Register an OAuth application in Cornerstone and authenticate requests from ServiceNow. Follow the steps in [Set up the Cornerstone spoke](https://www.servicenow.com/docs/access?context=setup-cornerstone&version=australia&pubname=australia-integrate-applications&ft:locale=en-US) to perform the integration.

</td></tr><tr><td id="d98879e357">

**Udemy application**

</td><td>

**Note:** You must manually configure fields such as logos and course reassignments in the learning system configuration table.

</td></tr></tbody>
</table>    The records from the third-party content are pulled into your ServiceNow instance using and API call. To successfully run this API call, you must set certain properties:

    1.  In the application navigator, enter `sys_properties.list`.
    2.  For each of the following properties, set the value to **1638400**:
        -   com.glide.transform.json.max-partial-length
        -   com.snc.process\_flow.reporting.serialized.val\_size\_limit
    For more information on these system properties, see [Coaching With Learning System Properties](https://www.servicenow.com/docs/access?context=components-installed-configurable-wfo-cs&version=australia&pubname=australia-customer-service-management&ft:locale=en-US).

3.  Activate schedule flows to integrate third-party learning content.

    1.  Navigate to **Process Automation** &gt; **Flow Designer**
    2.  In the **Flows** section, select each of the following flows and click **Activate**:
        -   Trigger Cornerstone Learning Sync
        -   Trigger Pluralsight Learning Sync
        -   Trigger Udemy Learning Sync
    3.  Navigate to **Learning** &gt; **Administration** &gt; **Learning System Configuration**
    4.  Select each of the third-party learning sources and set the **Active** field to **true**.
    Schedule flows automatically run on a scheduled basis to synchronize third-party learning content into your ServiceNow instance.

    For more information, see [configure the third-party integration sources](https://www.servicenow.com/docs/access?context=integration-source-coaching-with-learning-coaching-wfo-cs&version=australia&pubname=australia-customer-service-management&ft:locale=en-US)

4.  After you configure the third-party integration sources, you can refresh the entire third-party content or synchronize new and updated services into your ServiceNow instance.

    -   To refresh the entire content, set the **full\_pull** property to true.

        **Note:** For best results, periodically refresh the entire content.

    -   To synchronize new and updated services, set the **full\_pull** property to false.
    1.  Open any integration source for which you want to pull content.
    2.  Click **Run Job**.
    The integration framework pulls the corresponding third-party learning courses into the Learning External Content \[sn\_lc\_external\_content\] table on your ServiceNow instance.

    When synchronizing new and updated services, the content is populated as described in the following table.

<table id="table_h4y_4lj_ppb"><thead><tr><th>

Third-party content

</th><th>

New and Updated Services Synchronized

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

[Add external courses to Coaching With Learning](https://www.servicenow.com/docs/access?context=coaching-configurable-wfo-cs&version=australia&pubname=australia-customer-service-management&section=integrate-external-courses-configurable-wfo-cs&ft:locale=en-US)

## External Content Integration Sources

When you integrate Coaching with Learning with third-party learning management systems, the source record for Cornerstone OnDemand, Pluralsight, and Udemy applications are automatically created in the Enterprise Service Management Integrations Framework. These source records contain a predefined set of properties and integration services.

<table id="table_tyz_xpj_1nb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the record in Enterprise Service Management Integrations Framework: Cornerstone.

</td></tr><tr><td>

Properties

</td><td>

Set of properties that are predefined for Cornerstone OnDemand application.-   **page\_size**: Number of records that are pulled through an API call from Cornerstone OnDemand application.
-   **full\_pull**: When set to True, all active users and learning courses from the Cornerstone OnDemand system are pulled into the ServiceNow instance.

When set to False, modified users, modified transcripts, and updated courses are pulled from the Cornerstone OnDemand system into the ServiceNow instance.

-   **url\_prefix**: Deep link prefix to pull learning objects from Cornerstone OnDemand system during run time.
-   **pull\_offset\_hours**: The time, in hours, calculated from the last successful run for the next synchronization to occur

For example, the last successful run was on 12/12/2021 at 17:00:00, **pull\_offset\_hours** is set to 5, and **full\_pull** is set to False. The next pull fetches all the records that have been modified from 12/12/2021 12:00:00 until current date and time.


</td></tr><tr><td>

Integration Services

</td><td>

Services interact with Cornerstone Ondemand application to pull or push learning courses.-   **Course assign service**: Assigns a course to an employee in the Cornerstone Ondemand application.
-   **Sync users**: Maps users in the Cornerstone OnDemand system to users in the ServiceNow system using email IDs.

**Note:** If you want to use user\_id or user\_name field for mapping users, override **getCornerstoneUser method** in the sn\_lc.UserMappingUtil script.

-   **Courses**: Pulls learning courses from Cornerstone OnDemand system into the ServiceNow instance.
-   **User activity**: Pulls details of user activity on learning courses from Cornerstone OnDemand system into the ServiceNow instance.

</td></tr></tbody>
</table><table id="table_fqb_b4y_mpb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the record in Enterprise Service Management Integrations Framework: Pluralsight.

</td></tr><tr><td>

Properties

</td><td>

Set of properties that are predefined for the Pluralsight system.-   **page\_size**: Number of records that are pulled through an API call from Pluralsight.
-   **full\_pull**: When set to True, all the learning courses are pulled from Pluralsight into the ServiceNow instance. When set to False, the updated learning course's progress is pulled from Pluralsight into the ServiceNow instance.
-   **pull\_offset\_hours**: Value that is considered for pulling modified records.

For example, the last successful run was on 12/12/2021 at 17:00:00, **pull\_offset\_hours** is set to 5, and **full\_pull** is set to False. The next pull fetches all the records that have been modified from 12/12/2021 12:00:00 until current date and time.


</td></tr><tr><td>

Integration Services

</td><td>

Integration services interact with Plural sight application to pull learning courses into ServiceNow.-   **Courses**: Pulls learning courses from Pluralsight into the ServiceNow instance.
-   **Course progress**: Pulls the progress of learning courses from Pluralsight into the ServiceNow.

</td></tr></tbody>
</table><table id="table_kwt_5py_mpb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the record in Enterprise Service Management Integrations Framework: Udemy

</td></tr><tr><td>

Properties

</td><td>

Set of properties that are predefined for the Udemy system.-   **page\_size**: Number of records that are pulled through an API call from Udemy into the ServiceNow instance.
-   **full\_pull**: When set to **True**, all the learning courses are pulled from Udemy into the ServiceNow instance. When set to False, updated learning courses and learning course progress are pulled from Udemy into the ServiceNow instance.
-   **pull\_offset\_hours**: Value that is considered for pulling modified records.

For example, the last successful run was on 12/12/2021 at 17:00:00, **pull\_offset\_hours** is set to 5, and **full\_pull** is set to False. The next pull fetches all the records that have been modified from 12/12/2021 12:00:00 until current date and time.


</td></tr><tr><td>

Integration Services

</td><td>

Integration services interact with Udemy application to pull learning courses into ServiceNow.-   Pull Courses: Pulls learning courses from Udemy into the ServiceNow instance.
-   Pull user activity: Pulls details of user activity on learning courses from Udemy into the ServiceNow instance.

</td></tr></tbody>
</table>