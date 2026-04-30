---
title: Scope-to-target settings
description: Allow or deny access of all application resources in a source scope to a specific application resource \(business rule, table, script include, or event\) in a target scope.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Set the application scope, application resource, and event access, Restricted caller access privilege settings, Application access settings, Contextual development environment, Learning about developing on the ServiceNow AI Platform, Building applications]
---

# Scope-to-target settings

Allow or deny access of all application resources in a source scope to a specific application resource \(business rule, table, script include, or event\) in a target scope.

This setting combination is a many-to-one relationship. For example, you can specify that all application resources in source Scope A can access a script include in target Scope B. ![Restricted caller access scope to target setting](../image/Rcap-scope-to-target.png)

Enter the following field settings for Scope-to-Target restricted caller access.

|Field|Entries|
|-----|-------|
|Source Scope|Scope of the calling application that contains the source application resources.|
|Source Type|Type of record calling the application resource. Select **Scope** to include all application resources in the source scope.|
|Status|Status of the access request. Select **Allowed** to allow access, or select **Denied** to restrict access for this source-target resource relationship.|
|Target Scope|Scope of the requested resource that contains the target application resources that the source application resource requests access to.|
|Target Type|Type of requested resource. Select the specific application resource \(for example, business rule, script include, UI page, event\) the source application resource requests access to.|
|Operation|Type of operation \(for example, Read, Write\) in the target application resource the source application resource requests access to.|

**Parent Topic:**[Set the application scope, application resource, and event access](../task/scope-resource-access.md)

