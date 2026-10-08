---
title: User criteria for Care Team Mobile
description: Care Team Operations applications include user criteria records, one for each support role, that you can apply to Field Service Management Mobile quick-action icons to control which icons each role sees.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/healthcare-life-sciences/cto-mobile-user-criteria.html
release: brazil
topic_type: reference
last_updated: "2026-09-24"
reading_time_minutes: 1
breadcrumb: [Configure Care Team Mobile, Care Team Mobile, Healthcare Operations, Healthcare and Life Sciences]
---

# User criteria for Care Team Mobile

Care Team Operations applications include user criteria records, one for each support role, that you can apply to Field Service Management Mobile quick-action icons to control which icons each role sees.

The Field Service Management Mobile home screen includes the following quick-action icons: My Group Tasks, Closed Tasks, My Schedule, My Task Map, Draft Task, and Asset Lookup. Icon visibility is controlled by user criteria. Select or combine the records below instead of creating your own.

**Note:** User criteria on an icon only grant visibility. They can't hide an icon from a user who already qualifies through another record or role.

User criteria control icon visibility only. Access to Care Team Mobile itself still requires the sn\_hco.care\_team\_member role. For more information, see [Assign roles for Care Team Mobile users](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/healthcare-life-sciences/cto-mobile-assign-roles.md).

|User criteria|Role|Installed with|Use for|
|-------------|----|--------------|-------|
|Biomed Support Agent|sn\_cto\_biomed.loc\_support\_agent|Care Team Operations for Biomed|Biomed support agents.|
|EVS Support Agent|sn\_cto\_evs.loc\_support\_agent|Care Team Operations for Environmental Services|Environmental Services support agents.|
|Facilities Support Agent|sn\_cto\_facilities.loc\_support\_agent|Care Team Operations for Facilities|Facilities support agents.|
|HCIT Support Agent|sn\_cto\_hcit.loc\_support\_agent|Care Team Operations for Healthcare IT|Healthcare IT support agents.|
|HCO Location Support Agent|sn\_hco.loc\_support\_agent|Healthcare Operations Core|Support agents in any of the four departments above. The four department roles inherit this role.|
|Care Team Agent|sn\_cto.care\_team\_agent|Care Team Work Management|Care team agents. Use this record for the base quick actions, My Group Tasks and Closed Tasks.|

