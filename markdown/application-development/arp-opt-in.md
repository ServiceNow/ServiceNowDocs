---
title: Opt in to Application Runtime Policy
description: Enable Application Runtime Policy for an application that's in development by setting the policy mode on the custom application form.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/arp-opt-in.html
release: brazil
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
keywords: [opt in, Application Runtime Policy, ARP, Tracking, Enforcing]
breadcrumb: [Configure, Application Runtime Policy \(ARP\), Developing your application, Building applications]
---

# Opt in to Application Runtime Policy

Enable Application Runtime Policy for an application that's in development by setting the policy mode on the custom application form.

## Before you begin

Role required: arp\_admin or admin.

## About this task

Application Runtime Policy \(ARP\) is an opt-in feature. It must be activated for each custom application by setting the **Application Runtime Policy** field to the active state while the app is in development. The mode selected when activating ARP determines whether the automatically-generated policy records require manual review and approval.

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **My Company Applications**.

2.  From the **In Development** tab, select the application for which you want to enable ARP.

3.  In the **Design and Runtime** section of the custom application form, select one of the following options in the **Application Runtime Policy** field.

<table><thead><tr><th align="left" id="d167984e110">

Value

</th><th align="left" id="d167984e113">

Description

</th></tr></thead><tbody><tr><td id="d167984e119">

**None**

</td><td>

The default. ARP is not enabled for this application and policies aren't automatically created.

</td></tr><tr><td id="d167984e128">

**Tracking**

</td><td>

ARP is enabled. Policy records are automatically created and approved as you exercise application functionality.**Note:** Tracking mode should only be used during application development. When you're ready to publish your application, change the ARP mode to **Enforcing**.

</td></tr><tr><td id="d167984e142">

**Enforcing**

</td><td>

ARP is enabled. Policy records are automatically created as you exercise application functionality, but out-of-scope access is blocked until you review and approve each policy record.

</td></tr></tbody>
</table>    \[Omitted image "arp-activation.png"\] Alt text: The Application Runtime Policy field is in the Design and Runtime section of the Custom Application form.

    For more information about ARP modes, see [Application Runtime Policy modes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/arp-modes.md).

4.  Select **Update** to save the custom application form.


## Result

ARP is enabled for the application in the selected mode. When you exercise application functionality that accesses out-of-scope resources, ARP creates policy records in the applicable policy tables automatically.

**Parent Topic:**[Configuring Application Runtime Policy](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/configuring-app-runtime-policy.md)

