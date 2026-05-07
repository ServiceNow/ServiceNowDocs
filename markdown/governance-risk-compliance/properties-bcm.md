---
title: Properties installed with BCM
description: Properties are added with the activation of Business Continuity Management.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [General administration setup for BCM, Configure, Business Continuity Management, Governance, Risk, and Compliance]
---

# Properties installed with BCM

Properties are added with the activation of Business Continuity Management.

<table id="table_lvc_3h5_bcc"><thead><tr><th>

Sr. No

</th><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

1

</td><td>

Default plan template name for generating the PDF for the plan\[sn\_bcp.default\_pdf\_plan\_template\]

</td><td>

-   Scope: GRC: Business Continuity Planning
-   Type: string
-   Default value: Business continuity plan template \(Default\)

</td></tr><tr><td>

2

</td><td>

Interval between two task IDs for a recovery task in Business Continuity Planning \(BCP\)\[sn\_bcp.taskIdOffset\]

</td><td>

-   Scope: GRC: Business Continuity Planning
-   Type: numerical value
-   Default value: 1

</td></tr><tr><td>

3

</td><td>

Option to control client-script's strict mode that disables direct DOM access. This property is used to override it for the Business Impact Analysis \(BIA\).\[sn\_bia.glide.script.block.client.globals\]

</td><td>

-   Scope GRC: Business Impact Analysis
-   Type: Yes or No

</td></tr><tr><td>

4

</td><td>

Logging level for BCM applications\[sn\_bcm.logging.verbosity\]

</td><td>

-   Scope: GRC: Business Continuity Management - Core
-   Type: choice list \(Debug, Info, Warn, Error\)
-   Default value: Warn

</td></tr><tr><td>

5

</td><td>

Default increment value for the order column on plan documentation\[sn\_bcp.document\_order\_increment\]

</td><td>

-   Scope: GRC: Business Continuity Planning
-   Type: numerical value
-   Default value: 100

</td></tr><tr><td>

6

</td><td>

Maximum time \(by hours\) allowed to update dependencies in events/exercises \[sn\_recovery.max\_dependency\_update\_processing\_time\]

</td><td>

-   Scope: GRC: Crisis Map
-   Type: numerical value
-   Default value: 3

</td></tr><tr><td>

7

</td><td>

Maximum number of records to show in a group in Asset dependencies RL in Plan \[sn\_bcp.asset\_dependencies\_max\_records\_in\_group\]

</td><td>

-   Scope: GRC: Business Continuity Planning
-   Type: numerical value
-   Default value:20

</td></tr><tr><td>

8

</td><td>

Enable/Disable use of google map's "Places" API\[sn\_bcm\_map.use\_google\_places\_lib\]

</td><td>

-   Scope: GRC: Crisis Map
-   Type: true or false
-   Default value: false

 **Note:** Prior to enabling the Crisis Map feature, verify that you have purchased and set up the Google Maps API.

</td></tr><tr><td>

9

</td><td>

Maximum time \(by hours\) allowed to update dependencies\[sn\_bcm.max\_dependency\_update\_processing\_time\]

</td><td>

-   Scope: GRC: Business Continuity Management - Core
-   Type: numerical value
-   Default value: 24

</td></tr><tr><td>

10

</td><td>

Max relationships for each level\[sn\_bia.cmdb\_max\_relationships\_per\_level\]

</td><td>

-   Scope GRC: Business Impact Analysis
-   Type: numerical value
-   Default value: 5000

</td></tr><tr><td>

11

</td><td>

Event task count limit for asynchronous order calculation in business rule\[sn\_recovery.sync\_task\_order\_calculation\_limit\]

</td><td>

-   Scope: GRC: Crisis Map
-   Type: Integer
-   Default value: 500

</td></tr><tr><td>

12

</td><td>

Maximum number of element definitions to show in UI\[sn\_bcm.element\_definitions\_limit\]

</td><td>

-   Scope: GRC: Business Continuity Management - Core
-   Type: numerical value
-   Default value: 20

</td></tr><tr><td>

13

</td><td>

Default limit for Category impact assessment question responses\[sn\_bcm.config.category\_impact.response\_limit\]

</td><td>

-   Scope GRC: Business Impact Analysis
-   Default value: 10

</td></tr><tr><td>

14

</td><td>

Maximum levels of activated plan to be created in an event\[sn\_recovery.max\_activated\_plan\_levels\]

</td><td>

-   Scope: GRC: Business Continuity Management - Core
-   Type: Integer
-   Default value: 10

</td></tr><tr><td>

15

</td><td>

Mark the Impact Assessment as Complete once all required questions are answered, or all questions \(required and optional\) are answered.\[sn\_bia.determine\_impact\_assessment\_status\]

</td><td>

-   Scope GRC: Business Impact Analysis
-   Type: Required questions or All questions
-   Default value: Required questions

</td></tr><tr><td>

16

</td><td>

Recovery task count limit for synchronous order calculation in business rule\[sn\_bcp.sync\_task\_order\_calculation\_task\_limit\]

</td><td>

-   Scope: GRC: Business Continuity Planning
-   Type: Integer
-   Default value: 500

</td></tr><tr><td>

17

</td><td>

Tables referenced by the system to fetch child records when analyzing CMDB asset dependencies, even if they are not part of the element definition.\[sn\_bcm.read\_cmdb\_tables = cmdb\_ci\_datacenter\]

</td><td>

-   GRC: Business Continuity Management - Core
-   Type: String
-   Default value: None

</td></tr><tr><td>

18

</td><td>

Default limit for IRM GlideRecord getter. \[sn\_irm\_shared\_cmn.config.get\_gliderecord\_limit\]

</td><td>

-   Scope: GRC: Risk Shared Common Components
-   Type: Integer
-   Default value: 1000

</td></tr></tbody>
</table>**Parent Topic:**[General administration setup for BCM](../concept/set-up-bcm-bcmadmin-tasks.md)

