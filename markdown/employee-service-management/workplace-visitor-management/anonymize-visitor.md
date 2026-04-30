---
title: Anonymize a visitor
description: As an admin, you can anonymize a visitor to delete the visitor record and all the details of the visitor. Any future registrations of the visitor are canceled.
locale: en-US
release: xanadu
product: Workplace Visitor Management
classification: workplace-visitor-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Manage visitor registrations, Workplace Visitor Management, Workplace Service Delivery, Employee Service Management]
---

# Anonymize a visitor

As an admin, you can anonymize a visitor to delete the visitor record and all the details of the visitor. Any future registrations of the visitor are canceled.

## Before you begin

Role required: sn\_wsd\_visitor.admin

## About this task

As an admin, you can anonymize a visitor. Employees can request to anonymize a visitor due to security reasons or for any other reason.

When you anonymize a visitor, the visitor record is deleted. In all current visitor registrations, the visitor data is replaced with a random value. Any future registrations of the visitor are canceled.

**Note:**

-   If you have installed Workplace Services Kiosk, any visitor pictures and signatures are removed when you anonymize a visitor.
-   After you anonymize a visitor, the visitor details must be deleted from the audit records for one time. To automatically delete the details from the audit records, a fixed script is provided along with the application on the store. Download the fixed script **WSD\_Fix\_Visitor\_Anonymize\_data.xml** attached with the Workplace Visitor Management application from the ServiceNow Store under the supporting documents.

## Procedure

1.  Navigate to **System Definition** &gt; **Tables**.

2.  Search for the Visitor \[sn\_wsd\_visitor\_visitor\] table.

    -   In the **Label** field, type `Visitor`.
    -   In the **Name** field, type `sn_wsd_visitor_visitor`.
3.  Select the Visitor \[sn\_wsd\_visitor\_visitor\] table.

4.  Under Related links, select **Show List**.

5.  In the application **Filter navigator**, type `sn_wsd_visitor_visitor.list` and search.

6.  From the list of visitors, select the visitor that you want to anonymize.

7.  On the visitor form, select **Anonymize Visitor Data**.

8.  In the Confirmation dialog box, click **OK**.


## Result

The visitor is anonymized and all the details of the visitor are deleted. Any future registrations for the visitor are canceled, and the data in the fields are replaced with random values.

**Parent Topic:**[Manage visitor registrations](../concept/manage-visitor-registrations.md)

**Related topics**  


[Update a visitor registration](update-visitor-registration.md)

[View visitor registrations](view-visitor-registrations.md)

[View visitor policy confirmations](view-policy-confirmations.md)

[Visitor registration states](../reference/visitor-registration-states.md)

[Apply visitor management archive policy](apply-visitor-management-archival-rule.md)

