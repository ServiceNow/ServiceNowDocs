---
title: Definitions of On-Call Scheduling terms
description: Some terms have specific meaning in the On-Call Scheduling application.
locale: en-US
release: xanadu
product: On-Call Scheduling
classification: on-call-scheduling
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Reference, On-Call Scheduling, IT Service Management]
---

# Definitions of On-Call Scheduling terms

Some terms have specific meaning in the On-Call Scheduling application.

-   **Shift**

    A shift is the time period during which the members of a roster are on-call. You can view the details of any shift from the calendar.

-   **Roster**

    A roster is a set of members that is on call for a shift. Because there is typically a roster for each escalation level \(primary, secondary, tertiary\), there are typically multiple rosters for a shift. The members of any roster are contacted in the order that is defined by the escalation policy.

-   **Roster members \(members\)**

    The members of a roster are the users that have been added to a single roster. Roster members typically have the itil role. During an assigned shift, members must be available to act if notified of an escalation.

    -   Users must be members of the same group.
    -   The shift manager \(rota\_manager role\) might or might not be a roster member.
-   **Rotation**

    Rotation is the process of exchanging the turn of duty of members of a roster.

    Members' From and To dates determine when they are members of the roster.

-   **Schedule**

    A schedule specifies the times that shifts are active. For example, a company that wants coverage of tasks around the clock would use a 24-7 schedule. Companies that provide support around the globe could use a follow the sun schedule to cover time zones across continents.

-   **Escalation**

    Escalations are a series of notifications to roster members for a task. The notifications happen in the order specified by the escalation path for the shift.

-   **Notification**

    On-Call Scheduling sends escalation notifications to members of a shift. Notification methods include email, voice, Slack, SMS, Microsoft Teams, and mobile push.

-   **Holidays and time off**

    Roster members can request time off. Managers can plan for and manage holidays and requests for time off.


**Parent Topic:**[Reference section for On-Call Scheduling](reference-for-on-call-scheduling.md)

**Related topics**  


[On-Call Scheduling](../../on-call-scheduling/concept/c_OnCallScheduling.md)

