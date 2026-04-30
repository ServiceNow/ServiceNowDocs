---
title: Universal Request for Health and Safety cases
description: With the integration of Health and Safety Case Management and Universal Request applications, you can provide a consistent user experience for employees while creating service requests.
locale: en-US
release: yokohama
product: Health and Safety Case Management
classification: health-and-safety-case-management
topic_type: concept
last_updated: "2025-11-24"
reading_time_minutes: 2
breadcrumb: [Health and Safety Case Management, Health and Safety, Employee Service Management]
---

# Universal Request for Health and Safety cases

With the integration of Health and Safety Case Management and Universal Request applications, you can provide a consistent user experience for employees while creating service requests.

## Universal Request for Health and Safety Case Management Workflow

A universal request gets created when an employee selects the **Request help** option in the Employee Center. On the **Request help** form, when the employee selects the **Issue contains sensitive or confidential information** check box, a drop-down menu to **Select the department for your issue** appears. When the employee selects **Health and Safety** and then selects **Submit**, the system automatically creates a Universal Request with Health and Safety case as a primary ticket.

All the important details, such as, users who are working on the issue, inter-department transfers, and work notes, are recorded in the universal request ticket. This provides complete visibility to the employee who has raised the request.

## Universal Request for Health and Safety Case Management overview

-   The **Health and safety routing group** contains agents with roles required to manage the universal requests with Health and Safety cases on the Health and Safety Workspace. Organizations can add users to this group for them to access the Health and Safety Workspace and also the Universal Request in the Health and Safety Workspace.
-   The Health and Safety cases that are associated with Universal Request appear under **All** &gt; **Health and Safety** &gt; **Health and Safety Cases** &gt; **All** and all the Universal Requests appear under the **Universal Request** &gt; **All** list.
-   The detail tab of the **Universal Request** record displays the **Primary ticket** field where you can preview the Health and Safety case that is associated with the universal request record.
-   The agent who has the case assigned to them, can view the **Transfer** button on the Health and Safety case record associated with the Universal Request. The agent can use the **Transfer** option to close current Health and Safety case record and move the Universal Request to another department or service.
-   The agent who is part of the **Health and safety routing group** can use the **Create Health and Safety Cases** option on the universal request record accessed from the Health and Safety Workspace to create a health and safety case. The new health and safety case will automatically be associated with the universal request and it also becomes the primary ticket for the universal request.
-   The safety requests that are created and are associated with Universal Request initiated by the current user on the Employee Center, appear under **Employee Center** &gt; **My Requests**.

## Installing the necessary plugins

The Universal Request \(com.snc.universal\_request\) plugin must be installed along with Health and Safety Case Management \(sn\_hs\_cm\) for this feature to operate seamlessly.

