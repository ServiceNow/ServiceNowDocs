---
title: Configuring a phone PIN
description: You can set up or reset a phone PIN that can be used for caller authentication during a call with an agent.Reset the phone PIN for a caller if the caller's account is locked.Set up or reset your phone PIN that can be used for caller authentication when you call an agent.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Setting up ServiceNow Voice, ServiceNow Voice, Manage people and work capabilities, Extend ServiceNow AI Platform capabilities]
---

# Configuring a phone PIN

You can set up or reset a phone PIN that can be used for caller authentication during a call with an agent.

If the **Require authentication** field is set to **true** for an operation handler, the corresponding operation is invoked only after the caller enters the PIN.

**Important:** It is applicable for both ServiceNow Voice for ITSM and ServiceNow Voice for CSM applications.

**Parent Topic:**[Setting up ServiceNow Voice](ccc-setup.md)

## Reset the phone PIN for a caller

Reset the phone PIN for a caller if the caller's account is locked.

### Before you begin

Role required: sn\_cti\_core.user\_manager

### About this task

### Procedure

1.  Navigate to **All** &gt; **ServiceNow Voice - Core** &gt; **User Pin Reset**.

2.  For the required CTI user, Click the preview icon and open the record to reset the PIN.

    1.  In the **PIN** field, enter the new PIN.

    2.  Clear the **Disabled** check box.

    3.  Click **Update**.


## Set or reset the phone PIN

Set up or reset your phone PIN that can be used for caller authentication when you call an agent.

### Before you begin

Role required: none

### Procedure

1.  Navigate to **All** &gt; **ServiceNow Voice - Core** &gt; **My Phone PIN**.

2.  On the Request Phone PIN form, enter the PIN and re-enter it.

3.  Click **Submit**.


