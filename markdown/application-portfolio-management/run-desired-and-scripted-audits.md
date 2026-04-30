---
title: Run audits to determine invalid and missing configuration data
description: Run the scripted audits and desired state audit to determine invalid and missing information in the configuration data. These audits help you find the gaps in business capability, business application, software models, and the life-cycle information.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 5
breadcrumb: [Configure, Enterprise Architecture \(formerly Application Portfolio Management\), Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# Run audits to determine invalid and missing configuration data

Run the scripted audits and desired state audit to determine invalid and missing information in the configuration data. These audits help you find the gaps in business capability, business application, software models, and the life-cycle information.

## Before you begin

Role required: sn\_apm.apm\_admin

## About this task

You can identify records that have gaps in their relationship with other configuration items by running the scripted audits. Such gaps in establishing the following relationships cannot give you a realistic appraisal of the business capabilities and the business applications that they are tied to.

-   Between the business capability and the business application
-   Between the business application and the software models
-   The software products with no life-cycle data

As a user with the sn\_apm.apm\_admin role, you require all the configuration items to be related appropriately to assess your business applications and to estimate and evaluate the business capabilities of your enterprise.

## Procedure

1.  Navigate to **All** &gt; **Enterprise Architecture** &gt; **Administration** &gt; **Desired State Audits** or **Scripted Audits**.

2.  Click the audit name.

3.  Click **Run Audit**.

    Running the audits help you to do the following:

    -   Identify the records that match the respective criteria.
    -   Create tasks to address the disparity in the records.
    -   Communicate to the owners of the IT business application, software model, and the business capability through an email notification to resolve the gap or certify the data.

        Application to facilitate addressing these notifications and to access the applications data, the IT business application owners, software model owners, and the business capability owners are granted the sn\_apm.apm\_user role. Users with this role can navigate to **Compliance** &gt; **My Follow On Tasks** to update the data.

    -   **Hardware Models with no life-cycle data**

        The scripted audit retrieves records of hardware models that don't have life-cycle data, but are used by an application service and are related to a business application. The audit generates tasks and sends email notifications to the hardware model owner.

        **Note:** The system checks only the life-cycle data for production instances of the business application. That is, it doesn't consider non-production instances such as development and test instances.

    -   **Software Products with no life-cycle data**

        The scripted audit retrieves software model records for all product versions used by the business applications that don't have life cycle-data such as life-cycle type, its phase, beginning and end dates of the life-cycle phase, and risk. The audit generates tasks and sends email notifications to the software model owner.

        **Note:** The system checks for the life-cycle data only for production instances of the business application. That is, it doesn't consider non-production instances such as development and test instances.

    -   **Orphaned business capabilities**

        The scripted audit checks the CI relationship \[cmdb\_rel\_ci\] table for capabilities that have no parent capability or child capabilities, and capabilities without any business applications tied to it. A task is created and the owner of the business capability is notified through an email about the assigned task.

    -   **Business applications related to multiple business capabilities in the same hierarchy**

        The scripted audit checks the CI relationship \[cmdb\_rel\_ci\] table for a possibility where the same business application is tied to multiple business capabilities at the same level in the hierarchy. For example, BA1 is tied to Cap 1.1.2 and is also tied to Cap 1.1.2.1. You can understand the hierarchy level of the capability from the Business Capability \[cmdb\_ci\_business\_capability\] table.

    -   **Business applications not related to any software model**

        The audit checks the CI relationship \[cmdb\_rel\_ci\] table for business applications that are not related to any software model. The scripted audit considers only the production instances of business services. A notification is sent to the IT application owner.

        **Note:** The system checks only for production instances of the business application and doesn't consider non-production instances such as development or test instances.

    -   **Business applications not related to any business capability**

        The desired state audit checks the CI relationship \[cmdb\_rel\_ci\] table for business applications that are not related to any business capability.

    -   **Business Applications not related to any Information Objects**

        The desired state audit checks the CI relationship \[cmdb\_rel\_ci\] table for business applications that are not related to any information object. If an unrelated business application is found, a notification is sent to the IT application owner.

    -   **Business Application and Information Object relation not captured in relation attributes**

        The desired state audit checks the CI Relation Attributes \[cmdb\_rel\_attributes\] table for CI relationships between the business application and the information objects. If relationship attributes are not found, a notification is sent to the business owner.

    -   **CRUD information not captured for Business Application and Information Object relation**

        The desired state audit checks the CI Relation Attributes \[cmdb\_rel\_attributes\] table for CI relationships between the business application and the information objects. If relationship attributes are found but the qualifier properties information for CRUD is empty, a notification is sent to the business owner.

    -   **Information Objects not related to any Business Application**

        The desired state audit checks the Information Object \[cmdb\_ci\_information\_object\] table for information objects that are not tied to any business application. You can run such audits on demand. If there is any unrelated information object found, then a notification is sent to the owner of the information object mentioned in the **Assign to** field.

    In addition, whenever a [certification schedule either On Demand or Quarterly](schedule-data-in-business-applications.md) is executed, a notification is shown on the Enterprise Architecture home page. For each certification schedule that is executed, a corresponding notification entry appears on the home page. The notification shows open certification instances that are not 100% complete. Conversely, the home page section doesn't display certification instances that are 100% complete and have not been generated at all.

    Notifications are also shown for software models that are at high and moderate risks on the current date and within the next 90 days. The risk factors of software models tied to business applications that are related to production instances are only considered. Click the notification to open the related records from the software model table.

    The scripted and desired state audit results are also posted in the [Notification section of the Application Portfolio Management Home page](../concept/application-portfolio-management-home.md#dt_ots_1gr_2wb). Click the notification to open the related tasks or the related data certification tasks.


**Parent Topic:**[Configuring Enterprise Architecture \(formerly Application Portfolio Management\)](../concept/configure-apm.md)

