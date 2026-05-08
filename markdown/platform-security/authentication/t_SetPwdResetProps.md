---
title: Configure Password Reset properties
description: You can specify properties that configure the Password Reset experience for end users.
locale: en-US
release: australia
product: Authentication
classification: authentication
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Password Reset, Local authentication, Authentication, Access Management]
---

# Configure Password Reset properties

You can specify properties that configure the Password Reset experience for end users.

## Before you begin

Role required: password\_reset\_admin

## About this task

While there are no range limits for the values you can enter for properties, consider using only positive integer values starting at 1. When you determine the limit for the upper range of a property, consider the task that the user is performing.

For example, you would not want to allow 100 attempts for users to verify their identity. A more common value is 3 attempts. Similarly, you may not want to force users who are completing the enrollment process to spend time selecting and answering 30 security questions. The more commonly used number of security questions is between 5 and 7.

## Procedure

1.  Navigate to **All** &gt; **Password Reset** &gt; **Properties**.

    For information about the Password Reset properties, see Password Reset global properties.

2.  Update settings as needed and then click **Save**.


