---
title: Role assignment alerts for Operational Technology Setup
description: If there are errors during the role assignment process for Operational Technology \(OT\) Setup, an error message appears that describes the cause.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/operational-technology/alerts-ot-setup.html
release: australia
topic_type: reference
last_updated: "2026-08-27"
reading_time_minutes: 1
breadcrumb: [Reference, Operational Technology Setup, Operational Technology]
---

# Role assignment alerts for Operational Technology Setup

If there are errors during the role assignment process for Operational Technology \(OT\) Setup, an error message appears that describes the cause.

|Error cause|Alert|
|-----------|-----|
|Selected group or user already has all the necessary roles.|**Roles already assigned**. The user assigned all the necessary roles.|
|A role assignment failed.|**\[Role name\] roles couldn't be assigned**. Please try again.|
|No user is selected.|**No user selected**. Select at least one user before assigning roles.|
|Role assignment process is stuck due to an unexpected error.|**Something went wrong**. An unexpected error occurred while assigning roles.|
|During OT admin role assignment, an admin role isn't selected.|**Only the Implementation Agent \(sn\_ia\_config.ia\_user\) role is selected**. Please select at least one of the OT Admin roles to get started.|

