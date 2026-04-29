---
title: Sources for Learning Core
description: Once you set up the Learning Core application, the source record for Cornerstone On Demand, Pluralsight, Udemy, Sumtotal, and Saba applications are automatically created in the Source module in Enterprise Service Management Integrations Framework. The source records in the Enterprise Service Management Integrations Framework application contain a predefined set of properties and integration services.
locale: en-US
release: australia
product: Learning Core
classification: learning-core
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Integrating Learning Core with third-party learning management systems, Configuring Learning Core, Learning Core, HR Service Delivery, Employee Service Management]
---

# Sources for Learning Core

Once you set up the Learning Core application, the source record for Cornerstone On Demand, Pluralsight, Udemy, Sumtotal, and Saba applications are automatically created in the Source module in Enterprise Service Management Integrations Framework. The source records in the Enterprise Service Management Integrations Framework application contain a predefined set of properties and integration services.

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

Set of properties that are predefined for the Cornerstone OnDemand application.-   **page\_size**: Number of records that are pulled through an API call from the Cornerstone OnDemand application.
-   **full\_pull**: When set to **True**, all the active users and learning courses from the Cornerstone OnDemand system are pulled into the ServiceNow application.

When set to **False**, modified users, modified transcripts, and updated courses are pulled from the Cornerstone OnDemand system into the ServiceNow instance.

-   **url\_prefix**: Deep link prefix to pull learning objects from Cornerstone OnDemand system during run time.
-   **pull\_offset\_hours**: Value that is considered for pulling modified records.

For example, the last successful run was on 12/12/2021 at 17:00:00, pull\_offset\_hours is set to 5, and full\_pull is set to False. The next pull fetches all the records that have been modified from 12/12/2021 12:00:00 until current date and time.


</td></tr><tr><td>

Integration Services

</td><td>

Services that interact with the Cornerstone OnDemand application to pull or push learning courses.-   **Course assign service**: Assigns a course to an employee in the Cornerstone Ondemand application.
-   **Sync users**: Maps users in the Cornerstone OnDemand system to users in the ServiceNow system using email Ids.

**Note:** If you want to use user\_id or user\_name field for mapping users, then override**getCornerstoneUser method** in the sn\_lc.UserMappingUtil script.

-   **Courses**: Pulls learning courses from the Cornerstone OnDemand application into the ServiceNow application.
-   **User activity**: Pulls details of user activity on learning courses from the Cornerstone OnDemand application into the ServiceNow application.

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
-   **full\_pull**: When set to **True**, all the learning courses are pulled from Pluralsight into the ServiceNow instance. When set to **False**, updated learning courses progress is pulled from Pluralsight into the ServiceNow instance.
-   **pull\_offset\_hours**: Value that is considered for pulling modified records.

For example, the last successful run was on 12/12/2021 at 17:00:00, pull\_offset\_hours is set to 5, and full\_pull is set to False. The next pull fetches all the records that have been modified from 12/12/2021 12:00:00 until current date and time.


</td></tr><tr><td>

Integration Services

</td><td>

Services that interact with the Plural sight application to pull learning courses into the ServiceNow application.

 -   **Courses**: Pulls learning courses from the Pluralsight application into the ServiceNow application.
-   **Course progress**: Pulls the progress of learning courses from the Pluralsight application into the ServiceNow application.

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

Set of properties that are predefined for the Udemy application.-   **page\_size**: Number of records that are pulled through an API call from Udemy into the ServiceNow application.
-   **full\_pull**: When set to **True**, all the learning courses are pulled from Udemy into the ServiceNow application. When set to **False**, updated learning courses and learning courses progress are pulled from Udemy into the ServiceNow application.
-   **pull\_offset\_hours**: Value that is considered for pulling modified records.

For example, the last successful run was on 12/12/2021 at 17:00:00, pull\_offset\_hours is set to 5, and full\_pull is set to False. The next pull fetches all the records that have been modified from 12/12/2021 12:00:00 until current date and time.


</td></tr><tr><td>

Integration Services

</td><td>

Services that interact with the Udemy application to pull learning courses into the ServiceNow application.

 -   Pull Courses: Pulls learning courses from the Udemy application into the ServiceNow application.
-   Pull user activity: Pulls details of user activity on learning courses from the Udemy application into the ServiceNow application.

</td></tr></tbody>
</table><table id="table_zyg_hvz_mqb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the record in Enterprise Service Management Integrations Framework: Sumtotal

</td></tr><tr><td>

Properties

</td><td>

Set of properties that are predefined for the Sumtotal application.

 -   **full\_pull**: When set to **True**, all the learning courses are pulled from Sumtotal into the ServiceNow application. When set to **False**, updated learning courses and learning courses progress are pulled from Sumtotal into the ServiceNow application.
-   **url\_prefix**: Deep link prefix to pull learning objects from Sumtotal during run time.

</td></tr><tr><td>

Integration Services

</td><td>

Services interact with the Sumtotal application to pull or push learning courses.

 -   **Assign course in Sumtotal**: Assigns a course to an employee in the Sumtotal application.
-   **Pull Courses**: Pulls learning courses from the Sumtotal application into the ServiceNow application.
-   **Sync users**: Maps users in the Sumtotal system to users in the ServiceNow system using user IDs.
-   **User activity**: Pulls details of user activity on learning courses from the Sumtotal application into the ServiceNow application.

</td></tr></tbody>
</table><table id="table_smk_stz_hrb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the record in Enterprise Service Management Integrations Framework: Saba

</td></tr><tr><td>

Properties

</td><td>

Set of properties that are predefined for the Saba application.-   **full\_pull**: When set to **True**, all the learning courses are pulled from Saba into the ServiceNow application. When set to **False**, updated users, learning courses, and learning course progress are pulled from the Saba system into the ServiceNow application.
-   page\_size: Number of records that are pulled per page.

</td></tr><tr><td>

Integration Services

</td><td>

Services that interact with the Saba application to pull or push learning courses.-   **Course assign service**: Assigns a course to an employee in the Saba application.
-   **Pull Courses from Saba**: Pulls learning courses from the Saba application into the ServiceNow application.
-   **Sync Saba Users**: Maps users in the Saba system to users in the ServiceNow application based on email IDs.
-   **Pull Saba User Course Activity**: Pulls details of user activity on learning courses from the Saba application into the ServiceNow application.

</td></tr></tbody>
</table>**Parent Topic:**[Integrating Learning Core with third-party learning management systems](../task/setup-learning-third-party-1.md)

