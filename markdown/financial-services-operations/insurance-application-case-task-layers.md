---
title: Insurance case and task layers by application
description: Case and task definitions organized by FSO Insurance application scope. Use this reference to identify which service definitions support each case type and task type across personal lines, commercial lines, life insurance, claims, and underwriting applications.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/financial-services-operations/insurance-application-case-task-layers.html
release: brazil
topic_type: reference
last_updated: "2026-09-14"
reading_time_minutes: 6
breadcrumb: [Using case types and service definitions in FSO, Developer resources, Financial Services Operations \(FSO\)]
---

# Insurance case and task layers by application

Case and task definitions organized by FSO Insurance application scope. Use this reference to identify which service definitions support each case type and task type across personal lines, commercial lines, life insurance, claims, and underwriting applications.

## Personal Lines Servicing \(sn\_ins\_policy\_b2c\)

Handle mid-term policy changes and coverage inquiries for personal auto and homeowners policyholders across phone, digital, and self-service channels.

<table id="table_personal-lines-servicing-overview"><thead><tr><th>

Case layer — what the policyholder requests

</th><th>

Task layer — how the work gets fulfilled

</th></tr></thead><tbody><tr><td>

**Auto Policy Case** `sn_ins_policy_b2c_service`

 -   Personal auto change coverage — `personal_auto_change_coverage`

 **Homeowner Policy Case** `sn_ins_policy_b2c_home_service`

 -   Homeowners change coverage — `homeowners_change_coverage`

</td><td>

**Auto Policy Task** `sn_ins_policy_b2c_task`

 -   Personal auto update policy — `personal_auto_update_policy`
-   Personal auto send policy document — `personal_auto_send_policy_document`

 **Homeowner Policy Task** `sn_ins_policy_b2c_home_service_task`

 -   Homeowners update policy — `homeowners_update_policy`
-   Homeowners send policy documents — `homeowners_send_policy_documents`

</td></tr></tbody>
</table>## Commercial Lines Servicing \(sn\_ins\_policy\_b2b\)

Service commercial policies with support for the agent and broker relationship model, multi-party policy structures, and audit-ready controls.

<table id="table_commercial-lines-servicing-overview"><thead><tr><th>

Case layer — what the policyholder requests

</th><th>

Task layer — how the work gets fulfilled

</th></tr></thead><tbody><tr><td>

**Business Owner Policy Case** `sn_ins_policy_b2b_bop_service`

 -   BOP change coverage — `bop_change_coverage`

</td><td>

**Business Owner Policy Task** `sn_ins_policy_b2b_bop_task`

 -   BOP update policy — `bop_update_policy`
-   BOP send policy documents — `bop_send_policy_documents`

</td></tr></tbody>
</table>## Complaint Management \(sn\_bom\_compl\)

Prioritize and quickly resolve policyholder complaints in a consistent, controlled, and auditable way — common app, shared with every FSO vertical.

<table id="table_complaint-management-overview"><thead><tr><th>

Case layer — what the policyholder requests

</th><th>

Task layer — how the work gets fulfilled

</th></tr></thead><tbody><tr><td>

**Complaint Case** `sn_bom_compl_service`

 -   Complaint service — `complaint_service`

</td><td>

**Complaint Service Task** `sn_bom_compl_task`

 -   Complaint fulfillment — `complaint_fulfillment`
-   Complaint legal fulfillment — `complaint_legal_fulfillment`

 **Quality Control Task** `sn_bom_compl_qc_task`

 -   Complaint draft response — `complaint_draft_response`

</td></tr></tbody>
</table>## Individual Life Servicing \(sn\_ins\_indiv\_life\)

Manage beneficiary changes, coverage adjustments, and policy loans for individual life and disability policyholders.

<table id="table_individual-life-servicing-overview"><thead><tr><th>

Case layer — what the policyholder requests

</th><th>

Task layer — how the work gets fulfilled

</th></tr></thead><tbody><tr><td>

**Individual Life Policy Case** `sn_ins_indiv_life_service`

 -   Cancel policy — `indiv_life_policy_cancellation`
-   Increase coverage — `indiv_life_increase_coverage`
-   Policy Loan Request — `policy_loan_request`
-   Add/Change beneficiary — `indiv_life_change_beneficiary`
-   Convert term to perm — `indiv_life_convert_term_to_perm`
-   Decrease coverage — `indiv_life_decrease_coverage`

</td><td>

**Individual Life Policy Task** `sn_ins_indiv_life_task`

 -   Update individual life policy — `indiv_life_update_policy`
-   Request medical exam — `sn_request_medical_exam`
-   Review Loan Request — `review_loan_request`
-   Review Policy and Claim Details — `review_policy_claim_details`
-   Review Previous Case Details — `review_previous_case_details`
-   Initiate Quality Review — `initiate_quality_review`
-   Share Payment Details To Disbursement System — `share_payment_details`
-   Initiate Loan Request Task — `initiate_loan_request_task`
-   Compare Loan Amount with Maximum and Threshold — `compare_loan_amount_with_max_threshold`
-   Send individual life policy documents — `indiv_life_send_policy_documents`

</td></tr></tbody>
</table>## Group Life Servicing \(sn\_ins\_group\_life\)

Administer group life and employee benefits policies through the employer and group administrator relationship rather than the individual policyholder.

<table id="table_group-life-servicing-overview"><thead><tr><th>

Case layer — what the group administrator requests

</th><th>

Task layer — how the work gets fulfilled

</th></tr></thead><tbody><tr><td>

**Group Life Policy Case** `sn_ins_group_life_service`

 -   Group life change member info — `group_life_change_member_info`

</td><td>

**Group Life Policy Task** `sn_ins_group_life_task`

 -   Group life update policy — `group_life_update_policy`
-   Group life send policy documents — `group_life_send_policy_documents`

</td></tr></tbody>
</table>## Personal Lines Claims \(sn\_ins\_claim\_pers\)

Run the personal auto and accident claims lifecycle from first notice of loss through resolution with persona-based adjuster workspaces.

<table id="table_personal-lines-claims-overview"><thead><tr><th>

Case layer — what the policyholder requests

</th><th>

Task layer — how the work gets fulfilled

</th></tr></thead><tbody><tr><td>

**Personal Auto Claim Case** `sn_ins_claim_pers_auto_service`

 -   Personal auto policy report claim — `personal_auto_policy_claim`

 **Personal Accident Claim Case** `sn_ins_claim_pers_accident_claim_case`

 -   Personal accident policy report claim — `personal_accident_policy_report_claim`

</td><td>

**Personal Auto Claim Task** `sn_ins_claim_pers_auto_task` — shared across this application's case types

 -   Personal auto close claim — `pers_auto_close_claim`
-   Personal auto manual claim validation — `pers_auto_claim_manual_validation`

 **Personal Auto Claim Adjuster Task** `sn_ins_claim_pers_auto_adj_task` — shared across this application's case types

 -   Personal auto claim review — `pers_auto_claim_review`

</td></tr></tbody>
</table>## Commercial Lines Claims \(sn\_ins\_claim\_cml\)

Coordinate multi-adjuster commercial auto claims from FNOL through settlement, with manual validation and straight-through closure paths.

<table id="table_commercial-lines-claims-overview"><thead><tr><th>

Case layer — what the policyholder requests

</th><th>

Task layer — how the work gets fulfilled

</th></tr></thead><tbody><tr><td>

**Commercial Auto Claim Case** `sn_ins_claim_cml_auto_service`

 -   Commercial auto policy report claim — `commercial_auto_policy_claim`

</td><td>

**Commercial Auto Claim Task** `sn_ins_claim_cml_auto_task`

 -   Commercial auto manual claim validation — `manual_cml_auto_claim_validation`
-   Commercial auto close claim — `cml_auto_close_claim`

 **Commercial Auto Claim Adjuster Task** `sn_ins_claim_cml_auto_adj_task`

 -   Commercial auto claim review — `cml_auto_claim_review`

</td></tr></tbody>
</table>## Individual Life Claims \(sn\_ins\_claim\_indl\)

Digitize individual life death-claim intake with beneficiary verification and task orchestration across the carrier and beneficiary journey.

<table id="table_individual-life-claims-overview"><thead><tr><th>

Case layer — what the beneficiary requests

</th><th>

Task layer — how the work gets fulfilled

</th></tr></thead><tbody><tr><td>

**Individual Death Claim** `sn_ins_claim_indl_death_case`

 -   Report individual death claim — `indiv_death_claim_report`

 **Related Death Policy Claim** `sn_ins_claim_indl_rel_death_case` — no service definitions configured.

</td><td>

**Individual Death Claim Task** `sn_ins_claim_indl_death_task` — shared across this application's case types — no service definitions configured.

</td></tr></tbody>
</table>## Insurance Claims \(sn\_ins\_gen\_claim\)

A single configurable claims framework that adapts to any line of business — P&amp;C, life, travel, or others — without new case types, shown here with a travel insurance configuration.

<table id="table_insurance-claims-overview"><thead><tr><th>

Case layer — what the claimant requests

</th><th>

Task layer — how the work gets fulfilled

</th></tr></thead><tbody><tr><td>

**Claim Case** `sn_ins_gen_claim_case`

 -   Report accidental injury benefit claim — `report_accidental_injury_benefit_claim`
-   Report Personal Property Damage Benefit Claim — `personal_property_damage_claim`
-   Report travel claim — `general_claim_report`

</td><td>

**Claim Task** `sn_ins_gen_claim_task` — no service definitions configured.

 **Claim Adjuster Task** `sn_ins_gen_claim_adj_task`

 -   Quality Review Task — `Quality_Review_Task`
-   Travel claim trip incident adjuster review — `travel_claim_trip_adj_review`
-   Review Previous Case Details — `Review_Previous_Case_Details_Per_Acciden`
-   Share Payment Details To Disbursement System — `share_payment_details_claims`
-   Travel claim baggage incident adjuster review — `travel_claim_baggage_adj_review`
-   Compare Estimated Payment with Reserve — `Compare_Estimated_Payment_with_Reserve`
-   Personal Property Damage Adjuster Review — `personal_property_damage_adjuster_review`
-   Accidental Injury Adjuster Review — `accidental_injury_adjuster_review`
-   Bodily Injury Adjuster Task — `bodily_injury_adjuster_task`
-   Review Policy Details and Eligibility — `review_policy_details_and_eligibility`

</td></tr></tbody>
</table>## Personal Lines Underwriting \(sn\_ins\_underwrite\)

Shared underwriting task library consumed by the personal lines servicing app to review coverage and terms on requested policy changes.

<table id="table_personal-lines-underwriting-overview"><thead><tr><th>

Case layer — what the policyholder requests

</th><th>

Task layer — how the work gets fulfilled

</th></tr></thead><tbody><tr><td>

This application defines no case types.

</td><td>

**Underwriting Service Task** `sn_ins_underwrite_b2c_task`

 -   Underwriter coverage review — `underwriter_coverage_review`

</td></tr></tbody>
</table>## Commercial Lines Underwriting \(sn\_ins\_uw\_b2b\)

Shared underwriting task library consumed by the commercial lines servicing app to approve new coverages and terms on a policy.

<table id="table_commercial-lines-underwriting-overview"><thead><tr><th>

Case layer — what the policyholder requests

</th><th>

Task layer — how the work gets fulfilled

</th></tr></thead><tbody><tr><td>

This application defines no case types.

</td><td>

**Commercial Underwriting Service Task** `sn_ins_uw_b2b_task`

 -   Commercial lines underwriting approval — `commercial_lines_underwriting_approval`

</td></tr></tbody>
</table>## Individual Life Underwriting \(sn\_ins\_indiv\_uw\)

Shared underwriting task library consumed by the individual life servicing app to approve requested coverage increases.

<table id="table_individual-life-underwriting-overview"><thead><tr><th>

Case layer — what the policyholder requests

</th><th>

Task layer — how the work gets fulfilled

</th></tr></thead><tbody><tr><td>

This application defines no case types.

</td><td>

**Individual Life Underwriting Service Task** `sn_ins_indiv_uw_task`

 -   Individual life increase coverage underwriter approval — `indiv_life_incr_cov_uw_approval`

</td></tr></tbody>
</table>## Group Life Underwriting \(sn\_ins\_group\_uw\)

Shared underwriting task library consumed by the group life servicing app to approve new member info on a group policy.

<table id="table_group-life-underwriting-overview"><thead><tr><th>

Case layer — what the group administrator requests

</th><th>

Task layer — how the work gets fulfilled

</th></tr></thead><tbody><tr><td>

This application defines no case types.

</td><td>

**Group Life Underwriting Service Task** `sn_ins_group_uw_task`

 -   Group life underwriting approval — `group_life_underwriting_approval`

</td></tr></tbody>
</table>## Insurance Special Investigations \(sn\_ins\_siu\)

Shared SIU task library consumed by the personal and commercial auto claims apps to investigate claims flagged for potential fraud.

<table id="table_insurance-special-investigations-overview"><thead><tr><th>

Case layer — what the policyholder requests

</th><th>

Task layer — how the work gets fulfilled

</th></tr></thead><tbody><tr><td>

This application defines no case types.

</td><td>

**SIU Task** `sn_ins_siu_task`

 -   Commercial auto claim evaluation for fraud — `cml_auto_claim_evaluation_for_fraud`
-   Personal auto claim evaluation for fraud — `pers_auto_claim_evaluation_for_fraud`

</td></tr></tbody>
</table>**Parent Topic:**[Using case types and service definitions in FSO](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/financial-services-operations/fso-int_guide-work_case_types.md)

