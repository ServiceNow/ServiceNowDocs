---
title: Prevent users from canceling module transactions
description: You can explicitly prevent users from canceling the activity of a module by updating the module definition.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-user-interface/t\_PrevUsersCancelModTrans.html
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Navigation action cancellation, User interface configuration, Working in Core UI, Configure UIs and portals, Configure user experiences]
---

# Prevent users from canceling module transactions

You can explicitly prevent users from canceling the activity of a module by updating the module definition.

## Before you begin

Role required: admin

## Procedure

1.  Point to the application menu you want to add the module to and click the edit application \(pencil\) icon.

2.  In the **Modules** related list, click the module you want to prevent users from canceling.

3.  [Configuring the form layout](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/configure-form-layout.md) layout and add the field **Uncancelable by Other Modules**.

4.  Select the check box for **Uncancelable by Other Modules**.

    \[Omitted image "600px-Uncancelable\_by\_other\_modules.png"\] Alt text: Prevent users from canceling this module when they navigate away

5.  Click **Update**.


**Parent Topic:**[Navigation action cancellation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/c_CancelingNavigationActions.md)

**Related topics**  


[Add sites to the always cancel list]()

