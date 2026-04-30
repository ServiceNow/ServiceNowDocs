---
title: How Notify processes incoming calls
description: Notify processes incoming calls using workflow activities.
locale: en-US
release: xanadu
product: Notify
classification: notify
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Notify voice and SMS capabilities, Explore, Notify, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# How Notify processes incoming calls

Notify processes incoming calls using workflow activities.

Any Notify activity that manages incoming phone calls creates a record on the Notify Workflow Activity \[notify\_wf\_activity\] table. Each notify\_wf\_activity record is associated with a single call. These records store JSON data detailing the actions to send to the telephony provider.

Notify processes incoming calls in the following way:

1.  A person calls a Notify phone number.
2.  Notify launches the incoming call workflow associated with that Notify phone number.
3.  The workflow reaches a Notify activity and invokes the activity onExecute\(\) function.
4.  The activity creates a new notify\_wf\_activity record detailing any actions to take, with a **State** value of execute.
5.  Notify sends the specified actions to the telephony provider.
6.  The notify\_wf\_activity record **State** changes to processed.
7.  The telephony provider sends a response.
8.  Response arguments, such as user input or recording info, are stored as JSON data in the notify\_wf\_activity **response\_args** field.
9.  The notify\_wf\_activity **State** changes to complete.
10. The JSON data from the notify\_wf\_activity record is copied to the **Last action** field in the Notify call record that triggered the workflow.
11. The workflow invokes the onUpdate\(\) function in executing activities.
12. The activity confirms that the associated notify\_wf\_activity record has completed, and changes the activity state to finished.
13. The workflow transitions to the next activity.

**Parent Topic:**[Notify voice and SMS capabilities](notify-voice-SMS-capabilities.md)

