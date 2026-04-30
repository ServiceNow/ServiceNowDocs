---
title: Scope-to-scope settings
description: Allow or deny access of all application resources in a source scope to all application resources in a target scope. This setting combination is a many-to-many relationship.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Set the application scope, application resource, and event access, Restricted caller access privilege settings, Application access settings, Contextual development environment, Learning about developing on the ServiceNow AI Platform, Building applications]
---

# Scope-to-scope settings

Allow or deny access of all application resources in a source scope to all application resources in a target scope. This setting combination is a many-to-many relationship.

![Restricted caller access scope to scope setting](../image/scope-to-scope.png)

Enter the following field settings for Scope-to-Scope restricted caller access.

|Field|Entries|
|-----|-------|
|Source Scope|Scope of the calling application that contains the source application resources.|
|Source Type|Type of record calling the application resource. To allow access from an entire application, select **Scope**.|
|Status|Status of the access request. Select **Allowed** to allow access, or select **Denied** to restrict access for this source-target resource relationship.|
|Target Scope|Scope of the requested resource that contains the target application resources that the source application resource requests access to.|
|Target Type|Type of requested resource. Select **Scope** to include all application resources in the target scope.|

**Parent Topic:**[Set the application scope, application resource, and event access](../task/scope-resource-access.md)

