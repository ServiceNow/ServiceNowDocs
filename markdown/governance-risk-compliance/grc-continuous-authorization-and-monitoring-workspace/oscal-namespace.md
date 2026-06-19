---
title: OSCAL custom properties
description: Custom properties with a unique namespace are used to include specific information, capture impact, and tailor OSCAL content for CAM import and export across all supported models.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/grc-continuous-authorization-and-monitoring-workspace/oscal-namespace.html
release: australia
product: GRC: Continuous Authorization and Monitoring Workspace
classification: grc-continuous-authorization-and-monitoring-workspace
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [CAM OSCAL, Continuous authorization and monitoring tasks in the CAM Workspace, Using CAM, Continuous Authorization and Monitoring, Governance, Risk, and Compliance]
---

# OSCAL custom properties

Custom properties with a unique namespace are used to include specific information, capture impact, and tailor OSCAL content for CAM import and export across all supported models.

## Catalog

|Field|Description|
|-----|-----------|
|impact|Captures control objective impact.|
|active|Indicates whether a control objective is active.|
|source|Source of the baseline control objective.|
|configuration|Applies a policy to baseline controls using configurations such as Addition, Subtraction, and Custom Action.|
|order|The order in which you applied the policy.|
|action|Combination of behavior and configuration.|
|behavior|Compares the control objective reference in the policy with those in the baseline controls.|
|auto\_control\_create|Indicates whether controls are automatically created.|
|create\_control\_requirements|Indicates whether control requirements are automatically created.|
|organizational\_guidance|Captures organizational guidance associated with the catalog.|

## System Security Plan \(SSP\)

**General SSP properties**

|Field|Description|
|-----|-----------|
|impact-change-justification|Justification for changing the recommended impact level.|
|justification|Justification for making a baseline control not applicable. Present only when a baseline control is made not applicable.|
|source|Source of the baseline control objective.|
|behavior|Behavior applied when comparing policy control objectives with baseline controls.|
|action|Combination of behavior and configuration.|
|order|The order in which you applied the policy.|
|category|Category of information type.|
|sub\_category|Subcategory of information type.|
|mission-critical|Indicates whether the system is mission-critical.|
|type|System type.|
|classification|System classification level.|
|version|System version.|
|skip-attestations|Indicates whether attestations are skipped.|
|active|Indicates whether the record is active.|
|business-process|Associated business process.|
|is\_fully\_inherited|Indicates whether the control is fully inherited.|
|implementation-status-type|Type of implementation status.|
|state-model|State model associated with the SSP.|
|workflow-version|Version of the associated workflow.|
|workflow-impact|Impact level associated with the workflow.|
|workflow-configuration|Configuration of the associated workflow.|
|package-step|Current step in the authorization package workflow.|

**Privacy Impact Assessment \(PIA\) properties**

|Field|Description|
|-----|-----------|
|pii-in-identifiable-form|Indicates whether the system contains PII in identifiable form.|
|pii-information-about-public|Indicates whether the system contains PII about members of the public.|
|privacy-impact-assessment|Indicates whether a privacy impact assessment is required.|
|system-of-records-notice|Indicates whether a system of records notice applies.|
|privacy-sensitive-system|Indicates whether the system is privacy-sensitive.|

**Metric properties**

|Field|Description|
|-----|-----------|
|percentage-of-controls-implemented|Percentage of controls implemented in the system.|
|number-of-change-requests|Number of change requests associated with the system.|
|number-of-incidents|Number of incidents associated with the system.|
|change-request-average-risk-score|Average risk score across change requests.|
|incident-average-impact|Average impact score across incidents.|
|number-of-vulnerable-items|Number of vulnerable items associated with the system.|
|vulnerable-item-average-risk-score|Average risk score across vulnerable items.|
|number-of-security-incidents|Number of security incidents associated with the system.|
|security-incident-average-risk-score|Average risk score across security incidents.|

**Control Tailoring Request \(CTR\) properties**

|Field|Description|
|-----|-----------|
|uuid|Unique identifier of the Control Tailoring Request.|
|state|Current state of the CTR.|
|request\_reason|Reason for submitting the CTR.|
|opened\_by|User who opened the CTR.|
|assigned\_to|User assigned to the CTR.|
|control\_tailoring\_request\_uuid|UUID of the associated CTR. Present on baseline control overlays and work notes.|
|work\_note|Work note associated with the CTR.|
|additional\_comment|Additional comment associated with the CTR.|

**Baseline control overlay properties**

|Field|Description|
|-----|-----------|
|requested\_allocation|Requested control allocation in the CTR.|
|previous\_allocation|Previous control allocation before the CTR.|
|policy\_name|Name of the policy associated with the overlay.|
|inherited\_from|Source from which the control is inherited.|
|requested\_configuration|Requested configuration in the overlay.|
|previous\_configuration|Previous configuration before the overlay.|
|control\_objective\_reference|Reference to the associated control objective.|

**Approval workflow properties**

|Field|Description|
|-----|-----------|
|approver|User assigned as approver in the workflow.|
|comments|Comments submitted during the approval step.|
|approving|Indicates whether the record is in an approving state.|
|due\_date|Due date for the approval step.|
|expected\_start|Expected start date for the approval step.|
|iteration|Current iteration of the approval workflow.|
|step|Current step in the approval workflow.|
|source\_table|Source table of the record being approved.|
|approval\_for|Record or object for which approval is requested.|

**Control and control requirement properties**

|Field|Description|
|-----|-----------|
|description|Description of the control or control requirement.|
|status|Status of the control or control requirement.|
|content|Content associated with the control.|
|owner|Owner of the control.|
|owning\_group|Group that owns the control.|
|respondents|Respondents assigned to the control or control requirement.|
|implementation\_statement|Implementation statement for the control.|
|frequency|Assessment frequency for the control.|
|weighting|Weighting assigned to the control.|
|sync\_with\_entity\_owner|Indicates whether the control syncs with the entity owner.|
|supplemental\_guidance|Supplemental guidance for the control.|
|attestation|Attestation associated with the control or control requirement.|
|discussion|Discussion notes for the control.|
|requirement\_level\_attestation|Attestation at the requirement level.|
|requirement\_number|Requirement number of the control requirement.|

## Assessment Plan \(AP\)

**Activity properties**

|Field|Description|
|-----|-----------|
|interview|Interview-based assessment activity.|
|test|Test-based assessment activity.|
|examine|Examine-based assessment activity.|
|source|Source of the assessment activity.|
|state|State of the assessment activity.|
|operational-assessment-procedures|Operational assessment procedures associated with the activity.|
|test\_plan\_uuid|UUID of the associated test plan.|
|active|Indicates whether the activity is active.|

**Assessment procedure properties**

|Field|Description|
|-----|-----------|
|assessment\_objective|Assessment objective associated with the procedure.|
|identifier|Identifier of the assessment procedure.|
|uuid|UUID of the assessment procedure.|
|label|Label of the assessment step.|

**Test plan properties**

|Field|Description|
|-----|-----------|
|entity|Entity associated with the test plan.|
|duration|Duration of the test plan.|
|operation\_assessment\_procedures|Operational assessment procedures in the test plan.|
|short\_description|Short description of the test plan.|
|test\_template|Test template used in the test plan.|
|test\_template\_source|Source of the test template.|
|planned\_start\_date|Planned start date of the test plan.|
|planned\_end\_date|Planned end date of the test plan.|

**Engagement metadata properties**

|Field|Description|
|-----|-----------|
|fieldwork\_complete\_percentage|Percentage of fieldwork completed in the engagement.|
|objective|Objective of the engagement.|
|engagement\_starts|Start date of the engagement.|
|engagement\_ends|End date of the engagement.|
|budget\_cost|Budgeted cost of the engagement.|
|planned\_cost|Planned cost of the engagement.|
|planned\_start\_date|Planned start date of the engagement.|
|planned\_end\_date|Planned end date of the engagement.|
|fieldwork\_start\_date|Actual fieldwork start date.|
|fieldwork\_end\_date|Actual fieldwork end date.|
|engagement\_actual\_start|Actual start date of the engagement.|
|engagement\_actual\_end|Actual end date of the engagement.|
|schedule\_start\_date|Scheduled start date.|
|schedule\_end\_date|Scheduled end date.|
|work\_start|Work start date.|
|work\_end|Work end date.|
|description|Description of the engagement.|
|short\_description|Short description of the engagement metadata.|
|state|State of the engagement.|
|active|Indicates whether the engagement is active.|

## Assessment Results \(AR\)

**Metadata properties**

|Field|Description|
|-----|-----------|
|source|Source of the assessment results.|
|actual\_cost|Actual cost of the assessment.|
|report\_template|Report template used for the assessment results.|

**Control test properties**

|Field|Description|
|-----|-----------|
|operation\_effectiveness|Operational effectiveness rating of the control test.|
|operation\_expectations|Expected operational outcomes of the control test.|
|operation\_results|Actual results of the control test.|
|actual\_start\_date|Actual start date of the control test.|
|actual\_end\_date|Actual end date of the control test.|
|planned\_start\_date|Planned start date of the control test.|
|planned\_end\_date|Planned end date of the control test.|
|operation\_assessment\_procedures|Operational assessment procedures for the control test.|
|entity|Entity associated with the control test.|

**Assessment procedure properties**

|Field|Description|
|-----|-----------|
|notes|Notes associated with the assessment procedure.|
|label|Label of the assessment step.|

## Plans of Action and Milestones \(POA&amp;M\)

**General POA&amp;M properties**

|Field|Description|
|-----|-----------|
|source|Source of the POA&amp;M item.|
|state|Current state of the POA&amp;M item.|
|priority|Priority of the POA&amp;M item.|
|response|Response associated with the POA&amp;M item.|
|explanation|Explanation for the POA&amp;M item.|
|issue\_type|Type of issue recorded in the POA&amp;M item.|
|classification|Classification of the POA&amp;M item.|
|issue\_rating|Risk rating of the issue.|
|issue\_source|Source of the issue.|
|planned\_start\_date|Planned start date for remediation.|
|planned\_end\_date|Planned end date for remediation.|
|actual\_start\_date|Actual start date of remediation.|
|actual\_end\_date|Actual end date of remediation.|

**User assignment properties**

|Field|Description|
|-----|-----------|
|assigned\_to|User assigned to the POA&amp;M item.|
|issue\_manager|User managing the issue.|
|issue\_manager\_group|Group managing the issue.|
|watch\_list|Users on the watch list for the POA&amp;M item.|

**Risk acceptance properties**

|Field|Description|
|-----|-----------|
|weakness\_description|Description of the identified weakness.|
|business\_effect|Business effect of the weakness.|
|business\_justification|Business justification for risk acceptance.|
|request\_justification|Justification for the risk acceptance request.|
|request\_overview|Overview of the risk acceptance request.|

**Milestone and acceptance task properties**

|Field|Description|
|-----|-----------|
|work\_note|Work note associated with the milestone or acceptance task.|
|additional\_comment|Additional comment on the milestone or acceptance task.|

**Parent Topic:**[CAM OSCAL](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-continuous-authorization-and-monitoring-workspace/oscal-cam-ws.md)

