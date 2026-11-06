---
title: Migration from ITSM Mobile to ITSM Mobile Agent
description: The ITSM Mobile plugin \(com.sn\_itsm\_mobile\) was deprecated in Quebec. Existing customers can migrate to ITSM Mobile Agent, a mobile-first base system application that agents use to triage, act on, and resolve incidents on the go.After you install the ServiceNow Agent app, avoid duplication of launcher screens and notifications from the deprecated ITSM Mobile app.When migrating from ITSM Mobile to ITSM Mobile Agent, administrators must check whether any customizations are defined in the deprecated ITSM Mobile application scope. Administrators must deactivate or move them to the ITSM Mobile Agent scope.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-service-management/itsm-mobile-agent/migration-itsm-mobile-itsm-mobile-agent.html
release: australia
product: ITSM Mobile Agent
classification: itsm-mobile-agent
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 3
breadcrumb: [Configuring ITSM Mobile Agent, ITSM Mobile Agent, IT Service Management]
---

# Migration from ITSM Mobile to ITSM Mobile Agent

The ITSM Mobile plugin \(com.sn\_itsm\_mobile\) was deprecated in Quebec. Existing customers can migrate to ITSM Mobile Agent, a mobile-first base system application that agents use to triage, act on, and resolve incidents on the go.

ITSM Mobile Agent application improves productivity with an intuitive interface to manage all the work, view schedules, check who is on-call, respond to major incidents, and more.

For information about getting started with ITSM Mobile Agent, see [Log in to ITSM Mobile Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/itsm-mobile-agent/install-itsm-mobile-app.md).

**Parent Topic:**[Configuring ITSM Mobile Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/itsm-mobile-agent/configuring-itsm-mobile-agent.md)

## Deactivate the ITSM Mobile launcher screens and notifications

After you install the ServiceNow Agent app, avoid duplication of launcher screens and notifications from the deprecated ITSM Mobile app.

### Before you begin

Role required: admin

### About this task

After installing the ITSM Mobile Agent app, launcher screens from the ITSM Mobile application remain visible when you log in to the ServiceNow Agent app \(Android or iOS\). Both apps being active on your instance can also cause duplicate notifications.

\[Omitted image "dep-incidents-approvals.png"\] Alt text: Deprecated applet launchers for incidents and approvals in the mobile app

Because no updates are supported on the ITSM Mobile plugin \(com.sn\_itsm\_mobile\), the related deprecated features shouldn't be used. Applets or applet launchers from both plugins \(ITSM Mobile and ITSM Mobile Agent\) shouldn't be active at the same time.

Because the single-tap uninstallation of plugins isn't supported, the deprecated plugin isn't deactivated in the base system. You must deactivate the applet launchers and notifications in the deprecated ITSM Mobile plugin.

### Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **Studio**.

2.  From the Select Application pop-up window, open the ITSM Mobile application in Studio.

3.  To deactivate the ITSM Mobile launcher screens, perform the following steps:

    1.  To deactivate the **Incidents** launcher screen, perform the following steps:

        1.  Navigate to **Mobile Studio** &gt; **Applet launchers** &gt; **Incidents**.
        2.  From the header menu, make this launcher screen inactive by using the **Active** toggle switch.
        3.  Select **Save**.
    2.  To deactivate the **My Approvals** launcher screen, perform the following steps:

        1.  Navigate to **Mobile Studio** &gt; **Applet launchers** &gt; **My Approvals**.
        2.  From the header menu, make this launcher screen inactive by using the **Active** toggle switch.
        3.  Select **Save**.
    When you log in to the ServiceNow Agent app, the deprecated launcher screens aren’t displayed.

    \[Omitted image "deactive\_result\_mobile.png"\] Alt text: ServiceNow Agent app without deprecated launcher screens

4.  To deactivate the ITSM Mobile notifications, perform the following steps:

    1.  To deactivate the notifications related to assigned approvals, perform the following steps:

        1.  Navigate to **Notifications** &gt; **Notifications** &gt; **Approval assigned to me**.
        2.  Clear the **Active** check box.
        3.  Select **Update**.
    2.  To deactivate the notifications related to commented incidents, perform the following steps:

        1.  Navigate to **Notifications** &gt; **Notifications** &gt; **Incident commented**.
        2.  Clear the **Active** check box.
        3.  Select **Update**.

## Migrating customizations from ITSM Mobile application scope to ITSM Mobile Agent scope

When migrating from ITSM Mobile to ITSM Mobile Agent, administrators must check whether any customizations are defined in the deprecated ITSM Mobile application scope. Administrators must deactivate or move them to the ITSM Mobile Agent scope.

Administrators must check whether any custom notifications are defined in the deprecated ITSM Mobile application scope and deactivate or move them to the ITSM Mobile Agent scope.

Administrators must also deactivate or move custom launcher screens or custom applets to the ITSM Mobile Agent application scope.

**Important:** To move customizations from the ITSM Mobile application scope to the ITSM Mobile Agent application scope, perform one of the following actions:

-   Copy the custom code and paste it into the ITSM Mobile Agent application scope.
-   Redefine the code in the ITSM Mobile Agent application scope.

