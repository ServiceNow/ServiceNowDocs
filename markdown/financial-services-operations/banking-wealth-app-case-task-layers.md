---
title: Banking &amp; wealth case and task layers by application
description: Case and task definitions for each FSO Banking &amp; Wealth application scope, organized by the customer requests they fulfill and the service definitions behind them. Use this reference when configuring workflows or understanding the structure of case and task layers.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/financial-services-operations/banking-wealth-app-case-task-layers.html
release: brazil
topic_type: reference
last_updated: "2026-09-14"
reading_time_minutes: 9
breadcrumb: [Using case types and service definitions in FSO, Developer resources, Financial Services Operations \(FSO\)]
---

# Banking &amp; wealth case and task layers by application

Case and task definitions for each FSO Banking &amp; Wealth application scope, organized by the customer requests they fulfill and the service definitions behind them. Use this reference when configuring workflows or understanding the structure of case and task layers.

## Business Lifecycle \(sn\_bom\_clo\_b2b\)

Speed customer onboarding and effectively respond to changes during the business lifecycle, with built-in compliance.

<table id="table_business-lifecycle-overview"><thead><tr><th>

Case layer — what the customer requests

</th><th>

Task layer — how the work gets fulfilled

</th></tr></thead><tbody><tr><td>

**Account Lifecycle Service Case** `sn_bom_clo_b2b_account_service`

 -   Onboard new account — `onboard_new_account`
-   Address change for account — `address_change_account`
-   Update business KYC — `kyc_compliance_breach`

 **Contact Lifecycle Service Case** `sn_bom_clo_b2b_contact_service`

 -   Onboard new contact — `onboard_new_contact`

</td><td>

**Account Lifecycle Task** \(shared across this application's case types\) `sn_bom_clo_b2b_account_task`

 -   Update KYC compliance business — `update_kyc_compliance_business`
-   Send business welcome kit — `send_welcome_kit_business`
-   Account activation — `account_activation`
-   Legal due diligence — `legal_due_diligence`
-   Tax due diligence — `tax_due_diligence`
-   Update account — `update_account`
-   Account lifecycle authorization — `account_lifecycle_authorization`
-   Update KYC non compliance business — `update_kyc_non_compliace`

</td></tr></tbody>
</table>## Client Lifecycle \(sn\_bom\_clo\_b2c\)

Speed client onboarding and effectively respond to changes with built-in compliance.

<table id="table_client-lifecycle-overview"><thead><tr><th>

Case layer — what the customer requests

</th><th>

Task layer — how the work gets fulfilled

</th></tr></thead><tbody><tr><td>

**Client Lifecycle Service Case** `sn_bom_clo_b2c_service`

 -   Onboard new customer — `onboard_new_customer`
-   Address change for customer — `address_change_for_customer`
-   Name change of customer — `name_change_of_customer`
-   Update personal KYC — `kyc_compliance_breach`
-   Notice of death — `notice_of_death`

</td><td>

**Client Lifecycle Task** `sn_bom_clo_b2c_task`

 -   Offboard customer — `offboard_customer`
-   Update lending account — `update_lending_account`
-   Send personal welcome kit — `send_welcome_kit_personal`
-   Activate customer — `activate_customer`
-   Update KYC non compliance personal — `update_kyc_non_compliance`
-   Freeze deposit accounts — `freeze_deposit_accounts`
-   Update KYC compliance personal — `update_kyc_compliance_personal`
-   Release funds — `release_funds`
-   Update deposit account — `update_deposit_account`
-   Client lifecycle authorize — `client_lifecycle_task_authorization`
-   Update customer information — `update_customer_information`

</td></tr></tbody>
</table>## Complaint Management \(sn\_bom\_compl\)

Prioritize and quickly resolve complaints in a consistent, controlled, and auditable way.

<table id="table_complaint-management-overview"><thead><tr><th>

Case layer — what the customer requests

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
</table>## Card Operations \(sn\_bom\_credit\_card\)

Digitize card operations across the front, middle, and back office, inclusive of dispute management capabilities.

<table id="table_card-operations-overview"><thead><tr><th>

Case layer — what the customer requests

</th><th>

Task layer — how the work gets fulfilled

</th></tr></thead><tbody><tr><td>

**Card Disputes Service Case** `sn_bom_credit_card_disputes_service`

 -   Dispute card transactions — `dispute_card_transactions`

 **Credit Card Service** `sn_bom_credit_card_service`

 -   Unblock credit card — `unblock_credit_card`
-   New credit card request — `new_credit_card_request`
-   Close credit card — `close_credit_card`
-   Decrease credit card limit — `decrease_credit_card_limit`
-   Increase credit card limit — `increase_credit_card_limit`
-   Block credit card — `block_credit_card`

</td><td>

**Card Disputes Task** `sn_bom_credit_card_disputes_task`

 -   Alert merchant — `alert_merchant`
-   Recovery for final credit — `recover_final_credit`
-   Write off — `write_off`
-   Final credit — `final_credit`
-   Provisional credit — `provisional_credit`
-   Manual investigation — `manual_investigation`
-   Fraud reporting — `fraud_reporting`
-   Initiate chargeback — `initiate_chargeback`
-   Reverse provisional credit — `reverse_provisional_credit`
-   Review pre-arbitration and create response — `review_pre_arb_and_create_response`
-   Evaluate NACHA operating guidelines — `evaluate_nacha_operating_guidelines`
-   Review arbitration response — `review_arbitration_response`
-   Settle payment with customer — `settle_payment_with_customer`
-   Review pre arbitration response and escalate to arbitration — `review_pre_arb_and_escalate_to_arb`
-   Review and respond to collaboration — `review_and_respond_to_collaboration`
-   Review ACH dispute return recommendation — `review_ach_dispute_return_recommendation`
-   Review case filing appeal — `review_arbitration_appeal_response`
-   Review dispute response and create pre arbitration — `review_dispute_response_and_pre_arb`
-   Review case filing and appeal — `review_arbitration_and_appeal`
-   Review case filing response and appeal — `review_arb_response_and_appeal`
-   File ACH return — `file_ach_return`
-   Review friendly fraud — `review_friendly_fraud`
-   Evaluate merchant analysis — `evaluate_merchant_analysis`
-   Review representment — `review_representment`
-   Dispute communication initiation — `dispute_communication_initiation`
-   Review pre arbitration response and create case filing — `review_pre_arb_response_and_arb`
-   Review chargeback response and respond — `review_chargeback_response_and_respond`
-   Verify customer supporting documents — `verify_customer_supporting_documents`
-   Verify ODFI supporting documents — `verify_odfi_supporting_documents`
-   Refund merchant — `refund_merchant`
-   Convert provisional credit to final credit — `convert_provisional_credit`
-   Block card and reissue new card — `block_and_reissue`

 **Card Disputes Transaction** `sn_bom_credit_card_disputes_transaction`

 -   Transaction dispute review — `transaction_dispute_review`

 **Credit Card Task** `sn_bom_credit_card_task`

 -   Credit card task customer agreement — `credit_card_task_customer_agreement`
-   Credit card task product eligibility — `credit_card_task_product_eligibilty`
-   Credit card task account creation — `credit_card_task_account_creation`
-   Credit card task update account — `credit_card_task_update_account`

</td></tr></tbody>
</table>## Intelligent Servicing for Fraud \(sn\_bom\_fraud\)

Facilitate fraud resolution with connected technology and teams in a consistent, controlled, and auditable way.

<table id="table_intelligent-servicing-fraud-overview"><thead><tr><th>

Case layer — what the customer requests

</th><th>

Task layer — how the work gets fulfilled

</th></tr></thead><tbody><tr><td>

**Fraud Case** `sn_bom_fraud_case`

 -   Card fraud by alert — `card_fraud_by_alert`
-   Card fraud — `card_fraud`

</td><td>

**Fraud Task** `sn_bom_fraud_task`

 -   Update fraud management system — `update_fraud_management_system`
-   Unblock card — `unblock_card`
-   Cancel transaction authorization — `cancel_transaction_authorization`
-   Report to risk and compliance team — `report_risk_compliance_team`
-   Write off funds — `write_off_funds`
-   Recover funds — `recover_funds`
-   Review fraud investigation — `review_investigation`
-   Reissue card — `reissue_card`
-   Contact customer — `contact_customer`
-   Block card — `block_card`
-   Report to legal team — `report_to_legal_team`
-   Report suspicious activity — `report_suspicious_activity`
-   Notify customer — `notify_customer`
-   Report to external authorities — `report_to_ext_authorities`

</td></tr></tbody>
</table>## Business Deposit Operations \(sn\_bom\_deposit\_b2b\)

Create transparent and repeatable processes that save time and cost for business deposits.

<table id="table_business-deposit-operations-overview"><thead><tr><th>

Case layer — what the customer requests

</th><th>

Task layer — how the work gets fulfilled

</th></tr></thead><tbody><tr><td>

**Business Deposit Service Case** `sn_bom_deposit_b2b_service`

 -   Manage financial relationship — `manage_financial_relationship`
-   Add business standing order — `add_standing_order_business`
-   Modify business standing order — `modify_standing_order_business`
-   Cancel business standing orders — `cancel_standing_orders_business`
-   Failed business standing order — `failed_standing_order_business`
-   Close business deposit account — `close_deposit_account_business`
-   Originate business deposit account — `originate_deposit_account_business`

</td><td>

**Business Deposit Task** `sn_bom_deposit_b2b_task`

 -   Create and activate business account — `create_and_activate_account_business`
-   Delink business deposit account — `delink_deposit_account_business`
-   Verify business operating instructions — `verify_operating_instructions_business`
-   Update business deposit account — `update_deposit_account_business`
-   Business deposit authorization — `Deposit_authorization_business`
-   Retry business standing order — `retry_standing_order_business`
-   Send business account opening kit — `account_opening_kit`

</td></tr></tbody>
</table>## Personal Deposit Operations \(sn\_bom\_deposit\_b2c\)

Create transparent and repeatable processes that save time and cost for Retail Deposit Operations.

<table id="table_personal-deposit-operations-overview"><thead><tr><th>

Case layer — what the customer requests

</th><th>

Task layer — how the work gets fulfilled

</th></tr></thead><tbody><tr><td>

**Personal Deposit Service Case** `sn_bom_deposit_b2c_service`

 -   Add personal standing order — `add_standing_order`
-   Modify personal standing order — `modify_standing_order`
-   Cancel personal standing orders — `cancel_standing_orders`
-   Failed personal standing order — `failed_standing_order_personal`
-   Add financial account relationship — `add_financial_account_relationship`
-   Modify financial account relationship — `modify_financial_account_relationship`
-   Remove financial account relationship — `remove_financial_account_relationship`
-   Originate personal deposit account — `originate_deposit_account_personal`
-   Close personal deposit account — `close_deposit_account_personal`

</td><td>

**Personal Deposit Task** `sn_bom_deposit_b2c_task`

 -   Create and activate personal account — `create_and_activate_account_personal`
-   Verify personal operating instructions — `verify_operating_instructions`
-   Personal deposit authorization — `deposit_task_authorization_personal`
-   Update personal deposit account — `update_deposit_account_personal`
-   Customer onboarding — `customer_onboarding_deposit_personal`
-   Delink personal deposit account — `delink_deposit_account_personal`
-   Retry personal standing order — `retry_standing_order_personal`
-   Send personal account opening kit — `send_account_opening_kit`

</td></tr></tbody>
</table>## Business Loan Operations \(sn\_bom\_loan\_b2b\)

Make better, faster loan servicing decisions with data-driven automation.

<table id="table_business-loan-operations-overview"><thead><tr><th>

Case layer — what the customer requests

</th><th>

Task layer — how the work gets fulfilled

</th></tr></thead><tbody><tr><td>

**Business Loan Service Case** `sn_bom_loan_b2b_service`

 -   Business loan restructure — `loan_restructure_business`
-   Loan drawdown — `loan_drawdown_business`
-   Business loan partial prepayment — `partial_prepayment_business`
-   Business loan deferment — `loan_deferment_business`
-   Business loan forgiveness — `loan_forgiveness_business`
-   Loan rollover — `loan_rollover_business`
-   Business loan write off — `loan_write_off_business`
-   Business missed installment repayment — `missed_installment_repayment_business`

</td><td>

**Business Loan Task** `sn_bom_loan_b2b_task`

 -   Business loan task authorization — `loan_task_authorization_business`
-   Business loan task review — `loan_task_review_business`
-   Business loan task update account — `loan_task_update_account_business`
-   Loan task disbursement — `loan_task_disbursement_business`

</td></tr></tbody>
</table>## Personal Loan Operations \(sn\_bom\_loan\)

Financial Services Personal Loan Operations workflows for customer requests.

<table id="table_personal-loan-operations-overview"><thead><tr><th>

Case layer — what the customer requests

</th><th>

Task layer — how the work gets fulfilled

</th></tr></thead><tbody><tr><td>

**Personal Loan Service Case** `sn_bom_loan_service`

 -   Personal loan restructure — `loan_restructure_personal`
-   Personal loan partial prepayment — `partial_prepayment_personal`
-   Personal loan deferment — `loan_deferment_personal`
-   Personal loan forgiveness — `loan_forgiveness_personal`
-   Personal missed installment repayment — `missed_installment_repayment_personal`
-   Personal loan write off — `loan_write_off_personal`

</td><td>

**Personal Loan Task** `sn_bom_loan_task`

 -   Personal loan task review — `loan_task_review_personal`
-   Personal loan task authorization — `loan_task_authorization_personal`
-   Personal loan task update account — `loan_task_update_account_personal`

</td></tr></tbody>
</table>## Credit Operations \(sn\_bom\_credit\_asmt\)

Credit assessment and covenant monitoring across business and personal lending.

<table id="table_credit-operations-overview"><thead><tr><th>

Case layer — what the customer requests

</th><th>

Task layer — how the work gets fulfilled

</th></tr></thead><tbody><tr><td>

**Business Loan Credit Service Case** `sn_bom_credit_asmt_loan_b2b_service`

 -   Business loan restructure proposal — `loan_restructure_proposal_business`
-   Business covenant breach — `covenant_breach_business`

 **Personal Loan Credit Service Case** `sn_bom_credit_asmt_loan_service`

 -   Personal loan restructure proposal — `loan_restructure_proposal_personal`
-   Personal covenant breach — `covenant_breach_personal`

 **Business Credit Service Case** `sn_bom_credit_asmt_b2b_service`

 No service definitions configured.

 **Personal Credit Service Case** `sn_bom_credit_asmt_service`

 No service definitions configured.

</td><td>

**Business Credit Task** \(shared across this application's case types\) `sn_bom_credit_asmt_b2b_task`

 -   Business credit authorization — `credit_authorization_business`
-   Business credit review — `credit_review_business`
-   Update business covenant — `update_covenant_business`
-   Business credit assessment — `credit_assessment_business`

 **Credit Task** \(shared across this application's case types\) `sn_bom_credit_asmt_task`

 -   Update personal covenant — `update_covenant_personal`
-   Personal credit assessment — `credit_assessment_personal`
-   Personal credit review — `credit_review_personal`
-   Personal credit authorization — `credit_authorization_personal`

</td></tr></tbody>
</table>## Payment Operations \(sn\_bom\_payment\)

Consolidate requests for payment operations and route them to appropriate teams across the middle and back office.

<table id="table_payment-operations-overview"><thead><tr><th>

Case layer — what the customer requests

</th><th>

Task layer — how the work gets fulfilled

</th></tr></thead><tbody><tr><td>

**Claim** `sn_bom_payment_claim`

 -   Internal claim — `internal_claim`
-   External claim — `external_claim`

 **Payment Inquiry Case** `sn_bom_payment_inquiry`

 -   Payment in error — `payment_in_error`
-   Beneficiary claim non-receipt - internal — `beneficiary_claim_non_receipt_internal`
-   Beneficiary claim non-receipt - external — `beneficiary_claim_non_receipt_external`

 **Payment Service** `sn_bom_payment_service`

 -   Debit approval — `debit_approval`

</td><td>

This application has no task-level service definitions.

</td></tr></tbody>
</table>## Treasury Operations \(sn\_bom\_treasury\)

Speed onboarding for treasury services with streamlined workflows and eliminate redundant requests for customer information.

<table id="table_treasury-operations-overview"><thead><tr><th>

Case layer — what the customer requests

</th><th>

Task layer — how the work gets fulfilled

</th></tr></thead><tbody><tr><td>

**RDC Service Case** `sn_bom_treasury_rdc_service`

 -   Onboard RDC service — `onboard_rdc_service`

 **Wire Service Case** `sn_bom_treasury_wire_service`

 -   Onboard wire service — `onboard_wire_service`

</td><td>

**Treasury Task** \(shared across this application's case types\) `sn_bom_treasury_task`

 -   Send activation email — `send_activation_email`
-   Activate RDC service — `activate_rdc_service`
-   Initiate customer training — `initiate_customer_training`
-   Due diligence - RDC — `due_diligence_rdc`
-   Activate wire service — `activate_wire_service`

</td></tr></tbody>
</table>## Financial Services Operations Core \(sn\_bom\)

Core Financial Services data model used in Financial Services Operations.

<table id="table_fso-core-overview"><thead><tr><th>

Case layer — what the customer requests

</th><th>

Task layer — how the work gets fulfilled

</th></tr></thead><tbody><tr><td>

**Financial Services Case** `sn_bom_financial_service`

 No service definitions configured.

</td><td>

This application has no task-level service definitions.

</td></tr></tbody>
</table>## Know Your Customer \(sn\_bom\_kyc\)

Shared KYC task library consumed by the lifecycle applications.

<table id="table_know-your-customer-overview"><thead><tr><th>

Case layer — what the customer requests

</th><th>

Task layer — how the work gets fulfilled

</th></tr></thead><tbody><tr><td>

This application defines no case types.

</td><td>

**KYC Account Task** `sn_bom_kyc_account_task`

 -   CDD - Account — `cdd_account`

 **KYC Contact Task** `sn_bom_kyc_contact_task`

 -   CDD - Contact — `cdd_contact`
-   Socure - CDD - Contact — `socure_cdd_contact`

 **KYC Customer Task** `sn_bom_kyc_customer_task`

 -   Socure - CDD - Customer — `socure_cdd_customer`
-   CDD - Customer — `cdd_customer`

</td></tr></tbody>
</table>**Parent Topic:**[Using case types and service definitions in FSO](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/financial-services-operations/fso-int_guide-work_case_types.md)

