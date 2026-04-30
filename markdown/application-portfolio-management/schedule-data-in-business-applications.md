---
title: Schedule a data certification task
description: Keep your business applications inventory up to date by certifying the data in the business applications table periodically. Keeping your business application data current helps you to assess your business applications precisely as there are indicators that are dependent on these business applications.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Configure, Enterprise Architecture \(formerly Application Portfolio Management\), Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# Schedule a data certification task

Keep your business applications inventory up to date by certifying the data in the business applications table periodically. Keeping your business application data current helps you to assess your business applications precisely as there are indicators that are dependent on these business applications.

## Before you begin

**Important:**

Starting with the Xanadu release, the legacy certifications schedules module is moved to the Enterprise Architecture Workspace. To learn more, see [Managing requests, certifications, and assessments](../concept/manage-requests-certs-assessments.md).

Role required: sn\_apm.apm\_admin

## About this task

As an administrator with the Enterprise Architecture admin role, you can create and assign the data certification tasks to the system owners for them to certify the business applications data. You also require certification\_filter\_admin role to set filter to those fields that require certification.

Inventory of business applications is created one time. But the data on a business applications table are highly dynamic and keep changing over time. Therefore, it’s imperative to keep the data complete, accurate, and current. Data certification is a platform feature that helps you to keep the data up to date.

The Enterprise Architecture \(com.snc.apm\) plugin installs the Data Certification \(snc.certification\_v2\) plugin and requires no separate subscription.

The following preconfigured certification schedules are available for the administrator to schedule data certification tasks. The certification schedule generates a set of certification tasks based on set conditions.

-   **Business Application Certification On Demand** / **Business Application Certification Quarterly**: Certifies the data in the Business Application \[cmdb\_ci\_business\_app\] table. Use **Business Application Certification On Demand** to schedule as and when required, and **Business Application Certification Quarterly** for every quarter. Use either of the schedules according to the specified time interval or on demand.
-   **Application Service Software Model Certification On Demand**: Certifies the software model and full version fields in the Application Service Software Model \[sn\_apm\_tpm\_service\_software\_model\] table.
-   **Software Product Lifecycle Internal Source Certification on Demand**: Certifies the full version field in the Custom Software Product Life cycle \[sam\_custom\_sw\_product\_lifecycle\] table.

## Procedure

1.  Navigate to **All** &gt; **Enterprise Architecture** &gt; **Administration** &gt; **Certification Schedules**.

2.  Select **New** to create a new record of certification schedule.

    You can also select the preconfigured certification schedules to review the record and update the details, if necessary.

    For field information, see [Certification Schedule form](../reference/certification-schedule-form.md).

3.  Select **Submit**.

4.  Select **Update** to save the changes or **Execute Now** to execute the schedule.

    When you select **Execute Now**, a certification instance is created and as a system administrator you can view it in the **Certification Instances** related list. You can also track the certification instance and the percentage of its completion.

    Related certification tasks \(to verify and certify the data of a business application record\) are created in the **Certification Tasks** related list and is assigned to the application owner. As a administrator you can also track the data certification progress assigned to the application owner.

    When a certification task is newly assigned, reassigned, or is about to expire, you can notify the task owners about the pending status of the task at hand by an email.

    Preconfigured email notifications such as **APM DC task assignment**, **APM DC task reassign**, and **APM DC task expiry** are available that you can trigger depending on the certification task when you execute a schedule by selecting **Execute Now**.

    These email notifications are inactive by default, which you must activate by setting it to true.

5.  To activate the email notifications, navigate to **Service Creator** &gt; **Notifications**.

6.  Select open the APM-related notification record.

7.  Enable the **Active** check box to activate the email notification.


## What to do next

You can review the certification tasks and update them if necessary.

-   **[View and update the application certifications](update-application-certifications.md)**  
A certification instance is a collection of certification tasks to execute a certification schedule. Review the application tasks that you created and update them if necessary.
-   **[Certify data in business applications table](certify-data-in-business-applications.md)**  
As an application owner with the certification role you can view the certification tasks assigned to you and certify the required fields. You can also update the data in the fields and then certify them.

**Parent Topic:**[Configuring Enterprise Architecture \(formerly Application Portfolio Management\)](../concept/configure-apm.md)

