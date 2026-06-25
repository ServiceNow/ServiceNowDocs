---
title: Streamlining the supplier risk assessment workflow
description: As procurement specialists, track activity on the Third-Party Risk Management \(TPRM\) records, and update and make changes to the sourcing requests and purchase requests based on the final risk rating.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/sourcing-and-procurement-operations/simplify-risk-assessment-wf.html
release: australia
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Working with playbooks, Use, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Streamlining the supplier risk assessment workflow

As procurement specialists, track activity on the Third-Party Risk Management \(TPRM\) records, and update and make changes to the sourcing requests and purchase requests based on the final risk rating.

With the due diligence playbook for due diligence case types, procurement specialists no longer need multiple clicks to manually update any tasks that they need to complete during the different stages of the supplier risk assessment workflow. They no longer need to open the supplier tiering assessment and risk assessment cases that get auto-triggered whenever there’s a need for supplier qualification. With the TRPM capabilities, when a sourcing request is added to a sourcing event, in the Qualification needed state, a supplier case of type due diligence is triggered to address risk assessments. The risk team is responsible for the workflow after the due diligence is triggered.

With this due diligence playbook, procurement specialists, sourcing managers, and procurement managers no longer need to handle these activities outside the system through emails, phone calls, or weekly zoom meetings with the risk team. There’s no need to check for any updates from the tiering assessor and update them back to their own working records. They’re also relieved from remembering or finding the appropriate records to update when the risk assessment is complete.

The tiering assessor must complete the tiering questionnaire after the supply manager submits the tiering questionnaire. The state of the tiering assessment questionnaire changes to Awaiting response.

The supplier contact completes the risk assessment from the supplier collaboration portal. For more information on this, see [Complete a risk assessment from the Supplier Collaboration Portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/complete-risk-assessments.md).

Note the following scenarios:

-   When Supplier Lifecycle Operations is installed, and the supplier is new, the Due Diligence Request \(DDR\) is created in Supplier Lifecycle Operations as a supplier case, and the due diligence case is taken care of through the onboard a supplier case.
-   When Supplier Lifecycle Operations is installed, but the supplier is old and already onboarded, the DDR is created as a procurement case.
-   When Supplier Lifecycle Operations is not installed, irrespective of whether the supplier is old or new, the DDR is created in Sourcing and Procurement Operations as a procurement case.

For information on how Supplier Lifecycle Operations similarly assesses suppliers during the onboarding process, see [Minimize risk by assessing suppliers during the onboarding process](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/better-together/better-tprm-slo.md). For detailed information on the supplier onboarding playbook, see [Use the supplier onboarding playbook to onboard suppliers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/use-playbooks-onboard-supp.md).

For information on how to configure TPRM, see [Configuring Third-party Risk Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/tprm-configuring.md). For detailed information on the due diligence workflow, see [Due diligence workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/tprm-workflow-in-workspace.md).

-   **[Track risk assessments from the due diligence playbook](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/track-risk-assess-due-diligence-playbook.md)**  
As procurement specialists, use the due diligence playbook to track supplier risk assessments and complete the associated tasks.

**Parent Topic:**[Working with Sourcing and Procurement Operations playbooks in the Source-to-Pay Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/work-playbooks-spo.md)

**Related topics**  


[Process a purchase order edit in playbook]()

[Process a purchase requisition edit request in playbook]()

[Process a return request in playbook]()

[Process a replacement request in playbook]()

[Process an edit receipt request in playbook]()

[Fulfilling request for copy of contract in playbook]()

[Routing NDAs to suppliers]()

[Verifying delivery addresses in playbook]()

[Reviewing and updating general ledger details in playbook]()

[Sourcing intake guided experience with playbooks]()

