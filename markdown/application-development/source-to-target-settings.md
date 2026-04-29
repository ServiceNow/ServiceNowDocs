---
title: Source-to-target settings
description: Allow or deny access of a specific application resource in a source scope to a specific application resource in a target scope.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Set the application scope, application resource, and event access, Restricted caller access privilege settings, Application access settings, Contextual development environment, Learning about developing on the ServiceNow AI Platform, Building applications]
---

# Source-to-target settings

Allow or deny access of a specific application resource in a source scope to a specific application resource in a target scope.

This setting combination is a one-to-one relationship. For example, you can specify that a specific business rule in source Scope A can access a specific application resource, such as a business rule, table, script include or event, in a target scope.

![Restricted caller access source-to-target setting](../image/Rcap-source-to-target.png)

Enter the following field settings for Source-to-Target restricted caller access.

|Field|Entries|
|-----|-------|
|Source Scope|Scope of the calling application that contains the source application resources.|
|Source Type|Type of record calling the application resource. Select the specific application resource \(for example, business rule, script include, or UI page\) requesting access to the specified target scope application resource.|
|Status|Status of the access request. Select **Allowed** to allow access, or select **Denied** to restrict access for this source-target resource relationship.|
|Target Scope|Scope of the requested resource that contains the target application resources that the source application resource requests access to.|
|Target Type|Type of requested resource. Select the specific application resource \(for example, business rule, Script Include, event\) the source application resource requests access to.|

**Parent Topic:**[Set the application scope, application resource, and event access](../task/scope-resource-access.md)

