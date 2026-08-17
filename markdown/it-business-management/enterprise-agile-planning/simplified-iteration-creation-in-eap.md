---
title: Creating iterations for teams in EAP
description: Create Planning Intervals \(PIs\) and Sprints directly from the Backlog by entering start and end dates, without setting up planning calendar entries first.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-business-management/enterprise-agile-planning/simplified-iteration-creation-in-eap.html
release: australia
product: Enterprise Agile Planning
classification: enterprise-agile-planning
topic_type: concept
last_updated: "2026-07-24"
reading_time_minutes: 9
breadcrumb: [Manage team backlog, Use, Enterprise Agile Planning, Strategic Planning, Strategic Portfolio Management]
---

# Creating iterations for teams in EAP

Create Planning Intervals \(PIs\) and Sprints directly from the Backlog by entering start and end dates, without setting up planning calendar entries first.

## PI, sprint, and iteration planning

Iteration planning in EAP lets scrum masters and team members plan their own cadence without depending on centralized setup or ongoing coordination with EAP admins.

-   Teams can start planning as soon as their EAP configuration is active. There's no need to wait for an admin to define planning calendars before iterations can be created.
-   A single Backlog action creates a Planning Interval and its child Sprints together, so a scrum master can plan an ART's cadence in one place.
-   Teams that share an ART share one timeline. When a team joins an ART later, its Sprints are aligned to the ART automatically. When you change an iteration date, aligned iterations on sibling teams update with it. Timeline coordination isn't a separate manual step.

## Creating iterations from the Backlog

From EAP version 4.17.0, create a Planning Interval or Sprint directly from the team's Backlog by entering the start and end dates on the modal. The underlying planning calendar entries are created for you, so nobody has to define calendar entries before teams can plan. For the steps, see [Create a Planning Interval or Sprint from EAP Backlog](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/enterprise-agile-planning/create-pi-sprint-eap-backlog.md).

If you upgraded from an earlier version, the planning calendar entries that your admin defined remain valid. Existing iterations keep their dates, and teams can continue to create iterations within the timelines that those entries define. When an entry already matches the team, the dates on the modal are read-only and the system uses the dates from that entry.

Define calendar entries in advance only if you have a specific requirement to manage iteration timelines from a central place. For more information, see [Create calendar entries for iterations in EAP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/enterprise-agile-planning/create-calendar-entries-in-eap.md).

## User roles to create and update iterations

The role that a user has and whether a timeline already exists for the team together determine who can create an iteration.

-   `sn_apw_advanced.eap_scrum_master`: Creates the first iteration for a set of teams that share a planning calendar. This role can also create, edit, and delete planning calendars and calendar spans, and it's the only role that can change the start date or end date of an iteration. The role is intended for team leads who plan iteration timelines without needing full EAP admin access.
-   `sn_apw_advanced.eap_user`: Creates iterations that follow a timeline which already exists, alongside their other Backlog activities. Users with this role can't change iteration dates.

Because many teams can share one planning calendar, an EAP scrum master creates the first iteration for one of the ARTs in a configuration. After that timeline exists, an EAP user can create the following Planning Intervals and Sprints for the other ARTs and teams that share the same calendar. If no timeline exists yet, the iteration isn't created and a message asks the user to contact their scrum master.

These roles are contained within one another. The EAP admin role contains the EAP scrum master role, which contains the EAP user role, which contains the EAP read-only role. A user with a containing role also gets the access of the roles within it. For details on the roles installed with Enterprise Agile Planning, see [Components installed with Enterprise Agile Planning](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/enterprise-agile-planning/components-installed-with-enterprise-agile-planning.md).

## Calendar sharing across teams

Planning calendars in EAP are set for each team level in the configuration. In the default configurations, the ART and Agile Team levels have a planning calendar. The levels above the ART, such as Portfolio and Solution Train, have no planning calendar, so they group teams organizationally and don't carry their own iteration timeline.

All Agile Teams in one ART share that ART's timeline. When you create a Planning Interval for an ART and add child Sprints, the Sprints apply to every Agile Team in that ART. If an Agile Team is added to the ART later, the in-progress Sprint and the upcoming Sprints are created for that team automatically, to match the Sprints on its sibling teams. Sprints that already ended aren't copied, and no Sprints are created if the sibling teams don't have any.

By default, the ARTs in one EAP configuration also share their planning calendars. When the first ART creates a Planning Interval, its dates are recorded on the shared calendar. The other ARTs each still create their own Planning Interval from their own Backlog, but the date fields are read-only and use the dates that are already set. A message on the modal states that the calendar is shared with a team that has already created iterations. In this way, every ART in the configuration follows one cadence.

To keep the ARTs in a configuration independent of each other, your admin selects **Have unique calendars** on the EAP configuration. Each ART that's added after this option is selected gets its own planning calendar, together with a matching calendar for each of its child levels. Creating a Planning Interval for one of those ARTs doesn't affect the others. Select this option before you add your teams, because it can't be cleared afterward and it doesn't change the calendars or the iterations that already exist. For more information, see [Create or update a configuration in EAP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/enterprise-agile-planning/create-eap-configuration.md).

When you edit the start date or end date of an iteration, the change updates the underlying calendar entry. The change cascades to the iterations on all other teams that share that entry, which keeps iteration dates consistent across teams that plan together. For details on editing dates, see [Update iteration details in EAP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/enterprise-agile-planning/edit-pi-sprint-iteration-details-in-eap.md).

## Example: Full Configuration

The Full Configuration uses the hierarchy of **Portfolio &gt; Solution Train &gt; ART &gt; Agile Team**. Consider a Digital Banking portfolio that contains a Payments Platform Solution Train, which contains a Payment Analytics ART. The Payment Analytics ART has two Agile Teams, PAT Team 1 and PAT Team 2.

-   The EAP scrum master creates a Planning Interval named **Q1 2027** for Payment Analytics ART with a start date of 2027-01-01, end date of 2027-03-31, and six child Sprints of two weeks each. PAT Team 1 and PAT Team 2 both get the same six Sprints, aligned to Q1 2027.
-   PAT Team 3 joins Payment Analytics ART on 2027-02-15. Sprints matching the ART's remaining Q1 2027 Sprints are automatically created for PAT Team 3. The team can start scheduling work on Sprint 4 without any additional setup.
-   The scrum master shifts Sprint 4's start date from 2027-02-15 to 2027-02-22. The change updates Sprint 4 on every Agile Team in Payment Analytics ART.

## Example: Large Solution Configuration

The Large Solution Configuration uses the hierarchy **Solution Train &gt; ART &gt; Agile Team**, without a Portfolio tier. Consider a Loans Platform Solution Train that contains two ARTs: Personal Loans ART with PLT Team A and PLT Team B under it, and Business Loans ART with BLT Team X under it.

-   The EAP scrum master creates a Planning Interval named **Q1 2027** for Personal Loans ART with six child Sprints. PLT Team A and PLT Team B both get the same six Sprints. Because both ARTs belong to the same configuration and share its planning calendar, these dates are now set for Business Loans ART as well. When someone creates the Planning Interval for Business Loans ART, the date fields are read-only and use the same dates, and BLT Team X's Sprints align to them.
-   The scrum master extends the Q1 2027 end date by one week. The change cascades to the existing Sprint 6 on PLT Team A, PLT Team B, and BLT Team X, because all three teams follow the same calendar entry.
-   If the admin had selected **Have unique calendars** on this configuration, each ART would follow its own calendar. Personal Loans ART and Business Loans ART would then keep separate Planning Intervals and Sprints, and a date change on one ART wouldn't affect the other.

## Rules that iteration dates must follow

When you create or edit an iteration such as a Planning Interval or Sprint, the system enforces these date rules.

-   Two Planning Intervals on the same ART can't have overlapping dates.
-   Two Sprints under the same parent Planning Interval and the same team can't have overlapping dates.
-   Sprint dates must fit inside an existing Planning Interval. The ART must have a Planning Interval before an Agile Team under it can have Sprints.
-   Adjacent \(back-to-back\) dates are allowed. For example, one Sprint ending on March 14 and another starting on March 15 don't overlap.
-   If you shorten or move a Planning Interval, its existing Sprints must still fall inside the new dates. Otherwise the change isn't saved.
-   Cancelled iterations don't reserve their dates. You can create an iteration with the same dates as a cancelled one.
-   Complete iterations do reserve their dates, so you can't create an iteration that overlaps one. Complete iterations are also left unchanged when iteration dates cascade, which keeps historical dates and metrics intact.

**Parent Topic:**[Manage team backlog in EAP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/enterprise-agile-planning/using-eap.md)

**Related topics**  


[Create a Planning Interval or Sprint from EAP Backlog](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/enterprise-agile-planning/create-pi-sprint-eap-backlog.md)

[Update iteration details in EAP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/enterprise-agile-planning/edit-pi-sprint-iteration-details-in-eap.md)

[Create calendar entries for iterations in EAP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/enterprise-agile-planning/create-calendar-entries-in-eap.md)

[Agile configurations in EAP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/enterprise-agile-planning/agile-configurations-in-eap.md)

[Components installed with Enterprise Agile Planning](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/enterprise-agile-planning/components-installed-with-enterprise-agile-planning.md)

