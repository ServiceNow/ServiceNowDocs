---
title: Employee Readiness Core Approval Portal
description: The Employee Readiness Core Approval Portal enables you to approve or deny submitted COVID-19 vaccine doses, vaccine exemptions, and health tests.
locale: en-US
release: zurich
product: Employee Readiness Core
classification: employee-readiness-core
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Employee Readiness Core, Safe Workplace, Health and Safety, Employee Service Management]
---

# Employee Readiness Core Approval Portal

The Employee Readiness Core Approval Portal enables you to approve or deny submitted COVID-19 vaccine doses, vaccine exemptions, and health tests.

## Installation and setup requirements

The Approval Portal is included with Employee Readiness Core. To use the Approval Portal, your organization must install Health and Safety Testing and Vaccination Status.

**Note:** Both applications must be installed, but your organization does not have to use both applications.

-   For more information on installing Health and Safety Testing, see [Install Health and Safety Testing](../../health-safety-testing/task/install-health-testing.md#).
-   For more information on installing Vaccination Status, see [Install Vaccination Status](../../vaccination-status/task/install-vaccination-status.md#).

## Using the Approval Portal

To use the Approval Portal, you must have either the Vaccination Status admin \[sn\_imt\_vaccine.admin\], Health and safety approver \[sn\_imt\_core.health\_and\_safety\_approver\], or Approval Portal manager \[sn\_imt\_core.approval\_portal\_manager\] roles.

Managers with the Approval Portal manager role can see only approvals for their direct reports. This role is automatically assigned to all managers as long as one of the following properties is enabled:

-   Allow managers the ability to update health test results \[sn\_imt\_health\_test.allow\_managers\_ability\_to\_update\_test\_result\_records\]
-   Allow managers the ability to update vaccine response records \[sn\_imt\_vaccine.allow\_managers\_ability\_to\_update\_vaccine\_response\_records\]
-   Allow managers the ability to update vaccine exemption requests \[sn\_imt\_vaccine.allow\_managers\_ability\_to\_update\_vaccine\_exemption\_records\]

Each property provides managers access to the Approval Portal, however, managers are able to see and interact with only records associated with the activated property. Activating multiple properties grants additional capabilities to the reviewing managers.

You can perform the following tasks on the Approval Portal:

-   View and approve or deny COVID-19 health test results. For more information, see [Confirm COVID-19 test results for a user](../../health-safety-testing/task/confirm-health-test-result.md).
-   View and approve or deny an employee's vaccination status and dose details. For more information, see [Confirm the reported vaccination status for a user](../../vaccination-status/task/confirm-vaccine-response.md).
-   View and approve or deny employee vaccination exemption requests. For more information, see [Confirm a vaccine exemption request for a user](../../vaccination-status/task/confirm-vaccine-exemption-request.md).
-   Review attachments and documentation submitted with the user's responses and requests. Supported documents open in the document viewer. For more information on supported formats, see [Document Viewer](https://www.servicenow.com/docs/access?context=Documentviewer&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).
-   Review and add work notes to the records.

The Employee readiness approvals page provides employee vaccine and health records in the tabs listed in the following table. You can filter the records that are displayed by selecting a record type from the **Record type** field list, using the search bar, or changing the **Sort** field list.

**Note:** The search behavior for the Approval Portal is a starts with search.

|Tab|Description|
|---|-----------|
|Approvals to review|Lists records that have not been approved or denied.|
|Approved|Lists all approved vaccine responses, exemption requests, and health tests.|
|Denied|Lists all denied vaccine responses, exemption requests, and health tests.|

**Parent Topic:**[Employee Readiness Core](employee-readiness-core.md)

