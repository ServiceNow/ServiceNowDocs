---
title: Integrate Password Reset with a CMS integration
description: You can configure a site in the ServiceNow content management \(CMS\) application to define a single-site access point that includes the Password Reset service. For example, you can create an employee self-service site that provides Password Reset service.
locale: en-US
release: xanadu
product: Password Reset
classification: password-reset
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configure, Password Reset, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Integrate Password Reset with a CMS integration

You can configure a site in the ServiceNow content management \(CMS\) application to define a single-site access point that includes the Password Reset service. For example, you can create an employee self-service site that provides Password Reset service.

## Before you begin

Role required: content\_admin

## About this task

Each Password Reset process requires a separate CMS page.

## Procedure

1.  Navigate to **All** &gt; **Content Management** &gt; **Specialty Content** &gt; **iFrames** and create an iFrame record.

2.  Go to **Content Management** &gt; **Sites** and create a site that has no login page.

    ![New site](../image/password-reset-cms.png)

3.  Go to **Content Management** &gt; **Pages** and create a password reset page.

4.  Enter the name of the site that you created in the **Content site** field \(**Password Reset self-service** in the example\).

5.  Right-click the form header and click **Save**.

6.  Click the **Edit Page** related link and then click **Add content**.

7.  In the **Content Blocks** section, select the iFrame that you created and add more content as needed.

8.  Click **Update**.


**Parent Topic:**[Configuring Password Reset](../../login/concept/password-reset-admin-guide.md)

