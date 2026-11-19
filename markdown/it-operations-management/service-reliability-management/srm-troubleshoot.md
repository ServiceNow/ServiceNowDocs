---
title: Troubleshoot SRM
description: Find answers to issues that you may encounter when using Service Reliability Management \(SRM\).
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/service-reliability-management/srm-troubleshoot.html
release: zurich
product: Service Reliability Management
classification: service-reliability-management
topic_type: topic
last_updated: "2022-08-11"
reading_time_minutes: 1
breadcrumb: [Service Reliability Management reference, Service Reliability Management, ITOM AIOps, IT Operations Management]
---

# Troubleshoot SRM

Find answers to issues that you may encounter when using Service Reliability Management \(SRM\).

## Condition

When trying to remove a service from SRM, you see one of the following messages:

-   `<service-name> couldn't be removed from SRM. Check your permissions. Only SRM team managers can remove their team's services.`
-   `<x> services couldn't be removed from SRM. Check your permissions. Only SRM team managers can remove their team's services.`

## Cause

You're not assigned the required role to remove the selected services. As an SRM manager, you can only remove services that belong to your teams. You can still view and filter services across teams, but you can't remove services owned by another team.

## Remedy

To remove the service from SRM, follow these steps to identify the manager to contact:

1.  Navigate to **Workspaces** &gt; **Service Operations Workspace** &gt; **Services**.
2.  Select the filter icon \(\[Omitted image "filter-icon-alerts.png"\] Alt text: Filter icon\) and remove the existing filters, letting you view services not assigned to your teams.
3.  Find and select the service you want to remove.
4.  Select the **Details** tab and then select the information icon \(\[Omitted image "info.png"\] Alt text: Information icon\) in the Support group field.

The manager's name appears below the team name. Contact the manager to request the removal of the service from SRM.

**Parent Topic:**[Service Reliability Management reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/service-reliability-management/service-reliability-management-reference.md)

