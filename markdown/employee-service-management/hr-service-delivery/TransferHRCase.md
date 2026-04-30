---
title: Move an HR case from one HR service to another
description: You can reclassify an HR case that you originally create under one HR service but want to move it under a different HR service.
locale: en-US
release: zurich
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Transfer an HR case, Use HR Case Management, Configure, Case and Knowledge Management, HR Service Delivery, Employee Service Management]
---

# Move an HR case from one HR service to another

You can reclassify an HR case that you originally create under one HR service but want to move it under a different HR service.

## Before you begin

Role required: sn\_hr\_core.case\_writer

## About this task

You can also retain the details of the original case. For example, you can take a General Inquiry case and reclassify it as a Medical Benefits Inquiry case.

## Procedure

1.  Open an existing HR case.

2.  From **Additional actions**, select **Transfer Case**.

3.  From **Transfer type**:

    -   **Transfer with existing case number**: The HR case number does not change, links redirect with new case, and work notes transfer to new case.
    -   **Transfer to a new case number**: The HR case number changes, links do not redirect, and work notes do not transfer. Both HR case numbers appear on the HR case for reference.
4.  From **New HR Service**, select the HR service you want to assign to your original case.

5.  Select **OK**.

    The current case and its child tasks close. When you transfer an HR case from one HR service to another, some field values do not transfer to the new case. The Opened for person receives a notification email with the closed case and transferred case information. Replies to the email appear in the Comments section of the HR case. If the subject person replies to the email associated with the closed case, the reply appears in the comments for both the closed and transferred cases.

    **Note:** If the sn\_hr\_core.restrict\_guest\_email system property is False \(default\), text from an email appears in the Work notes field when the employee is responding from a personal email account.

    See [Email setup](https://www.servicenow.com/docs/access?context=c_EmailConfiguration&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).


**Parent Topic:**[Transfer an HR case](../concept/reclassify-hr-case.md)

