---
title: Assign Developer Sandboxes packs
description: Assign Developer Sandboxes packs to managed instances from the App Engine Management Center \(AEMC\).
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/app-engine-management-center/assign-dsb-packs-aemc.html
release: brazil
product: App Engine Management Center
classification: app-engine-management-center
topic_type: task
last_updated: "2026-09-23"
reading_time_minutes: 2
keywords: [Assign Developer Sandboxes packs, Assign Developer Sandboxes packs in AEMC, Developer Sandboxes, App Engine Management Center, AEMC, Developer Sandboxes license assignment, Assign DSB packs in AEMC]
breadcrumb: [Manage app development, Use, App Engine Management Center, Run, AI Workflow Factory, Building applications]
---

# Assign Developer Sandboxes packs

Assign Developer Sandboxes packs to managed instances from the App Engine Management Center \(AEMC\).

## About this task

Developer Sandboxes are packaged in increments of 10, called packs. For more information about Developer Sandboxes entitlements and limits, see [Developer Sandboxes entitlements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/developer-sandboxes/dev-sbx-entitlements.md).

## Before you begin

**Warning:** Developer Sandboxes pack assignments are permanent after they are submitted. Plan your sandbox pack assignment before you begin to avoid unintentional assignment.

-   The Developer Sandboxes Licensing plugin \(com.glide.dsb.licensing\) must be installed on your controller instance.
-   The Developer Sandboxes plugin \(com.glide.dsb\) must be installed on the instances you want to assign Developer Sandboxes packs to.
-   Multi-Instance Management is required for assigning Developer Sandboxes licenses. It depends on the Multi-Instance Setup app \(`sn-app-amf`\), which must be installed separately from the ServiceNow® Store. This app is not a dependency of the `com.glide.dsb.licensing` plugin and is not installed automatically. For details on adding managed instances, see [Connecting controller and managed instances](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/connecting-controller-managed-instances.md).


Role required: sn\_dsb\_commons.sandbox\_license\_admin or admin

## Procedure

1.  Navigate to **All** &gt; **App Engine** &gt; **Administration** &gt; **App Engine Management Center**.

2.  Select the Developer Sandboxes page.

    \[Omitted image "dsb-assignment-page.png"\] Alt text: Developer Sandboxes page in AEMC that displays the number of purchased, unassigned, and free sandbox packs that you have, and which instances have packs already assigned.

3.  Select **Assign sandboxes**.

4.  In the **Instance** field, select the instance to assign Developer Sandboxes packs to.

    Multi-Instance Management is required for assigning Developer Sandboxes licenses. It depends on the Multi-Instance Setup app \(`sn-app-amf`\), which must be installed separately from the ServiceNow® Store. This app is not a dependency of the `com.glide.dsb.licensing` plugin and is not installed automatically. For details on adding managed instances, see [Connecting controller and managed instances](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/connecting-controller-managed-instances.md).

    The **Assign sandboxes** modal displays **Ready** by the instance name to indicate that the selected instance can be assigned sandboxes \(has the prerequisite Developer Sandboxes required plugins installed and Multi-Instance Management configured\). When an instance does not meet the requirements for sandbox assignment, an error message appears.

    \[Omitted image "dsb-assignment-instance-ready.png"\] Alt text: Assign sandboxes modal with an instance selected that is a managed instance.

5.  Select the plus icon \[Omitted image "dsb-add-icon.png"\] Alt text: to add packs or the minus icon \[Omitted image "dsb-remove-icon.png"\] Alt text: to remove packs.

    The maximum number of packs you can assign to an instance is 3 \(30 sandboxes\).

6.  If a free pack is available, toggle on the switch to allocate the 4 free sandboxes to the selected instance.

7.  Select the check box **I understand that assignments are permanent**.

8.  Select **Save**.


## Result

You have assigned Developer Sandboxes packs.

## What to do next

For more information about Developer Sandboxes, see [Developer Sandboxes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/developer-sandboxes/sandboxes-landing.md).

**Parent Topic:**[Managing app development using the App Engine Management Center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/app-engine-management-center/managing-app-development-using-aemc.md)

