---
title: Time recording for Customer Service Management
description: Record time worked on cases and case tasks. Time worked entries automatically generate time cards and time sheets for manager approval.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Agent management, Use, Customer Service Management]
---

# Time recording for Customer Service Management

Record time worked on cases and case tasks. Time worked entries automatically generate time cards and time sheets for manager approval.

Customer service agents \(users with the sn\_customerservice\_agent role\) can record time worked on case-related activities, create time cards and time sheets, and submit for approval. Managers can approve time sheets, define cost rates for different types of activities, and convert to expense lines.

The time recording feature extends the functionality of the Time Card Management application to Customer Service Management. Agents can record time worked on cases and tasks directly from the Case or Case Task form and time spent on other activities, such as meetings or training, from the Time Worked form. Time worked entries automatically create time cards for each task and selected work category. Time cards are automatically included in a weekly time sheet.

The time recording feature also extends the functionality of the Cost Management application to Customer Service Management. Customer service managers can create labor rate cards, which define different cost rates for different activities. Time sheets use labor rate cards to determine costs and to generate expense lines.

Agents can modify the hours recorded on time cards. Once a time sheet is approved and a time card is processed, the agent can still go back and modify the time worked. The time sheet reverts to the **Pending** state and new time cards are created. If an agent adds more time worked records to an approved time sheet for the same week, a new time sheet record is created for the current week.

Managers can view time worked records, time cards, and time sheets for agents in their assignment groups, as well as approve and reject time sheets. After a time sheet is approved, the system processes the time cards and uses rate cards based on the time card category to create expense lines.

## Time recording plugin

The time recording feature requires the Customer Service Management plugin \(com.sn\_customerservice\) and the Time Recording for Customer Service plugin \(com.snc.csm\_time\_recording\).

## User roles

The time recording feature adds the following roles.

<table id="table_rwn_rlq_mbb"><thead><tr><th>

Role

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Time card user\[timecard\_user\]

</td><td>

Record time worked on cases and tasks. View, modify, and delete time worked entries on time cards and submit time sheets for approval. Users with the customer service agent \(sn\_customerservice\_agent\) role inherit the timecard\_user role.

This role restricts access to the time sheets, time cards, and time worked records created by the agent.

</td></tr><tr><td>

Time card administrator \[timecard\_admin\]

</td><td>

Review, approve, and reject time sheets for customer service agents. Users with the customer service manager role \(sn\_customerservice\_manager\) inherit the timecard\_admin, timecard\_approver, and timecard\_manager roles.

 This role restricts access to the time sheets, time cards, and time worked records created by the agents in a manager's assigned groups.

</td></tr></tbody>
</table>## System properties

The time recording feature adds the following properties.

<table id="table_o4n_zsq_mbb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

com.snc.time\_card.time\_worked

</td><td>

Enables the time recording feature for Customer Service Management. The default setting is **false**.**Note:** This property has been replaced by the **Auto fill time card with time worked entries** field on the Time Sheet Policy form. When this field is enabled, the user's time card is auto-filled with the information from their time worked entries.

</td></tr><tr><td>

com.snc.time\_card.default\_rate

</td><td>

The default hourly rate used when processing time cards if a rate from a labor rate card is not available.

</td></tr></tbody>
</table>## Time Sheet policy

The time recording feature uses the **Default time sheet policy**.

For users with the sn\_customerservice\_agent role, creating time worked records automatically creates or modifies time cards regardless of the setting for the **com.snc.time\_card.time\_worked** system property. The time sheet policy controls this functionality. The system administrator can disable the auto-creation of time cards for a specific user with the sn\_customerservice\_agent role by creating a separate time sheet policy for that user.

## Labor rate cards

The time recording feature provides one labor rate card: **CSM Rate Card \(Default\)**.

If needed, system administrators can create additional labor rate cards. Navigate to **Cost** &gt; **Costs** &gt; **Labor Rate Cards** and click **New** to create a labor rate card.

