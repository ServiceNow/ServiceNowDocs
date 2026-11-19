---
title: Trigger additional actions in McAfee ePO integration
description: The List Threat Events and Initiate Malware Scan capabilities can be triggered from Run Additional Actions.​
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/security-management/security-incident-response/configure-additional-actions-mcafee.html
release: zurich
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [McAfee ePO integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Trigger additional actions in McAfee ePO integration

The List Threat Events and Initiate Malware Scan capabilities can be triggered from Run Additional Actions.​

## Before you begin

Role required: sn\_si.admin

## About this task

You can configure and trigger additional actions in the McAfee ePO integration enables by using **Run Additional Actions on Endpoint**, which include the McAfee ePO List Threat Events and McAfee ePO Initiate Malware Scan capabilities.

## Procedure

1.  Navigate to **Security Incidents** &gt; **Show All Incidents**.

2.  Select the security incident on which you want to run the additional actions.

3.  In the Related Links section, select **Run Additional Action\(s\) on Endpoint**.

4.  Browse and select the capability implementation that you want to trigger from the list of additional actions.

    For example, McAfee ePO List Threat Events.

5.  Select **Include Related CI** to run this additional action on all the related CIs of the profile.

    For example, if there are five CIs associated with the security incident, then the selected profile runs on all the five CIs.

6.  Select **Run Additional Actions**.

7.  View and validate the McAfee ePO Threat Event Details on the related lists.


**Parent Topic:**[McAfee ePO integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/security-incident-response/mcaffee-epo-overview-arch.md)

**Previous topic:**[Trigger McAfee ePO profile manually from a security incident](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/security-incident-response/mcafee-epo-submit-ih-fm-si.md)

**Next topic:**[Using McAfee ePO integration in Analyst Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/security-incident-response/using-mcafee-integration-aws.md)

