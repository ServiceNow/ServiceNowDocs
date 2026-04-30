---
title: External Content Integration Sources
description: When you integrate Coaching With Learning with third-party learning management systems, the source record for Cornerstone OnDemand, Pluralsight, and Udemy applications are automatically created in the Enterprise Service Management Integrations Framework. These source records contain a predefined set of properties and integration services.
locale: en-US
release: yokohama
product: Workforce Optimization for Customer Service
classification: workforce-optimization-for-customer-service
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Integrate Coaching With Learning with third-party learning management systems, Setting up Coaching in Workforce Optimization for Customer Service, Configuring Workforce Optimization for Customer Service, Workforce Optimization for Customer Service, Customer Service Management]
---

# External Content Integration Sources

When you integrate Coaching With Learning with third-party learning management systems, the source record for Cornerstone OnDemand, Pluralsight, and Udemy applications are automatically created in the Enterprise Service Management Integrations Framework. These source records contain a predefined set of properties and integration services.

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
-   **full\_pull**: When set to **True**, all the active users and learning courses from the Cornerstone OnDemand system are pulled into the ServiceNow instance.

When set to **False**, modified users, modified transcripts, and updated courses are pulled from the Cornerstone OnDemand system into the ServiceNow instance.

-   **url\_prefix**: Deep link prefix to pull learning objects from Cornerstone OnDemand system during run time.
-   **pull\_offset\_hours**: The time, in hours, calculated from the last successful run for the next synchronization to occur

For example, the last successful run was on 12/12/2021 at 17:00:00, pull\_offset\_hours is set to 5, and full\_pull is set to False. The next pull fetches all the records that have been modified from 12/12/2021 12:00:00 until current date and time.


</td></tr><tr><td>

Integration Services

</td><td>

Services interact with Cornerstone Ondemand application to pull or push learning courses.-   **Course assign service**: Assigns a course to an employee in the Cornerstone Ondemand application.
-   **Sync users**: Maps users in the Cornerstone OnDemand system to users in the ServiceNow system using email Ids.

**Note:** If you want to use user\_id or user\_name field for mapping users, then override**getCornerstoneUser method** in the sn\_lc.UserMappingUtil script.

-   **Courses**: Pulls learning courses from Cornerstone OnDemand system into ServiceNow.
-   **User activity**: Pulls details of user activity on learning courses from Cornerstone OnDemand system into ServiceNow.

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

Integration services interact with Plural sight application to pull learning courses into ServiceNow.-   **Courses**: Pulls learning courses from Pluralsight into ServiceNow.
-   **Course progress**: Pulls the progress of learning courses from Pluralsight into ServiceNow.

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

Set of properties that are predefined for the Udemy system.-   **page\_size**: Number of records that are pulled through an API call from Udemy into ServiceNow.
-   **full\_pull**: When set to **True**, all the learning courses are pulled from Udemy into the ServiceNow instance. When set to **False**, updated learning courses and learning course progress are pulled from Udemy into the ServiceNow instance.
-   **pull\_offset\_hours**: Value that is considered for pulling modified records.

For example, the last successful run was on 12/12/2021 at 17:00:00, pull\_offset\_hours is set to 5, and full\_pull is set to False. The next pull fetches all the records that have been modified from 12/12/2021 12:00:00 until current date and time.


</td></tr><tr><td>

Integration Services

</td><td>

Integration services interact with Udemy application to pull learning courses into ServiceNow.-   Pull Courses: Pulls learning courses from Udemy into ServiceNow.
-   Pull user activity: Pulls details of user activity on learning courses from Udemy into ServiceNow.

</td></tr></tbody>
</table>**Parent Topic:**[Integrate Coaching With Learning with third-party learning management systems](../task/integrate-learning-third-party-configurable-wfo-cs.md)

