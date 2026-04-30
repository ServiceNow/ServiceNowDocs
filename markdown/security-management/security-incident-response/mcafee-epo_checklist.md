---
title: Checklist for the McAfee ePO integration
description: Use this checklist to guide you through all the tasks of the integration. The following checklist includes setup and installation tasks and examples of use cases that include expected results for the integration.
locale: en-US
release: xanadu
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 5
breadcrumb: [McAfee ePO integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Checklist for the McAfee ePO integration

Use this checklist to guide you through all the tasks of the integration. The following checklist includes setup and installation tasks and examples of use cases that include expected results for the integration.

## Before you begin

Role required: Roles are listed for each step.

## About this task

Track your progress with the setup, installation, and configuration of the integration with the following table. Complete all the tasks for a step before moving on to the next step. Each row of the table lists tasks and identifies the roles that are required to perform the tasks. Numbered topics of the installation and configuration guide are also referenced.

## Procedure

1.  Follow the steps in the table in the order that they are presented.

<table id="table_f2c_xn4_sgb"><thead><tr><th>

Item

</th><th>

Description

</th></tr></thead><tbody><tr><td>

![Check box.](../../vulnerability-response/image/checkbox.png)

</td><td>

As a user with the ServiceNow AI Platform® administrator role, set up your ServiceNow AI Platform® instance.1.  Assign ServiceNow AI Platform® and Security Incident Response roles.
2.  Verify that any ServiceNow Security Incident Response and other plugins that support the integration are installed and activated for your release of the ServiceNow AI Platform.
3.  Install and configure a MID server in your ServiceNow AI Platform® instance.
4.  Create an approval group if you want to process requests submitted from the security incident analyst for the isolate host and initiate malware scan actions.
For more information, see [Set up your ServiceNow AI Platform instance for the McAfee ePO integration](../reference/mcaffee-epo-setup-now.md).

</td></tr><tr><td>

![Check box.](../../vulnerability-response/image/checkbox.png)

</td><td>

As McAfee ePO administrator, set up your McAfee ePO console.1.  Verify that you are using version 5.9 of McAfee ePO.
2.  Install the ServiceNow extension plugin in your McAfee ePO console.
3.  Verify you have created security tags in your McAfee ePO console for the isolate host and initiate malware scan actions.
For more information, see [Set up your McAfee ePO console to integrate with Security Incident Response \(SIR\)](mcafee-epo-setup-mcafee.md). For more information and to obtain the extension plugin file, in your ServiceNow AI Platform instance, navigate to **Knowledge** &gt; **Articles** &gt; **All** and, in the Search field, enter, `ServiceNow Security Operations Extension for McAfee ePO`.

</td></tr><tr><td>

![Check box.](../../vulnerability-response/image/checkbox.png)

</td><td>

As a user with the ServiceNow AI Platform administrator role, install the McAfee ePO application from the ServiceNow Store, configure a server, and connect to the McAfee ePO console.For more information, see [Install the application and configure a server for the McAfee ePO integration](mcaffe-epo-install.md).

</td></tr><tr><td>

![Check box.](../../vulnerability-response/image/checkbox.png)

</td><td>

As a user with the ServiceNow AI Platform security incident administrator role, edit the security tag names in your ServiceNow AI Platform® instance so that they match the tag names that you created in your McAfee ePO console.For more information, see [Edit security tags in the ServiceNow AI Platform for the McAfee ePO integration](mcafee-epo-match-tags.md).

</td></tr><tr><td>

![Check box.](../../vulnerability-response/image/checkbox.png)

</td><td>

As a user with the security incident administrator role, create a profile for McAfee ePO capabilities. For information about profiles, see [McAfee ePO integration capability profiles](../concept/mcafee-epo-creating-profiles.md). For the steps required to create a profile, see [Create a capability profile for the McAfee ePO integration](mcafee-epo-create-profile.md).

</td></tr><tr><td>

![Check box.](../../vulnerability-response/image/checkbox.png)

</td><td>

As a user with the security incident administrator role, configure a profile and test security incidents. 1.  Review the information about triggering conditions and settings.
2.  Configure a profile.
3.  Test and preview security incidents.
4.  Locate search results and other details on the related lists on the security incident.
5.  Create and Configure different types of profiles and test security incidents for each type.
 For information about triggering conditions and the alternate CI field, see [Defining triggering conditions with a Configuration item \(CI\) field for a McAfee ePO profile](../concept/mcafee-epo-alternate-ci.md). For the steps required to configure a profile, test, and preview security incidents and examples of profile types, see the examples that follow [Configuring profiles for the McAfee ePO integration](../concept/mcafee-epo-configuring-profile.md).

</td></tr><tr><td>

![Check box.](../../vulnerability-response/image/checkbox.png)

</td><td>

As a user with the ServiceNow AI Platform security incident analyst role, submit additional requests for Malware scans and List threat events. For more information, see [Trigger McAfee ePO profile manually from a security incident](mcafee-epo-submit-ih-fm-si.md)In the ServiceNow AI Platform, as a user with an approval role, or, as a member of an approval group, approve requests for isolate host isolation and remove isolation.

For more information on processing approval requests, see [Create an approval group](create-approval-group-mcafee.md).

</td></tr></tbody>
</table>    You have successfully completed the set up steps, installed and configured the application, and verified expected results for the integration.


**Parent Topic:**[McAfee ePO integration](../concept/mcaffee-epo-overview-arch.md)

**Previous topic:**[Integration architecture for McAfee ePO](../concept/mcafee-epo-integration-architecture.md)

**Next topic:**[Set up your ServiceNow AI Platform instance for the McAfee ePO integration](../reference/mcaffee-epo-setup-now.md)

