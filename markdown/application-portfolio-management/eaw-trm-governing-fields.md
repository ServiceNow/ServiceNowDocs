---
title: Governing TRM product fields
description: The TLM Technology Lifecycle \[sn\_apm\_tpm\_technology\_lifecycle\] table includes fields that link a discovered technology to the TRM product and product lifecycle that govern its obsolescence status.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/application-portfolio-management/eaw-trm-governing-fields.html
release: zurich
topic_type: reference
last_updated: "2026-08-24"
reading_time_minutes: 2
keywords: [governing TRM product, TPM technology lifecycle, TRM product lifecycle, obsolescence status]
breadcrumb: [Reference, Enterprise Architecture Workspace, Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# Governing TRM product fields

The TLM Technology Lifecycle \[sn\_apm\_tpm\_technology\_lifecycle\] table includes fields that link a discovered technology to the TRM product and product lifecycle that govern its obsolescence status.

This functionality requires Enterprise Architecture Workspace version 10.0.0 or later and TPM plugin \(sn\_apm\_tpm\) version 1.12.0 or later.

## Governing TRM product fields

The TLM Technology Lifecycle \[sn\_apm\_tpm\_technology\_lifecycle\] record includes the following fields. The system populates these fields only for software; for hardware, these fields remain unpopulated.

|Field|Description|
|-----|-----------|
|**Governing TRM Product**|Reference to the TRM product that governs the obsolescence status of this discovered technology. Cleared if no matching TRM product is found.|
|**Governing TRM Product Lifecycle**|Reference to the specific TRM product lifecycle \(version, or version and edition\) that matches this discovered technology. Cleared if no TRM product lifecycle matches, even when a **Governing TRM Product** is populated.|

## Field population by reason

The scheduled job **Populate TRM technical debts in the EA Workspace** populates or clears these fields each time it runs, based on whether the discovered technology matches a TRM standard.

|Reason|**Governing TRM Product**|**Governing TRM Product Lifecycle**|
|------|-------------------------|-----------------------------------|
|Software product has no TRM product defined|Cleared|Cleared|
|TRM product exists but is not production approved|Populated|Cleared|
|TRM product is approved but no matching lifecycle version is found|Populated|Cleared|
|Matching lifecycle exists but is not production approved|Populated|Populated|
|Lifecycle matches and is production approved \(no technical debt is created\)|Populated|Populated|

**Note:** On later job runs, if the discovered technology's underlying TRM product or lifecycle changes, these fields update to reflect the new match. If a previously matched TRM product is removed, both fields clear. If only the lifecycle match is lost while the TRM product match remains, only **Governing TRM Product Lifecycle** clears.

**Parent Topic:**[Enterprise Architecture Workspace reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-portfolio-management/eaw-reference.md)

**Related topics**  


[View technology lifecycle details](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-portfolio-management/eaw-view-tech-lifecycle.md)

[Technical debt calculation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-portfolio-management/eaw-trm-technical-debt-calc.md)

[Update TRM technical debt data using scheduled job](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-portfolio-management/eaw-run-job-trm-tech-debts.md)

