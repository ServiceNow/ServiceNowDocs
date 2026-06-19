---
title: Notifications on tool credential expiration
description: Notifications are sent to tool users on expiration of tool credentials to alert them. Notifications are also sent proactively before the expiration of tool credentials for GitHub tools created with basic authentication. This enables tool users with the sn\_devops.tool\_owner or sn\_devops.admin roles to update the tool credentials and prevent any loss of data.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-service-management/devops-change-velocity/notifications-for-tool-credential-expiry.html
release: zurich
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Update third-party tool credentials, Integrate, DevOps Change Velocity, IT Service Management]
---

# Notifications on tool credential expiration

Notifications are sent to tool users on expiration of tool credentials to alert them. Notifications are also sent proactively before the expiration of tool credentials for GitHub tools created with basic authentication. This enables tool users with the sn\_devops.tool\_owner or sn\_devops.admin roles to update the tool credentials and prevent any loss of data.

A universal task is created and assigned to users with the sn\_devops.tool\_owner role who are part of any user group specified in the **Maintained by** field, and any user with the sn\_devops.admin role. They will be notified of the universal task through notification \(in the bell icon\), email, and an open task in the workspace home page.

\[Omitted image "credentials-expiry-maintainedby.png"\] Alt text: Maintained by field in the tool record

Notifications are also displayed in the tool record in the form of a banner message to any user with access to the tool when the tool credentials expire. But the credentials can be updated only by users with the sn\_devops.tool\_owner or sn\_devops.admin role.

The credentials expiration check happens in the system every one hour. If your tool credentials have expired, it might take a maximum of one hour for the system to send notifications.

For GitHub tools created with basic auth, notifications are also sent proactively before the expiration of tool credentials. Apart from the universal task and banner notification, a field message is also displayed in the case of proactive expiration notifications. You can set the number of days before which expiration notifications must be sent in the **Number of days before tool credential expiry to assign a universal task and notify \(if applicable\)** property. By default, it is set to 3 days. To stop sending proactive notifications, select 0 as the value for this property. \[Omitted image "credentials-expiry-property.png"\] Alt text: Properties to configure notifications on tool credential expiry

If you want to stop sending notifications for expired credentials after expiry, disable the **Assign a universal task and notify to update tool credentials when expired** property. For more information, see [DevOps Change Velocity properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/devops-change-velocity/dev-ops-administration.md).

The following types of notifications are sent:

-   **Universal task**

    A universal task is created and notifications are sent to users with the sn\_devops.tool\_owner role who are part of any user group specified in the **Maintained by** field, and any user with the sn\_devops.admin role.

    \[Omitted image "credentials-expiry-bell-notifications.png"\] Alt text: Bell notifications on credentials expiration

    \[Omitted image "credentials-expiry-email-notification.png"\] Alt text: Email notification on credential expiration

    \[Omitted image "credentials-expiry-landing-page.png"\] Alt text: Open task on landing page on credential expiration

-   **Banner message**

    A banner message is displayed on the tool record to all users with access to the tool record.

    \[Omitted image "credentials-expiry-banner-notification.png"\] Alt text: Banner notification on credential expiration

-   **Field message**

    A field message is displayed on the **Credentials expiration** field in the tool record for a GitHub tool created with basic auth.

    \[Omitted image "credential-expiry-proactive-field.png"\] Alt text: Proactive field notification before credential expiration


When the credentials of your tool expire, the tool gets disconnected. You can select the **Update credentials** link in the notifications, and update your tool credentials. After the credentials are updated, connect to the tool again to start receiving data. For information on updating tool credentials, see [Update third-party tool credentials in DevOps Change Velocity](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/devops-change-velocity/update-third-party-tool-credentials-in-devops-change-velocity.md).

**Parent Topic:**[Update third-party tool credentials in DevOps Change Velocity](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/devops-change-velocity/update-third-party-tool-credentials-in-devops-change-velocity.md)

