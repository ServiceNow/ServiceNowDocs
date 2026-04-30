---
title: Tables installed with On-Call Scheduling
description: On-Call Scheduling adds the following tables.
locale: en-US
release: zurich
product: On-Call Scheduling
classification: on-call-scheduling
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Components installed with On-call scheduling, Reference, On-Call Scheduling, IT Service Management]
---

# Tables installed with On-Call Scheduling

On-Call Scheduling adds the following tables.

## Tables installed with On-Call Scheduling

**Note:** Tables with prefix "v\_" such as \[v\_alternate\_rotation\] are view-only tables used for generating on-call reports. Do not use these tables to create reports.

|Display name \[Table name\]|Description|
|---------------------------|-----------|
|On-call Member \[cmn\_rota\_member\]|Table of group members that are participating in the on-call schedule and escalations.|
|Roster \[cmn\_rota\_roster\]|Table that holds the members of the shift, the shift interval, and escalation settings.|
|Shift \[cmn\_rota\]|The table that holds the on-call schedule for a shift.|
|Roster Schedule Span \[roster\_schedule\_span\]|Table that contains the schedule span definitions. On-Call Scheduling adds a group reference and the On-call type to the Type field.|
|Trigger Rule \[trigger\_rule\]|Table that extends the Assignment Rule \[sysrule\_assignment\] table and stores when the escalation process is triggered and what actions to take.|
|On-call Notifications \[v\_on\_call\]|Table that lists the reminder notifications that were sent.|
|Rotation Schedule \[v\_rotation\]|Table that lists shift schedules by start date and time and includes user contact information, if available.|
|User Rotation Schedule \[v\_user\_rotation\]|Table that lists the shift schedule by user.|
|Alternate Rotation Schedule \[v\_alternate\_rotation\]|Table that lists the alternate user schedules by shift and roster and the start and end date and time stamps.|
|Rotation Escalation \[cmn\_rota\_escalation\]|Table that lists the escalations including the event and last updated time stamp.|
|Shift Contact Preference \[cmn\_rota\_contact\_preference\]|Table that holds the contact preferences for default and custom escalations.|
|On-Call Communication Type \[on\_call\_communication\_type\]|Table that lists the type of communication channel used.|
|On-Call Group Template \[sys\_on\_call\_group\_template\]|Table with information about the template used to create/edit a schedule of a group.|
|On-Call Shift Template \[sys\_on\_call\_shift\_template\]|Table with information about the template used to create/edit a schedule of a shift.|
|On-Call User Preference \[on\_call\_user\_preference\]|Table with information on a member's preferences.|
|On-Call User Contact Preference \[on\_call\_user\_contact\_preference\]|Table with information on a member's contact preferences.|
|\[sys\_on\_call\_contact\_source\]|Table that lists the contact sources and devices|
|On-Call Escalation \[on\_call\_escalation\]|Table that records the source, group, and related details for escalation tracking.|
|On-Call Escalation Level \[on\_call\_escalation\_level\]|Table that logs the escalation levels reached for an escalation and related details for escalation tracking.|
|On-Call Escalation Contact Attempt \[on\_call\_escalation\_con\_attempt\]|Table that logs contact attempts at an escalation level and related details for escalation tracking.|
|On-Call Escalation Notification \[on\_call\_escalation\_comm\]|Table that logs both the notifications and the responses for a contact attempt and related details for escalation tracking.|
|On-Call Escalation Response \[on\_call\_escalation\_response\]|Table that tracks On-Call escalation responses by On-Call workflows. Once consumed, entries are deleted by the system.|
|Trigger Rule Table Configuration \[trigger\_rule\_table\_cfg\]|Table that lists the tables that are enabled for creating escalation trigger rules. The table is used to enable the escalation trigger rules for the tables that do not extend tasks.|
|On-Call Add Member \[on\_call\_add\_member\]|Table that records the member details for adding a member to the roster.|
|On-Call Remove Member \[on\_call\_remove\_member\]|Table that records the member details for removing a member from the roster.|
|On-Call Move Member \[on\_call\_swap\_member\]|Table that records the member details for swapping the order of a member with the target member or moving the order of a member after the target member in the roster.|

**Parent Topic:**[Components installed with On-call scheduling](../../user-administration/concept/components-installed-with-on-call-scheduling.md)

