---
title: Additional roles for SOW admin
description: You can add various user roles to Service Operations Workspace \(SOW\) Admin role to perform SOW configurations.
locale: en-US
release: australia
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Service Operations Workspace for ITSM reference, Service Operations Workspace for ITSM, IT Service Management]
---

# Additional roles for SOW admin

You can add various user roles to Service Operations Workspace \(SOW\) Admin role to perform SOW configurations.

<table id="table_qkn_j4g_1cc"><thead><tr><th>

Role

</th><th>

Description

</th><th>

Inherited roles

</th></tr></thead><tbody><tr><td>

sn\_admin\_center.read\_only

</td><td>

Provides configuration access to the adoption blueprint section of the Overview and Learning page in SOW Admin Center.

</td><td>

None

</td></tr><tr><td>

script\_include\_admin

</td><td>

Provides configuration access to the following sections of the Landing Page in SOW Admin Center:-   Greetings
-   Tier1 - Upcoming tasks
-   Tier2 - Upcoming tasks

</td><td>

teamdev\_code\_reviewer

</td></tr><tr><td>

ui\_builder\_admin

</td><td>

Provides configuration access to the following pages in SOW Admin Center:-   List configurations - Collapsed lists section in the landing page
-   UX App Route section in the Contextual side panel configurations page
-   Set display count to improve list loading section in the SOW Properties page
-   Overview - tab visibility for tier 1 agents - Toggle button in the Incident record page
-   Overview tab section in the Problem record page
-   Overview tab section in the Change record page

</td><td>

 

</td></tr><tr><td>

personalize

</td><td>

Provides configuration access to following sections of the incident record page in SOW Admin Center:-   Overview - Summary
-   Overview - Impact
-   Overview - Cause
-   Overview - Resolution
-   Details - Record
-   Details - New Record

</td><td>

 

</td></tr><tr><td>

form\_admin

</td><td>

Provides configuration access to following pages in SOW Admin Center:-   Overview - Summary section in the Incident record page
-   Overview - Impact section in the Incident record page
-   Overview - Cause section in the Incident record page
-   Overview - Resolution section in the Incident record page
-   List configurations - List view configurations in the Landing page

</td><td>

 

</td></tr><tr><td>

personalize\_form

</td><td>

Provides configuration access to the following pages in SOW Admin Center:-   Section fields in the Problem record page
-   Details tab in the Problem record page
-   Details tab in the Problem task record page
-   Section fields in the Change record page
-   Details tab in the Change record page
-   Details tab in the Change task record page
-   List configurations - List view configurations in the Landing page

</td><td>

 

</td></tr><tr><td>

dashboard\_admin

</td><td>

Provides configuration access to the following sections of the Landing page in the SOW Admin Center:-   Tier1 - Donut configurations
-   Tier2 - Donut configurations

</td><td>

 

</td></tr><tr><td>

evam\_admin

</td><td>

Provides configuration access to the following sections of the Landing page in the SOW Admin Center:-   Tier1 - Announcements
-   Tier2 - Announcements

</td><td>

 

</td></tr><tr><td>

user\_criteria\_admin or user\_admin

</td><td>

Provides configuration access to the Overview - tab visibility for tier 1 agents - Configure button section of the Incident record page in SOW Admin Center.

</td><td>

 

</td></tr><tr><td>

sn\_templated\_snip.template\_snippet\_writer

</td><td>

Provides configuration access to the Response templates section of the Incident record page in SOW Admin Center.

</td><td>

 

</td></tr><tr><td>

Incident Manager \[incident\_manager\]

\(Existing role with added responsibilities\)

</td><td>

-   Manages incident properties and major incident trigger rules.
-   Can create and edit Communication Plan Definitions.

</td><td>

itil

</td></tr><tr><td>

problem\_manager

</td><td>

Responsible for the overall Problem Management process and can configure Problem Management settings in the SOW Admin Center. Also, act as a problem coordinator.

</td><td>

problem\_coordinator

</td></tr><tr><td>

change\_manager

</td><td>

Provides access to configurations related to Change Management in SOW Admin Center.

</td><td>

-   sn\_sttrm\_attribute\_read
-   sn\_sttrm\_condition\_read
-   sn\_chg\_soc.change\_soc\_admin
-   personalize\_decision\_table\_input
-   sn\_sow\_admin.sow\_admin\_center\_user
-   itil

</td></tr></tbody>
</table>**Parent Topic:**[Service Operations Workspace for ITSM reference](../concept/sow-reference.md)

**Related topics**  


[Terminology in Service Operations Workspace for ITSM](../concept/terminology-used-in-sow-for-itsm.md)

[Version compatibility between Service Operations Workspace for ITSM and Service Operations Workspace ITOM](sow-itsm-itom-version.md)

[Service Operations Workspace for ITSM data model](sow-itsm-data-model.md)

[Components installed with Service Operations Workspace ITSM Applications](components-installed-with-sow.md)

