---
title: Source-to-scope settings
description: Allow or deny access of a specific application resource in a source scope to all application resources in a target scope.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Set the application scope, application resource, and event access, Restricted caller access privilege settings, Application access settings, Contextual development environment, Learning about developing on the ServiceNow AI Platform, Building applications]
---

# Source-to-scope settings

Allow or deny access of a specific application resource in a source scope to all application resources in a target scope.

This setting combination is a one-to-many relationship. For example, you can specify that a particular business rule in source Scope A can access all application resources in target Scope B.

![Restricted caller access source to scope setting](../image/Rcap-source-to-scope.png)

Enter the following field settings for Source-to-Scope restricted caller access.

|Field|Entries|
|-----|-------|
|Source Scope|Scope of the calling application that contains the source application resource requesting access to the target scope application resource.|
|Source Type|Type of record calling the application resource. Select the specific application resource \(for example, business rule or script include\) requesting access to the specified target scope application resource.|
|Status|Status of the access request. Select **Allowed** to allow access, or select **Denied** to restrict access for this source-target resource relationship.|
|Target Scope|Scope of the requested resource that contains the target application resources that the source application resource requests access to.|
|Target Type|Type of requested resource. Select **Target** to include all application resources in the selected target scope.|
|Operation|Type of operation \(for example, Read, Write\) in the target application resource the source application resource requests access to.|

**Parent Topic:**[Set the application scope, application resource, and event access](../task/scope-resource-access.md)

