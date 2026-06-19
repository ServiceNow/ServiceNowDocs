---
title: Grant Proposal funding statuses
description: Status values a grant proposal can hold during the Funding Allocation workflow, including the trigger, the responsible role, and whether the status is terminal.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/government-industry/public-sector-digital-services/psds-gm-proposal-funding-status-ref.html
release: australia
product: Public Sector Digital Services
classification: public-sector-digital-services
topic_type: reference
last_updated: "2026-06-08"
reading_time_minutes: 1
breadcrumb: [Grants Management reference, Reference, Public Sector Digital Services \(PSDS\)]
---

# Grant Proposal funding statuses

Status values a grant proposal can hold during the Funding Allocation workflow, including the trigger, the responsible role, and whether the status is terminal.

|Status|Definition|Triggered by|Role|Terminal|
|------|----------|------------|----|--------|
|Undecided|Default state after scoring. No recommendation applied.|System \(automatic\)|None|No|
|Marked for Funding|Grant program manager has flagged the proposal for potential funding. Tentative and reversible before submission.|Mark for funding action|Grant program manager|No|
|Marked for Decline|Grant program manager has flagged the proposal for potential decline. Tentative and reversible before submission.|Mark for decline action|Grant program manager|No|
|Submitted for Funding|Grant program manager has submitted the proposal to the Grant Program Director for potential funding as part of a Funding Request. Proposals are locked.|Send for approval action|Grant program manager|No|
|Submitted for Decline|Grant program manager has submitted the proposal to the Grant Program Director for potential decline as part of a Funding Request. Proposals are locked.|Send for approval action \(decline track\)|Grant program manager|No|
|Funding confirmed|Grant Program Director has confirmed the funding recommendation. Proceeds to award notice generation, agreement signing, and contracting.|Grant Program Director approves the funding request|Grant Program Director|Yes|
|Decline confirmed|Proposal formally declined after Grant Program Director review. Proceeds to rejection letter generation.|Grant Program Director approves the funding request \(decline track\)|Grant Program Director|Yes|
|Returned|Grant Program Director has sent the proposal back for revision. Proposal remains in the Returned state in the grant program manager's working queue. Budget is released.|Grant Program Director rejects the funding request|Grant Program Director|No|

