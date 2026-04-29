---
title: Email notifications in Digital Product Release
description: List of automated email notifications that are installed with Digital Product Release.
locale: en-US
release: australia
product: Digital Product Release
classification: digital-product-release
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [Email notifications in Digital Product Release, Email notifications in DPR]
breadcrumb: [Reference, Digital Product Release, IT Service Management]
---

# Email notifications in Digital Product Release

List of automated email notifications that are installed with Digital Product Release.

The following table lists automated email notifications that trigger at key events throughout the release lifecycle. These notifications help stakeholders stay informed and take timely action, improving collaboration and release efficiency.

|Name|Description|When to send|Who to send|
|----|-----------|------------|-----------|
|Failed policies for a release phase|Notifies if any of the policies mapped to that phase are non-compliant.|On the phase end date|Release owner|
|Release task 2-days due reminder|Notifies to complete any pending release tasks.|2 days before the release task due date|Assignee of the task|
|Release readiness reminder|Notifies to complete any remaining activities in the release.|1 day before the release readiness date|Release owner|
|Release phase closed|Notifies completion of a release phase.|Phase's state change|Release owner|
|Policies are non-compliant for a release phase|Notifies when policies mapped to a release phase are non-compliant.|Policy executed with non-compliant status|Release owner|
|Release task rejected|Notifies when the release task approval request is rejected.|Task approval request is rejected|Release owner|
|Release task approval request|Notifies to review and approve or reject the release task request.|Task approval request submitted|Approver|

**Parent Topic:**[Digital Product Release reference](../concept/dpr-reference.md)

