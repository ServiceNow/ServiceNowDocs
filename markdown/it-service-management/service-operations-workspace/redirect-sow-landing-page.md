---
title: Redirect non-admin users to Service Operations Workspace
description: Enable a non-admin user to start prioritizing tasks quickly by redirecting to Service Operations Workspace after logging in to the ServiceNow instance.
locale: en-US
release: zurich
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Landing page redirection in Service Operations Workspace for ITSM, Getting started with Service Operations Workspace for ITSM, Configure, Service Operations Workspace for ITSM, IT Service Management]
---

# Redirect non-admin users to Service Operations Workspace

Enable a non-admin user to start prioritizing tasks quickly by redirecting to Service Operations Workspace after logging in to the ServiceNow instance.

## Before you begin

Role required: sn\_sow\_admin.sn\_sow\_admin, or admin

Ensure that Next Experience is enabled on your instance. For information about its activation, see [Considerations for activating Next Experience](https://www.servicenow.com/docs/access?context=next-experience-adoption-paths&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US).

## Procedure

1.  Navigate to **All** &gt; **Service Operations Workspace Admin Center** &gt; **Overview**.

2.  On the **Overview** tab, from the **Initial Setup** section, select the **Configure the landing page** option.

3.  Select **Initial setup** &gt; **Landing page redirection**.

4.  Configure the SOW redirection property.

    1.  From the **Homepage Destination Rule** section, select **Configure** for SOW Landing Page.

    2.  Select the **Active** check box.

    3.  Select **Update**.

5.  If required, configure the other SOW landing page redirection properties.

    1.  From the **System Properties** section, select **Configure** for the required property.

        -   glide.login.home: If set to true, the default homepage is displayed upon login. If left blank, the last page visited is used. This property is overwritten by the Homepage Destination Rule for the SOW landing page.
        -   glide.next\_experience.user\_selected\_landing\_page\_enabled: Sets the user selected landing page preference to true.
        -   glide.ux.user\_criteria\_enabled: Enables use of user criteria records instead of **Roles** fields for UX Framework variants.
    2.  Modify the property and select **Update**.


**Parent Topic:**[Landing page redirection in Service Operations Workspace for ITSM](../concept/landing-page-redirection-sow-itsm.md)

