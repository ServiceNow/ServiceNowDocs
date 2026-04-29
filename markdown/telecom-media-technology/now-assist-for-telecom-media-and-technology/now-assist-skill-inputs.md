---
title: Skill inputs for Now Assist for Telecommunications, Media and Technology \(TMT\)
description: Use inputs for each skill to configure how and when a skill is used.
locale: en-US
release: australia
product: Now Assist for Telecom, Media and Technology
classification: now-assist-for-telecom-media-and-technology
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 9
breadcrumb: [Configure, Now Assist for TMT, Telecommunications, Media, and Technology \(TMT\)]
---

# Skill inputs for Now Assist for Telecommunications, Media and Technology \(TMT\)

Use inputs for each skill to configure how and when a skill is used.

## Overview of Now Assist for TMT

Depending on the selected skill, you can configure inputs. These settings determine how a skill is used. An input identifies the data that is used for a skill, such as the table and fields that are used to generate a service problem case summary, resolution notes summary, customer service summary, and test summary.

Domain separation allows users to separate data, processes, and administrative tasks into logical groupings known as domains. Domain separation enables users to independently manage skill configurations, data visibility, and other settings within each domain. Domain separation is possible at the skill level and at the individual configuration level.

Domain separation is possible at the skill level and at the individual configuration level.

Enable security for Now Assist skills and flows through access control lists \(ACLs\) and user identities. For more information, see [Configure ACLs for AI agents and agentic workflows](https://www.servicenow.com/docs/access?context=aia-security-implementation&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).

To understand more about the ServiceNow domain separation, see [Exploring domain separation](https://www.servicenow.com/docs/access?context=c_DomainSeparation&version=australia&pubname=australia-platform-security&ft:locale=en-US).

## Service Problem Case sentiment analysis skill

The Service Problem Case sentiment analysis skill uses the following table and field inputs to analyze the customer sentiment on a service problem case.

<table id="table_irb_5xd_33c"><thead><tr><th>

Input

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Input table

</td><td>

Service Problem Case \[sn\_sprb\_mgmt.admin\]

</td></tr><tr><td>

Input fields

</td><td>

-   Description
-   Short description
-   State
-   Issue severity
-   Additional comments
-   Work notes

</td></tr></tbody>
</table>## Comprehensive summary of linked records skill

The comprehensive summary of linked records skill uses the following table and field inputs to generate the summary of linked records in an Alternative Dispute Resolution \(ADR\) case.

|Input|Description|
|-----|-----------|
|Input table|ADR Complaint \[sn\_telco\_adr\_mgmt\_complaint\]|
|Input fields|Short description|

## Deadlock letter draft generation skill

The deadlock letter draft generation skill uses the following table and field inputs to generate a deadlock letter for an ADR case.

|Input|Description|
|-----|-----------|
|Input table|ADR Complaint \[sn\_telco\_adr\_mgmt\_complaint\]|
|Input fields|ADR record sys\_id|

## Resolution notes generation for ADR skill

The resolution notes generation for ADR skill uses the following table and field inputs to generate the resolution notes for an ADR case.

|Input|Description|
|-----|-----------|
|Input table|ADR Complaint \[sn\_telco\_adr\_mgmt\_complaint\]|
|Input fields|ADR record sys\_id|

## Risk signal and issues summarization skill

The risk signal and issues summarization skill includes the inputs that identify the table and fields that are used when a risk signal and issues summary is generated.

<table id="table_ecp_vqk_fhc"><thead><tr><th>

Input

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Input table

</td><td>

Risk signal and issues

</td></tr><tr><td>

Input fields

</td><td>

-   Account Name
-   Priority
-   Description
-   Short description
-   State
-   Source record
-   Category Name
-   Probability

</td></tr></tbody>
</table><table id="table_wps_lrk_fhc"><thead><tr><th>

Input

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Input table

</td><td>

Risk solution

</td></tr><tr><td>

Input fields

</td><td>

-   Source record
-   Source table
-   impacted\_record
-   impacted\_table

</td></tr></tbody>
</table>## Draft risk closure notes summarization skill

The draft risk closure notes summarization skill automatically generates closure notes and closes eligible risk signals at the end of each day based on the status of their associated risk solutions.

<table id="table_f2g_ntt_j3c"><thead><tr><th>

Input

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Input table

</td><td>

Risk signal and issues

</td></tr><tr><td>

Input fields

</td><td>

-   Account Name
-   Priority
-   Description
-   Short description
-   State
-   Source record
-   Category Name
-   Probability

</td></tr></tbody>
</table>## Customer service summary skill

The customer service summary skill helps user to get information on the customer service issues from their knowledge graph. You can configure the input in the following customer service summarization stages:

-   General details
-   Graph questionnaire

    To add or modify the queries, see [Configure the graph questionnaire Now Assist for Telecommunications, Media and Technology \(TMT\)](../task/now-assist-configure-graph-questionnaire.md).

-   Customize prompt

    To customize the prompt, see [Customize a skill in Now Assist for TMT](../task/now-assist-tmt-customize.md).

-   Define access
-   Select display
-   Review and activate

|Input|Description|
|-----|-----------|
|Input table|Service Problem Case \[sn\_sprb\_mgmt.admin\]|

## Service problem case summarization skill

The service problem case summarization skill includes the inputs that identify the table and fields that are used when a service problem case summary is generated. You can configure the input in the following service problem case summarization stages:

-   General details
-   View input
-   Customize prompt
-   Define availability
-   Select display
-   Review and activate

In this release, you can't modify a skill's input data source. The data source contains the tables and fields that the skill relies on.

<table id="table_bsy_bdp_5bc"><thead><tr><th>

Input

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Input table

</td><td>

Service Problem Case \[sn\_sprb\_mgmt\_case\]

</td></tr><tr><td>

Input fields

</td><td>

-   Description
-   Short description
-   Work notes
-   Additional comments
-   Diagnostic Task

Fields:

    -   Description
    -   Short description
    -   Work notes
    -   state
    -   sys id
-   Resolution Task

Fields:

    -   Description
    -   Short description
    -   Work notes
    -   state

</td></tr><tr><td>

Input templates

</td><td>

-   Verify
-   Diagnose
-   Repair
-   Test &amp; Resolve
-   Close

</td></tr></tbody>
</table>## Resolution notes generation skill

The resolution notes generation skill includes the inputs that identify the table and fields that are used when the resolution notes are generated for a service problem case.

In this release, you can't modify a skill's input data source. The data source contains the tables and fields that the skill relies on.

<table id="table_yng_4jp_5bc"><thead><tr><th>

Input

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Input table

</td><td>

Service Problem Case \[sn\_sprb\_mgmt\_case\]

</td></tr><tr><td>

Input fields

</td><td>

-   Description
-   Short description
-   Work notes
-   Additional comments

</td></tr></tbody>
</table>## Test summarization skill

The test summarization skill includes the inputs that identify the table and fields that are used when a test summary is generated.

The following table lists the inputs that you can configure for the test summarization skill.

|Input|Description|
|-----|-----------|
|Input table|Test Run \[sn\_st\_mgmt\_test\]|
|Input field|Name|

<table id="table_g5c_ntm_1cc"><thead><tr><th>

Input

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Input table

</td><td>

Test Measure \[sn\_st\_mgmt\_test\_measure\]

</td></tr><tr><td>

Input field

</td><td>

-   Metric name
-   Metric description
-   Value
-   Rule violation

</td></tr></tbody>
</table>## Knowledge article generation skill

The knowledge article generation skill includes the inputs that identify the table and fields that are used when the knowledge article draft is generated for a case.

In this release, you can't modify a skill's input data source. The data source contains the tables and fields that the skill relies on.

The following table lists the inputs for the knowledge article generation skill.

<table id="table_g5x_yjm_vdc"><thead><tr><th>

Input

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Input table

</td><td>

Case \[sn\_customerservice\_case\]

</td></tr><tr><td>

Input fields

</td><td>

-   Short description
-   Description
-   Resolution notes
-   Work notes
-   Comments

</td></tr></tbody>
</table>## Account onboarding case summarization skill

The account onboarding case summarization skill includes the inputs that identify the table and fields that are used when an account onboarding summary is generated. You can configure the input in the following account onboarding case stages:

-   Form details
-   Data capture
-   Development
-   Training
-   Testing

<table id="table_aj3_mtc_5dc"><thead><tr><th>

Input

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Input table

</td><td>

Account Onboarding Case \[sn\_acct\_lc\_onb\_case\]

</td></tr><tr><td>

Input fields

</td><td>

-   Service Exchange integration
-   Short description
-   Description
-   Go live date
-   Days remaining
-   Work notes
-   Additional comments

</td></tr><tr><td>

Stage - Data Capture

</td><td>

 

</td></tr></tbody>
</table><table id="table_r5b_ftf_5dc"><thead><tr><th>

Input

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Input table

</td><td>

Account Lifecycle Import Task

</td></tr><tr><td>

Input field

</td><td>

-   State
-   Days remaining
-   Published records
-   Work notes
-   Additional comments
-   Target table
-   Total records updated

</td></tr></tbody>
</table><table id="table_e5s_g5f_5dc"><thead><tr><th>

Input

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Input table

</td><td>

Account Lifecycle Task

</td></tr><tr><td>

Input field

</td><td>

-   Short description
-   State
-   Days remaining
-   Type
-   Work notes
-   Additional comments

</td></tr></tbody>
</table><table id="table_xnb_p5f_5dc"><thead><tr><th>

Input

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Input table

</td><td>

Account Lifecycle Import Task

</td></tr><tr><td>

Input field

</td><td>

-   State
-   Days remaining
-   Published records
-   Work notes
-   Additional comments
-   Target table
-   Total records updated

</td></tr></tbody>
</table>## Engagement summarization skill

The engagement summarization skill includes the inputs that identify the table and fields that are used when an engagement summary is generated.

<table id="table_nqb_kvf_5dc"><thead><tr><th>

Input

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Input table

</td><td>

Engagement \[sn\_acct\_lc\_engagement\]

</td></tr><tr><td>

Input fields

</td><td>

-   State
-   Stage
-   Renewal date
-   Initial go-live date
-   Perceived health

</td></tr></tbody>
</table><table id="table_azy_pvf_5dc"><thead><tr><th>

Input

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Input table

</td><td>

Risk and issue

</td></tr><tr><td>

Input fields

</td><td>

-   State
-   Due date
-   Probability

</td></tr></tbody>
</table><table id="table_dk4_5vf_5dc"><thead><tr><th>

Input

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Input table

</td><td>

Internal play

</td></tr><tr><td>

Input fields

</td><td>

-   Due date
-   Progress

</td></tr></tbody>
</table><table id="table_czk_xvf_5dc"><thead><tr><th>

Input

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Input table

</td><td>

Success case

</td></tr><tr><td>

Input fields

</td><td>

-   Due date
-   Progress

</td></tr></tbody>
</table><table id="table_dss_yvf_5dc"><thead><tr><th>

Input

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Input table

</td><td>

Success initiative

</td></tr><tr><td>

Input fields

</td><td>

-   Due date
-   Progress

</td></tr></tbody>
</table><table id="table_h5p_1wf_5dc"><thead><tr><th>

Input

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Input table

</td><td>

Success outcome

</td></tr><tr><td>

Input fields

</td><td>

-   Progress
-   Base value
-   Current value
-   Target value

</td></tr></tbody>
</table>## Touchpoint summarization skill

The touchpoint summarization skill includes the inputs that identify the table and fields that are used when a touchpoint summary is generated.

<table id="table_zsv_mwf_5dc"><thead><tr><th>

Input

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Input table

</td><td>

Engagement \[sn\_acct\_lc\_touchpoint\]

</td></tr><tr><td>

Input fields

</td><td>

-   Squad
-   Progress

</td></tr></tbody>
</table><table id="table_btv_mwf_5dc"><thead><tr><th>

Input

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Input table

</td><td>

Meeting details

</td></tr><tr><td>

Input fields

</td><td>

-   Conference details
-   Meeting type
-   Meeting start time
-   Meeting end time
-   Customer notes
-   Meeting notes
-   State

</td></tr></tbody>
</table>## Customer play summarization skill

The customer play summarization skill includes the inputs that identify the table and fields that are used when a customer play summary is generated.

<table id="table_vv5_4cb_lgc"><thead><tr><th>

Input

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Input table

</td><td>

Customer play

</td></tr><tr><td>

Input fields

</td><td>

-   Engagement
-   Account
-   Progress
-   Days remaining
-   Squad
-   Contact
-   Short description
-   Description
-   Product

</td></tr></tbody>
</table><table id="table_xv5_4cb_lgc"><thead><tr><th>

Input

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Input table

</td><td>

Success task

</td></tr><tr><td>

Input fields

</td><td>

-   State
-   Short description
-   Description
-   Due date

</td></tr></tbody>
</table><table id="table_bnh_jdb_lgc"><thead><tr><th>

Input

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Input table

</td><td>

Meeting details

</td></tr><tr><td>

Input fields

</td><td>

-   State
-   Name
-   Meeting start time
-   Meeting end time

</td></tr></tbody>
</table>## Internal play summarization skill

The internal play summarization skill includes the inputs that identify the table and fields that are used when an internal play summary is generated.

<table id="table_cjk_mdb_lgc"><thead><tr><th>

Input

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Input table

</td><td>

Internal play

</td></tr><tr><td>

Input fields

</td><td>

-   Engagement
-   Account
-   Progress
-   Squad
-   Contract
-   Short description
-   Description
-   Product
-   Days remaining

</td></tr></tbody>
</table><table id="table_ejk_mdb_lgc"><thead><tr><th>

Input

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Input table

</td><td>

Internal play task

</td></tr><tr><td>

Input fields

</td><td>

-   State
-   Short description
-   Description
-   Due date
-   Days remaining

</td></tr></tbody>
</table>## Success initiative summarization skill

The success initiative summarization skill includes the inputs that identify the table and fields that are used when a success initiative summary is generated.

<table id="table_vgq_zdb_lgc"><thead><tr><th>

Input

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Input table

</td><td>

Success initiative

</td></tr><tr><td>

Input fields

</td><td>

-   Primary success outcome
-   Account
-   Sold product name
-   Sold product number
-   Squad
-   Short description
-   Description
-   State
-   Contact
-   Days remaining

</td></tr></tbody>
</table><table id="table_xgq_zdb_lgc"><thead><tr><th>

Input

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Input table

</td><td>

Success task

</td></tr><tr><td>

Input fields

</td><td>

-   State
-   Short description
-   Description
-   Due date
-   Days remaining

</td></tr></tbody>
</table>## Lookup similar engagements skill

The Lookup similar engagements skill includes the inputs that identify the table and fields that are used when a product adoption roadmap is generated.

<table id="table_ffx_5d2_33c"><thead><tr><th>

Input

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Input table

</td><td>

Engagement \[sn\_acct\_lc\_engagement\]

</td></tr><tr><td>

Input fields

</td><td>

-   Phase table
    -   Product usage
    -   Product capability usage
-   Phase field \(Activation status, Business criticality, Customer priority, Usage plan\)

</td></tr></tbody>
</table>## Remote Hands Case Summarization skill

<table id="table_lty_fgf_k3c"><thead><tr><th>

Input

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Input table

</td><td>

Remote Hands Case table \(sn\_remote\_hands\_case\)

</td></tr><tr><td>

Input fields

</td><td>

-   Remote Hands Case table
-   -   Service
-   Priority
-   State
-   Channel
-   Short Description
-   Description

</td></tr></tbody>
</table>