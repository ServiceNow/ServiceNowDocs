---
title: Tables installed with Operational Resilience
description: Several types of tables are installed with the Operational Resilience application.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Reference, Operational Resilience, Governance, Risk, and Compliance]
---

# Tables installed with Operational Resilience

Several types of tables are installed with the Operational Resilience application.

## Tables installed with Operational Resilience

|Table name|Description|
|----------|-----------|
|Activity log \[sn\_oper\_res\_activity\_log\]|Activity log for the application.|
|ASMT rating scale \[sn\_oper\_res\_asmt\_rating\_scale\]|ASMT rating scale.|
|BCM plan \[sn\_oper\_res\_bcm\_plan\]|BCM plan.|
|Choice \[sn\_grc\_choice\]|List of all GRC choices.|
|Change request \[sn\_oper\_res\_change\_request\]|Change request created for the application.|
|Critical service outage \[sn\_oper\_res\_critical\_service\_outage\]|Outage of the critical service.|
|Event \[sn\_oper\_res\_event\]|Event recorded for the application.|
|Failed control \[sn\_oper\_res\_failed\_control\]|Failed control.|
|GRC Profile \[sn\_grc\_profile\]|List of all GRC entities.|
|Importance impact tolerance assessment \[sn\_oper\_res\_importance\_impact\_tolerance\_assessment\]|Importance of the impact tolerance assessment.|
|Incident \[sn\_oper\_res\_incident\]|Incident registered due to an event.|
|Issue \[sn\_oper\_res\_issue\]|Issue logged due to an event.|
|M2M analysis participant \[sn\_oper\_res\_m2m\_analysis\_participant\]|Association between analysis and participant.|
|M2M analysis scenario event \[sn\_oper\_res\_m2m\_analysis\_scenario\_event\]|Association between analysis and scenario event.|
|M2M scenario analysis service \[sn\_oper\_res\_scenario\_analysis\_service\]|Association between scenario and analysis service.|
|M2M scenario event \[sn\_oper\_res\_m2m\_scenario\_event\]|Association between scenario and event.|
|M2M service importance impact tolerance assessment \[sn\_oper\_res\_m2m\_service\_importance\_impact\_tolerance\_assessment\]|Association between service and importance of the impact tolerance assessment.|
|Operational Resilience profile \[sn\_oper\_res\_profile\]|Operational Resilience entity.|
|Profile type \[sn\_grc\_profile\_type\]|List of all GRC entity types.|
|Risk \[sn\_oper\_res\_risk\]|Risk defined in the application. Starting with the Xanadu release \(Release 19.0.4\), the Advanced Risk Assessment \(ARA\) integration with Operational Resilience uses the **Status** field. When an entity is shared between Operational Resilience and Advanced Risk Assessment \(ARA\), and the ARA has the highest risk rating with a status of **Completed**, a record is created for the ARA integration and stored in the \[sn\_oper\_res\_risk\] table.|
|Scenario \[sn\_oper\_res\_scenario\]|Scenario defined in the application.|
|Scenario analysis \[sn\_oper\_res\_scenario analysis\]|Scenario analysis defined in the application.|
|Service impact analysis \[sn\_oper\_res\_service\_impact\_analysis\]|Service impact analysis defined in the application.|
|Service process pillar \[sn\_oper\_res\_service\_process\_pillar\]|Service process pillar defined in the application.|
|Task \[sn\_oper\_res\_task\]|Task defined in the application.|
|Vulnerability profile \[sn\_oper\_res\_vul\_profile\]|Vulnerability profile defined in the application.|
|Services with operational vulnerabilities \[sn\_oper\_res\_vulnerability\_profile\]|Services with operational vulnerabilities.|
|M2M scenario event participant \[sn\_opres\_res\_m2m\_scenario\_event\_participant\]|Each participant can be associated with one or more scenario events. This table stores many-to-many relationships between the participant and scenario events.|
|M2M scenario event issue \[sn\_oper\_res\_m2m\_scenario\_event\_issue\]|Stores many-to-many relationships between the issues and scenario events.|
|Service related information \[sn\_oper\_res\_service\_related\_info\]|Service related information defined in the application.|
|Service Summary \[sn\_oper\_res\_service\_summary\]|Service summary defined in the application.|
|Service tasks \[sn\_oper\_res\_resp\_task\]|Service tasks defined in the application.|
|Response tasks \[sn\_oper\_res\_response\_task\]|Response tasks that are defined in the application.|

## Tables installed with Digital resilience incident reporting

|Table name|Description|
|----------|-----------|
|Action task \[sn\_grc\_case\_mgmt\_case\_task\]|Action tasks associated with the case.|
|Digital Resilience Incident \[sn\_grc\_inc\_rptg\_case\_task\]|Incident reporting case task.|
|Impacted area \[sn\_grc\_case\_mgmt\_impacted\_area\]|Impacted area for the case.|
|Related area \[sn\_grc\_case\_mgmt\_related\_area\]|Related area for the case.|

## Database views

|Table view name|Database view label|Plural|
|---------------|-------------------|------|
|sn\_oper\_res\_risk\_dependency|Services with high risk|Services with high risks|
|Services with high risk|Vulnerable entity|Vulnerable entities|
|sn\_oper\_res\_failed\_control\_dependency|Services with failed control|Services with failed controls|
|sn\_oper\_res\_service\_outage|Service Outage|Service Outage|

