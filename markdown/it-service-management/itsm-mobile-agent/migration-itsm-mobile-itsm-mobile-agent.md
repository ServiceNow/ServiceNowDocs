---
title: Migration from ITSM Mobile to ITSM Mobile Agent
description: The ITSM Mobile plugin \(com.sn\_itsm\_mobile\) was deprecated in Quebec. The existing customers can migrate to ITSM Mobile Agent for enhanced mobile-first experiences in the base system, designed for agents to triage, act on, and resolve incidents on the go. ITSM Mobile Agent application improves productivity with an intuitive interface to manage all the work, view schedules, check who is on-call, respond to major incidents, and more.After you install the ServiceNow Agent app, avoid duplication of launcher screens and notifications from the deprecated ITSM Mobile app.When migrating from ITSM Mobile to ITSM Mobile Agent, an admin must verify if any customizations are defined in the deprecated ITSM Mobile application scope. Such customizations should be deactivated or moved to the ITSM Mobile Agent scope.
locale: en-US
release: zurich
product: ITSM Mobile Agent
classification: itsm-mobile-agent
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Configure, ITSM Mobile Agent, IT Service Management]
---

# Migration from ITSM Mobile to ITSM Mobile Agent

The ITSM Mobile plugin \(com.sn\_itsm\_mobile\) was deprecated in Quebec. The existing customers can migrate to ITSM Mobile Agent for enhanced mobile-first experiences in the base system, designed for agents to triage, act on, and resolve incidents on the go. ITSM Mobile Agent application improves productivity with an intuitive interface to manage all the work, view schedules, check who is on-call, respond to major incidents, and more.

For information about getting started with ITSM Mobile Agent, see [Log in to ITSM Mobile Agent](../task/install-itsm-mobile-app.md).

**Parent Topic:**[Configuring ITSM Mobile Agent](configuring-itsm-mobile-agent.md)

## Deactivate the ITSM Mobile launcher screens and notifications

After you install the ServiceNow Agent app, avoid duplication of launcher screens and notifications from the deprecated ITSM Mobile app.

### Before you begin

Role required: admin

### About this task

After installing the ITSM Mobile Agent app on your instance, you can still view the launcher screens from the ITSM Mobile application when you log in to the ServiceNow Agent app \(Android or iOS\). Also, you might receive duplicate notifications since both ITSM Mobile and ITSM Mobile Agent apps are active on your instance.

![Screenshot for deprecated applet launchers for incidents and approvals](../image/dep-incidents-approvals.png "Deprecated applet launchers for incidents and approvals")

Since no updates are supported on the ITSM Mobile plugin \(com.sn\_itsm\_mobile\), it's recommended that customers stop using the related deprecated features. It's also recommended that applets or applet launchers from both plugins \(ITSM Mobile and ITSM Mobile Agent\) aren't active at the same time.

Since the single-click uninstallation of plugins isn't supported, the deprecated plugin isn't deactivated in the base system. Hence, deactivate the applet launchers and notifications that exist in the deprecated ITSM Mobile plugin.

### Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **Studio**.

2.  From the Select Application pop-up window, open the ITSM Mobile application in the studio.

3.  To deactivate the ITSM Mobile launcher screens, perform the following steps:

    1.  To deactivate the **Incidents** launcher screen, perform the following steps:

        1.  Navigate to **Mobile Studio** &gt; **Applet launchers** &gt; **Incidents**.
        2.  From the header menu, make this launcher screen inactive by using the **Active** toggle switch.
        3.  Click **Save**.
    2.  To deactivate the **My Approvals** launcher screen, perform the following steps:

        1.  Navigate to **Mobile Studio** &gt; **Applet launchers** &gt; **My Approvals**.
        2.  From the header menu, make this launcher screen inactive by using the **Active** toggle switch.
        3.  Click **Save**.
    When you log into the ServiceNow Agent app, the deprecated launcher screens aren’t displayed.

    ![Screenshot for ServiceNow Agent app without deprecated launcher screens](../image/deactive_result_mobile.png "ServiceNow Agent app without deprecated launcher screens")

4.  To deactivate the ITSM Mobile notifications, perform the following steps:

    1.  To deactivate the notifications related to assigned approvals, perform the following steps:

        1.  Navigate to **Notifications** &gt; **Notifications** &gt; **Approval assigned to me**.
        2.  Clear the **Active** check box.
        3.  Click **Update**.
    2.  To deactivate the notifications related to commented incidents, perform the following steps:

        1.  Navigate to **Notifications** &gt; **Notifications** &gt; **Incident commented**.
        2.  Clear the **Active** check box.
        3.  Click **Update**.

## Migrate customizations from the ITSM Mobile application scope to the ITSM Mobile Agent scope

When migrating from ITSM Mobile to ITSM Mobile Agent, an admin must verify if any customizations are defined in the deprecated ITSM Mobile application scope. Such customizations should be deactivated or moved to the ITSM Mobile Agent scope.

The admin must verify if any custom notifications are defined in the deprecated ITSM Mobile application scope. Such notifications should be deactivated or moved to the ITSM Mobile Agent scope.

Similarly, the admin must deactivate or move the custom launcher screens or custom applets to the ITSM Mobile Agent application scope.

**Important:** To move customizations from the ITSM Mobile application scope to the ITSM Mobile Agent application scope, perform one of the following actions:

-   Copy the custom code and paste it in the ITSM Mobile Agent application scope.
-   Redefine the code in the ITSM Mobile Agent application scope.

